---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/disable-spositerestrictedappaccesscontrol
applicable: SharePoint Online
title: Disable-SPOSiteRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Learn how to use Disable-SPOSiteRestrictedAppAccessControl in SharePoint Online PowerShell to pause site-level app access enforcement without losing saved settings.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Disable-SPOSiteRestrictedAppAccessControl

## SYNOPSIS

Turns off App Restrictions enforcement for a site while preserving the site's active mode and both lists.

## SYNTAX

```
Disable-SPOSiteRestrictedAppAccessControl -Identity <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Disable-SPOSiteRestrictedAppAccessControl` cmdlet to turn off App Restrictions enforcement for a single site. The cmdlet disables enforcement while preserving the active mode and both lists. A stored site policy with enforcement disabled keeps its active mode and both lists staged and preserved, so you can re-enable the same configuration later with `Enable-SPOSiteRestrictedAppAccessControl`.

Disabling a site is different from clearing it. To remove the mode and both lists and clear the stored site policy entirely, use `Clear-SPOSiteRestrictedAppAccessControlPolicy`.

Configuration and enablement are orthogonal. Mode and list changes never turn enforcement on, so after you disable a site you can continue to stage changes with `Set-SPOSiteRestrictedAppAccessControlMode` and `Set-SPOSiteRestrictedAppAccessControlList` without reactivating enforcement. Site enforcement is turned on only by `Enable-SPOSiteRestrictedAppAccessControl`.

While the site is disabled, no site-level App Restrictions decision applies to requests for that site. Tenant-level policy is unaffected: the tenant switch gates all site enforcement, and the tenant deny list can't be overridden by a site allow list.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions, so disabling a site policy doesn't grant any application access it doesn't already have.

App Restrictions for Apps administration is isolated from the general-purpose `Get-SPOSite` and `Set-SPOSite` cmdlets. App Restrictions is fully decoupled from `SiteProperties`, so `Get-SPOSite` doesn't load site policy data and `Set-SPOSite` can't change it. Use the dedicated App Restrictions cmdlets listed in [Related Links](#related-links).

You must be at least a SharePoint Administrator or to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Disable-SPOSiteRestrictedAppAccessControl -Identity "https://contoso.sharepoint.com/sites/Finance"
```

This example turns off App Restrictions enforcement for the Finance site. The site's active mode, allow list, and deny list are preserved.

### Example 2

```powershell
Disable-SPOSiteRestrictedAppAccessControl -Identity "e1b2c3d4-5678-4abc-9def-0123456789ab" -WhatIf
```

This example uses a site ID and shows what would happen without changing the policy. Every site App Restrictions cmdlet accepts `-Identity` as either a site URL or a site ID.

### Example 3

```powershell
$url = "https://contoso.sharepoint.com/sites/Finance"
Disable-SPOSiteRestrictedAppAccessControl -Identity $url -Confirm:$false
Get-SPOSiteRestrictedAppAccessControl -Identity $url
```

This example disables enforcement without an interactive prompt and then reads the policy back to confirm that the mode and both lists are still stored. Using `-Confirm:$false` doesn't bypass validation, authorization, auditing, or first-party protection.

## PARAMETERS

### -Identity

Specifies the site to disable. Provide either the site URL or the site ID.

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

This cmdlet doesn't return an object. Use `Get-SPOSiteRestrictedAppAccessControl` to read the resulting policy.

## NOTES

- Disabling preserves the active mode and both lists. Use `Clear-SPOSiteRestrictedAppAccessControlPolicy` to remove the mode and lists and clear the stored site policy.
- Site enforcement is turned on again only by `Enable-SPOSiteRestrictedAppAccessControl`. Mode and list changes never turn enforcement on.
- The tenant switch gates all site enforcement, so a site policy has no effect while the tenant switch is off. The tenant deny list can't be overridden by a site allow list.
- App Restrictions never grants permissions. A request must still pass existing SharePoint authorization.
- This cmdlet supports `-WhatIf` and `-Confirm` with `ConfirmImpact.High`. `-Confirm:$false` is allowed for automation and doesn't bypass validation, authorization, auditing, or first-party protection.
- [Add the exact warning and error text emitted by the cmdlet.]

## RELATED LINKS

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Set-SPOSiteRestrictedAppAccessControlMode](Set-SPOSiteRestrictedAppAccessControlMode.md)

[Set-SPOSiteRestrictedAppAccessControlList](Set-SPOSiteRestrictedAppAccessControlList.md)

[Enable-SPOSiteRestrictedAppAccessControl](Enable-SPOSiteRestrictedAppAccessControl.md)

[Clear-SPOSiteRestrictedAppAccessControlList](Clear-SPOSiteRestrictedAppAccessControlList.md)

[Clear-SPOSiteRestrictedAppAccessControlPolicy](Clear-SPOSiteRestrictedAppAccessControlPolicy.md)

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
