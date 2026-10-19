---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/enable-spositerestrictedappaccesscontrol
applicable: SharePoint Online
title: Enable-SPOSiteRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Enable-SPOSiteRestrictedAppAccessControl turns on Application Restrictions enforcement for a SharePoint site using its configured mode and lists. Learn syntax and examples.
ms.date: 10/13/2026
ms.topic: reference
---

# Enable-SPOSiteRestrictedAppAccessControl

## SYNOPSIS

Turns on Application Restrictions enforcement for a site using its configured mode and lists.

## SYNTAX

```powershell
Enable-SPOSiteRestrictedAppAccessControl -Identity <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Enable-SPOSiteRestrictedAppAccessControl` cmdlet to turn on Application Restrictions enforcement for a single site. A mode must already be configured with `Set-SPOSiteRestrictedAppAccessControlMode`; the cmdlet fails when no mode is set.

Site enforcement is turned on only by this cmdlet. Configuration and enablement are independent: mode and list changes never turn enforcement on. An administrator can stage a policy with `Set-SPOSiteRestrictedAppAccessControlMode` and `Set-SPOSiteRestrictedAppAccessControlList` and then enable it explicitly.

The active mode determines the site policy decision:

- **Allow** - applications in the allow list pass the Application Restrictions check, and all other governed applications are denied by the site policy. An empty active allow list causes the site policy to deny all governed third-party and agentic applications.
- **Deny** - applications in the deny list are denied by the site policy, and all other governed applications pass the Application Restrictions check.

The inactive list is preserved and has no runtime effect.

The tenant switch gates all site enforcement. A site policy has no effect while the tenant switch is off, and the tenant deny list can't be overridden by a site allow list. Use `Get-SPOTenantRestrictedAppAccessControl` to confirm the tenant switch before you rely on a site policy.

Application Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Microsoft Entra consent. A request must pass both the existing permission model and Application Restrictions.

Site Application Restrictions administration is isolated from the general-purpose `Get-SPOSite` and `Set-SPOSite` cmdlets. Application Restrictions is fully decoupled from `SiteProperties`, so `Get-SPOSite` doesn't load site policy data and `Set-SPOSite` can't change it. Use the dedicated Application Restrictions cmdlets listed in [Related Links](#related-links).

Microsoft first-party and core applications are excluded from Application Restrictions configuration and enforcement.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Enable-SPOSiteRestrictedAppAccessControl -Identity "https://contoso.sharepoint.com/sites/Finance"
```

This example turns on Application Restrictions enforcement for the Finance site identified by its URL. Enforcement uses the mode and lists that are already configured on the site.

### Example 2

```powershell
Enable-SPOSiteRestrictedAppAccessControl -Identity "e1b2c3d4-5678-4abc-9def-0123456789ab"
```

This example turns on enforcement for a site identified by its ID. Every site Application Restrictions cmdlet accepts `-Identity` as either a site URL or a site ID.

### Example 3

```powershell
$url = "https://contoso.sharepoint.com/sites/Finance"
Set-SPOSiteRestrictedAppAccessControlMode -Identity $url -Mode Allow
Set-SPOSiteRestrictedAppAccessControlList -Identity $url -ListType AllowList -AddRestrictedAppIds "11111111-1111-1111-1111-111111111111"
Enable-SPOSiteRestrictedAppAccessControl -Identity $url
```

This example configures a mode and allow list and then enables the policy explicitly. The mode and list changes don't turn enforcement on, so nothing is enforced until the final command runs. Applications in the allow list pass the Application Restrictions check; all other governed applications are denied by the site policy. Existing Microsoft Entra consent and SharePoint authorization still apply.

### Example 4

```powershell
Enable-SPOSiteRestrictedAppAccessControl -Identity "https://contoso.sharepoint.com/sites/Finance" -Confirm:$false
```

This example turns on enforcement without an interactive confirmation prompt, for use in automation. Using `-Confirm:$false` doesn't bypass validation, authorization, auditing, or first-party protection.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the site to enable. Provide either the site URL or the site ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

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

### None

## OUTPUTS

### None

This cmdlet doesn't return an object. Use `Get-SPOSiteRestrictedAppAccessControl` to read the resulting policy.

## NOTES

- This cmdlet fails when no mode is configured on the site. Set the mode to `Allow` or `Deny` before enabling the policy.
- Site enforcement is turned on only by this cmdlet. Mode and list changes preserve the current enablement state.
- An empty active allow list causes the site policy to deny all governed third-party and agentic applications. Review the active list with `Get-SPOSiteRestrictedAppAccessControl` before you enable a site.
- In `Deny` mode, applications represented in the deny list are denied by the site policy. All other governed applications pass the Application Restrictions check.
- The tenant switch gates all site enforcement, so a site policy has no effect while the tenant switch is off. The tenant deny list can't be overridden by a site allow list.
- Application Restrictions never grants permissions. A request must still pass existing SharePoint authorization.
- This cmdlet supports `-WhatIf` and `-Confirm` with `ConfirmImpact.High`. `-Confirm:$false` is allowed for automation and doesn't bypass validation, authorization, auditing, or first-party protection.

## RELATED LINKS

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Set-SPOSiteRestrictedAppAccessControlMode](Set-SPOSiteRestrictedAppAccessControlMode.md)

[Set-SPOSiteRestrictedAppAccessControlList](Set-SPOSiteRestrictedAppAccessControlList.md)

[Disable-SPOSiteRestrictedAppAccessControl](Disable-SPOSiteRestrictedAppAccessControl.md)

[Clear-SPOSiteRestrictedAppAccessControlList](Clear-SPOSiteRestrictedAppAccessControlList.md)

[Clear-SPOSiteRestrictedAppAccessControlPolicy](Clear-SPOSiteRestrictedAppAccessControlPolicy.md)

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
