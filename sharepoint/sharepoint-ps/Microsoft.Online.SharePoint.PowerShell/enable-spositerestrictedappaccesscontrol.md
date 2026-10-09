---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/enable-spositerestrictedappaccesscontrol
applicable: SharePoint Online
title: Enable-SPOSiteRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: [ Add reviewer alias ]
description: Enable-SPOSiteRestrictedAppAccessControl turns on App Restrictions enforcement for a SharePoint site using its existing mode and lists. Learn syntax and examples.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Enable-SPOSiteRestrictedAppAccessControl

## SYNOPSIS

Turns on App Restrictions enforcement for a site, using the mode and lists that are already configured on that site.

## SYNTAX

```powershell
Enable-SPOSiteRestrictedAppAccessControl -Identity <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Enable-SPOSiteRestrictedAppAccessControl` cmdlet to turn on App Restrictions enforcement for a single site. The cmdlet enables enforcement using the mode and lists that are already configured on the site, and it fails when no mode is set. The only combination that the backend rejects is enabled with mode `None`.

Site enforcement is turned on only by this cmdlet. Configuration and enablement are orthogonal: mode and list changes never turn enforcement on, so an administrator can stage a policy with `Set-SPOSiteRestrictedAppAccessControlMode` and `Set-SPOSiteRestrictedAppAccessControlList` and then enable it explicitly. This avoids the dangerous case where adding a single ID to an unconfigured site would immediately activate an allow list and block every other application.

The active mode determines what enforcement does once the site is enabled:

- **Allow** - subjects in the allow list are allowed and all other governed apps are denied. `Allow` is the default mode when a site is enabled without existing configuration. An empty active allow list blocks all governed third-party and agentic apps.
- **Deny** - subjects in the deny list are denied and all other governed apps are allowed.

The inactive list is preserved and has no runtime effect.

The tenant switch gates all site enforcement. A site policy has no effect while the tenant switch is off, and the tenant deny list can't be overridden by a site allow list. Use `Get-SPOTenantRestrictedAppAccessControl` to confirm the tenant switch before you rely on a site policy.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions.

Site App Restrictions administration is isolated from the general-purpose `Get-SPOSite` and `Set-SPOSite` cmdlets. App Restrictions is fully decoupled from `SiteProperties`, so `Get-SPOSite` doesn't load site policy data and `Set-SPOSite` can't change it. Use the dedicated App Restrictions cmdlets listed in [Related Links](#related-links).

You must be at least a SharePoint Administrator to run this cmdlet. 
Microsoft first-party and core applications are excluded from App Restrictions configuration and enforcement.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Enable-SPOSiteRestrictedAppAccessControl -Identity "https://contoso.sharepoint.com/sites/Finance"
```

This example turns on App Restrictions enforcement for the Finance site by using its site URL. Enforcement uses the mode and lists that are already configured on the site.

### Example 2

```powershell
Enable-SPOSiteRestrictedAppAccessControl -Identity "e1b2c3d4-5678-4abc-9def-0123456789ab"
```

This example turns on enforcement for the same site by using its site ID. Every site App Restrictions cmdlet accepts `-Identity` as either a site URL or a site ID.

### Example 3

```powershell
$url = "https://contoso.sharepoint.com/sites/Finance"
Set-SPOSiteRestrictedAppAccessControlMode -Identity $url -Mode Allow
Set-SPOSiteRestrictedAppAccessControlList -Identity $url -ListType AllowList -AddRestrictedAppIds "11111111-1111-1111-1111-111111111111"
Enable-SPOSiteRestrictedAppAccessControl -Identity $url
```

This example stages a policy and then enables it explicitly. The mode and list changes are configuration-only and don't turn enforcement on, so nothing is enforced until the final command runs.

### Example 4

```powershell
Enable-SPOSiteRestrictedAppAccessControl -Identity "https://contoso.sharepoint.com/sites/Finance" -Confirm:$false
```

This example turns on enforcement without an interactive confirmation prompt, for use in automation. Using `-Confirm:$false` doesn't bypass validation, authorization, auditing, or first-party protection.

## PARAMETERS

### -Identity

Specifies the site to enable. Provide either the site URL or the site ID.

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

- This cmdlet fails when no mode is set on the site. Enabled with mode `None` is the only combination that the backend rejects.
- Site enforcement is turned on only by this cmdlet. Mode and list changes are configuration-only and preserve the current enablement state.
- An empty active allow list blocks all governed third-party and agentic apps. Review the active list with `Get-SPOSiteRestrictedAppAccessControl` before you enable a site.
- The tenant switch gates all site enforcement, so a site policy has no effect while the tenant switch is off. The tenant deny list can't be overridden by a site allow list.
- App Restrictions never grants permissions. A request must still pass existing SharePoint authorization.
- This cmdlet supports `-WhatIf` and `-Confirm` with `ConfirmImpact.High`. `-Confirm:$false` is allowed for automation and doesn't bypass validation, authorization, auditing, or first-party protection.
- [Add the exact warning and error text emitted by the cmdlet.]

## RELATED LINKS

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Set-SPOSiteRestrictedAppAccessControlMode](Set-SPOSiteRestrictedAppAccessControlMode.md)

[Set-SPOSiteRestrictedAppAccessControlList](Set-SPOSiteRestrictedAppAccessControlList.md)

[Disable-SPOSiteRestrictedAppAccessControl](Disable-SPOSiteRestrictedAppAccessControl.md)

[Clear-SPOSiteRestrictedAppAccessControlList](Clear-SPOSiteRestrictedAppAccessControlList.md)

[Clear-SPOSiteRestrictedAppAccessControlPolicy](Clear-SPOSiteRestrictedAppAccessControlPolicy.md)

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
