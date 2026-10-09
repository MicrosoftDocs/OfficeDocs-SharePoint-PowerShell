---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/clear-spositerestrictedappaccesscontrolpolicy
applicable: SharePoint Online
title: Clear-SPOSiteRestrictedAppAccessControlPolicy
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Clear-SPOSiteRestrictedAppAccessControlPolicy removes a site's App Restrictions policy, disabling enforcement and clearing lists. Learn syntax and examples.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Clear-SPOSiteRestrictedAppAccessControlPolicy

## SYNOPSIS

Removes the complete app restrictions policy from a site. The cmdlet disables enforcement, and removes the active mode and both lists.

## SYNTAX

```
Clear-SPOSiteRestrictedAppAccessControlPolicy -Identity <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Clear-SPOSiteRestrictedAppAccessControlPolicy` cmdlet to return a site to its unconfigured state. The cmdlet disables enforcement, removes the active mode and both lists, and clears the stored site policy. After the policy is cleared, the site is in the same state as a site that was never configured: enforcement is disabled and there are no entries.

Clearing is different from disabling. `Disable-SPOSiteRestrictedAppAccessControl` turns off enforcement but preserves the active mode and both lists so the same configuration can be re-enabled later. Use `Clear-SPOSiteRestrictedAppAccessControlPolicy` when you want the configuration removed as well. To clear only one list and keep the other list, the mode, and site enablement, use `Clear-SPOSiteRestrictedAppAccessControlList`.

Because the mode is removed along with the lists, a cleared site can't be enabled again until a mode is set. `Enable-SPOSiteRestrictedAppAccessControl` fails when no mode is set; enabled with mode `None` is the only combination the backend rejects. Rebuild the policy with `Set-SPOSiteRestrictedAppAccessControlMode` and `Set-SPOSiteRestrictedAppAccessControlList`, then enable it explicitly. Configuration and enablement are orthogonal: mode and list changes never turn enforcement on, so an administrator can stage a policy and then enable it. This avoids the dangerous case where adding a single ID to an unconfigured site would immediately activate an allow list and block every other application.

Clearing a site policy affects only that site. The tenant switch gates all site enforcement, and the tenant deny list can't be overridden by a site allow list, so clearing a site policy never restores access for an application that the tenant denies. Use `Clear-SPOTenantRestrictedAppAccessControlPolicy` for the tenant scope.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions, so clearing a site policy doesn't grant any application access it doesn't already have.

Site App Restrictions administration is isolated from the general-purpose `Get-SPOSite` and `Set-SPOSite` cmdlets. App Restrictions is fully decoupled from `SiteProperties`, so `Get-SPOSite` doesn't load site policy data and `Set-SPOSite` can't change it. Use the dedicated App Restrictions cmdlets listed in [Related Links](#related-links).

You must be at least a SharePoint Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```
Clear-SPOSiteRestrictedAppAccessControlPolicy -Identity "https://contoso.sharepoint.com/sites/Finance"
```

This example removes the complete App Restrictions policy from the Finance site. It disables enforcement and removes the active mode, allow list, and deny list.

### Example 2

```
Clear-SPOSiteRestrictedAppAccessControlPolicy -Identity "e1b2c3d4-5678-4abc-9def-0123456789ab" -WhatIf
```

This example identifies the site by site ID and previews the change without modifying the policy. Every site App Restrictions cmdlet accepts `-Identity` as either a site URL or a site ID.

### Example 3

```
$url = "https://contoso.sharepoint.com/sites/Finance"
Clear-SPOSiteRestrictedAppAccessControlPolicy -Identity $url -Confirm:$false
Set-SPOSiteRestrictedAppAccessControlMode -Identity $url -Mode Deny
Set-SPOSiteRestrictedAppAccessControlList -Identity $url -ListType DenyList -AddRestrictedAppIds "11111111-1111-1111-1111-111111111111"
Enable-SPOSiteRestrictedAppAccessControl -Identity $url
```

This example removes an existing policy and then rebuilds it from scratch. Because the mode is removed when the policy is cleared, you must assign a mode to the site before you can enable it.

## PARAMETERS

### -Identity

Specifies the site whose policy is cleared. Provide either the site URL or the site ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet. This cmdlet uses `ConfirmImpact.High`, so it prompts by default. Use `-Confirm:$false` to suppress the prompt in automation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### None

This cmdlet doesn't return an object. Use `Get-SPOSiteRestrictedAppAccessControl` to confirm that the site is unconfigured.

## NOTES

- Clearing a site policy disables enforcement, removes the active mode and both lists, and clears the stored site policy. A cleared site is indistinguishable from a site that was never configured.
- To keep the configuration for later use, use `Disable-SPOSiteRestrictedAppAccessControl` instead. It preserves the active mode and both lists.
- To clear only one list, use `Clear-SPOSiteRestrictedAppAccessControlList`, which preserves the other list, the active mode, and site enablement.
- After clearing, the site can't be enabled until a mode is set. `Enable-SPOSiteRestrictedAppAccessControl` fails when no mode is set.
- The tenant switch gates all site enforcement, so a site policy has no effect while the tenant switch is off. The tenant deny list can't be overridden by a site allow list.
- App Restrictions never grants permissions. A request must still pass existing SharePoint authorization.
- This cmdlet supports `-WhatIf` and `-Confirm` with `ConfirmImpact.High`. `-Confirm:$false` is allowed for automation and doesn't bypass validation, authorization, auditing, or first-party protection.
- [Add the exact warning and error text emitted by the cmdlet.]

## Related links

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Set-SPOSiteRestrictedAppAccessControlMode](Set-SPOSiteRestrictedAppAccessControlMode.md)

[Set-SPOSiteRestrictedAppAccessControlList](Set-SPOSiteRestrictedAppAccessControlList.md)

[Enable-SPOSiteRestrictedAppAccessControl](Enable-SPOSiteRestrictedAppAccessControl.md)

[Disable-SPOSiteRestrictedAppAccessControl](Disable-SPOSiteRestrictedAppAccessControl.md)

[Clear-SPOSiteRestrictedAppAccessControlList](Clear-SPOSiteRestrictedAppAccessControlList.md)

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
