---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spositerestrictedappaccesscontrolmode
applicable: SharePoint Online
title: Set-SPOSiteRestrictedAppAccessControlMode
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Set-SPOSiteRestrictedAppAccessControlMode switches a site between Allow and Deny modes while preserving both application lists. Learn the syntax and examples.
ms.date: 10/13/2026
ms.topic: reference
---

# Set-SPOSiteRestrictedAppAccessControlMode

## SYNOPSIS

Sets the active mode of the site-level Application Restrictions policy to `Allow` or `Deny`, preserving site enablement and both lists.

## SYNTAX

```powershell
Set-SPOSiteRestrictedAppAccessControlMode [-Identity] <String> -Mode <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Set-SPOSiteRestrictedAppAccessControlMode` cmdlet to change which list a site enforces. This cmdlet changes the active mode only. It preserves site enablement and both the allow list and the deny list.

Application Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and Application Restrictions.

The active mode selects the list that is enforced:

- **Allow** - applications in the allow list pass the Application Restrictions check, and all other governed applications are denied by the site policy. An empty active allow list causes the site policy to deny all governed third-party and agentic applications.
- **Deny** - applications in the deny list are denied by the site policy, and all other governed applications pass the Application Restrictions check. An empty active deny list means the site policy denies none of them.

Both lists are always stored and can be managed regardless of which mode is active. Only the list selected by the active mode participates in runtime enforcement. The inactive list is preserved for future mode changes and has no runtime effect. A mode must be explicitly configured before the site policy can be enabled.

Because a mode switch can change the effective decision for every governed application on the site, the cmdlet displays a warning before it makes the change. The warning identifies the current mode, the target mode, the size of the newly active preserved list, and the new default decision, and it clearly states that both lists are preserved. The cmdlet then asks you to confirm. Use `-WhatIf` to display the same impact without changing the policy.

Configuration and enablement are orthogonal: a mode change never turns enforcement on. Site enforcement is turned on only by `Enable-SPOSiteRestrictedAppAccessControl`, so you can stage a mode and lists and then enable the site explicitly. The only combination the backend rejects is enabled with mode `None`.

Site enforcement is also gated by the tenant switch. While the tenant switch is on, the tenant deny list takes precedence and can't be overridden by a site allow list.

Automation can use the standard `-Confirm:$false`. Suppressing the prompt doesn't bypass validation, authorization, auditing, or first-party protection.

Site Application Restrictions administration is isolated from the general-purpose `Get-SPOSite` and `Set-SPOSite` cmdlets. `Get-SPOSite` doesn't load site policy data and `Set-SPOSite` can't change it. Use the dedicated Application Restrictions cmdlets listed in [Related Links](#related-links).

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Set-SPOSiteRestrictedAppAccessControlMode -Identity https://contoso.sharepoint.com/sites/Finance -Mode Allow
```

This example sets the active mode of the Finance site to `Allow`. Applications in the site allow list pass the Application Restrictions check, and all other governed applications are denied by the site policy. Existing Microsoft Entra consent and SharePoint authorization still apply. The deny list is preserved but becomes inactive. The cmdlet displays the mode-switch warning and asks for confirmation before it applies the change.

### Example 2

```powershell
Set-SPOSiteRestrictedAppAccessControlMode -Identity https://contoso.sharepoint.com/sites/Finance -Mode Deny -WhatIf
```

This example displays the impact of switching the Finance site to `Deny`, including the current mode, the target mode, the size of the newly active deny list, and the new default decision, without changing the policy.

### Example 3

```powershell
Set-SPOSiteRestrictedAppAccessControlMode -Identity 8a1e30f6-2f52-4b9e-9d1b-2e9f6c1d40aa -Mode Deny -Confirm:$false
```

This example switches a site identified by its ID to `Deny` without prompting, for use in automation. Suppressing the prompt doesn't bypass validation, authorization, auditing, or first-party protection.

### Example 4

```powershell
Set-SPOSiteRestrictedAppAccessControlMode -Identity https://contoso.sharepoint.com/sites/Finance -Mode Allow
Enable-SPOSiteRestrictedAppAccessControl -Identity https://contoso.sharepoint.com/sites/Finance
```

This example stages the mode first and then turns enforcement on explicitly. A mode change never turns enforcement on by itself.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the site to configure. You can specify either the site URL or the site ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Mode

> Applicable: SharePoint Online

Specifies the active mode of the site policy. Valid values are `Allow` and `Deny`.

When the mode is `Allow`, applications in the allow list pass the Application Restrictions check and all other governed applications are denied by the site policy. When the mode is `Deny`, applications in the deny list are denied by the site policy and all other governed applications pass the Application Restrictions check. Both lists are preserved either way. Existing Microsoft Entra consent and SharePoint authorization still apply.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before running the cmdlet. This cmdlet uses `ConfirmImpact.High`, so it prompts by default. Use `-Confirm:$false` to suppress the prompt in automation.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Online

Shows what would happen if the cmdlet runs. The cmdlet isn't run. `-WhatIf` displays the same mode-switch impact as the confirmation warning without changing the policy.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### None

## NOTES

- A mode change changes only the active mode. It preserves site enablement and both lists.
- Before the switch, the cmdlet warns with the current mode, target mode, size of the newly active preserved list, and new default decision.
- The warning states that both lists are preserved, and the cmdlet asks for confirmation.
- An empty active allow list causes the site policy to deny all governed third-party and agentic applications. An empty active deny list means the site policy denies none of them. Existing Microsoft Entra consent and SharePoint authorization still apply.
- Configuration and enablement are orthogonal. Site enforcement is turned on only by `Enable-SPOSiteRestrictedAppAccessControl`. The only combination the backend rejects is enabled with mode `None`.
- The tenant switch gates all site enforcement. While the tenant switch is on, the tenant deny list can't be overridden by a site allow list.
- Use `Get-SPOSiteRestrictedAppAccessControl` to confirm the resulting mode and both lists.

## RELATED LINKS

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Set-SPOSiteRestrictedAppAccessControlList](Set-SPOSiteRestrictedAppAccessControlList.md)

[Enable-SPOSiteRestrictedAppAccessControl](Enable-SPOSiteRestrictedAppAccessControl.md)

[Disable-SPOSiteRestrictedAppAccessControl](Disable-SPOSiteRestrictedAppAccessControl.md)

[Clear-SPOSiteRestrictedAppAccessControlList](Clear-SPOSiteRestrictedAppAccessControlList.md)

[Clear-SPOSiteRestrictedAppAccessControlPolicy](Clear-SPOSiteRestrictedAppAccessControlPolicy.md)

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
