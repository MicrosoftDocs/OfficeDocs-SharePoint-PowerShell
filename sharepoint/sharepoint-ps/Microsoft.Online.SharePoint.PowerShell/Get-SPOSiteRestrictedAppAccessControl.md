---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositerestrictedappaccesscontrol
applicable: SharePoint Online
title: Get-SPOSiteRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Learn how to use Get-SPOSiteRestrictedAppAccessControl to read a SharePoint site's App Restrictions policy and check enforcement status with PowerShell.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Get-SPOSiteRestrictedAppAccessControl

## SYNOPSIS

Returns the complete site-level App Restrictions policy for a site, including enablement, active mode, and both the allow list and the deny list.

## SYNTAX

```
Get-SPOSiteRestrictedAppAccessControl [-Identity] <String> [<CommonParameters>]
```

## DESCRIPTION

Use the `Get-SPOSiteRestrictedAppAccessControl` cmdlet to read the complete Restricted App Access Control policy stored for a single site.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions.

A site policy has four parts:

- **Enabled** - whether site enforcement is turned on. Site enforcement is turned on only by `Enable-SPOSiteRestrictedAppAccessControl`. Mode and list changes are configuration-only and preserve the current enablement state.
- **Mode** - the active mode. When the mode is `Allow`, applications in the allow list are allowed and all other governed apps are denied. When the mode is `Deny`, applications in the deny list are denied and all other governed apps are allowed. `Allow` is the default mode when a site is enabled without existing configuration.
- **AllowList** - the persistent list used when the mode is `Allow`.
- **DenyList** - the persistent list used when the mode is `Deny`.

Both lists are always stored and can be managed regardless of which mode is active. Only the list selected by the active mode participates in runtime enforcement. The inactive list is preserved for future mode changes and has no runtime effect. An empty active allow list blocks all governed third-party and agentic apps. An empty active deny list allows all governed apps.

`AllowList` and `DenyList` are returned as GUID arrays. Each list can contain both concrete application IDs and parent agent blueprint IDs, and a blueprint ID applies to the blueprint application itself and to every current or future agent app created from that blueprint. The cmdlet doesn't require you to distinguish between the two: each property merges its internally typed application and blueprint entries into one stable, duplicate-free list of GUIDs.

This cmdlet performs an uncached read and always returns the authoritative stored policy rather than a cached copy.

Site enforcement is gated by the tenant switch. While the tenant switch is off, no site policy is enforced, even when a site policy reports `Enabled` as `True`. While the tenant switch is on, the tenant deny list takes precedence and can't be overridden by a site allow list. Use `Get-SPOTenantRestrictedAppAccessControl` to read the tenant switch and the tenant deny list.

Site App Restrictions administration is isolated from the general-purpose `Get-SPOSite` and `Set-SPOSite` cmdlets. App Restrictions is fully decoupled from site properties, so `Get-SPOSite` doesn't load site policy data and `Set-SPOSite` can't change it. Use the dedicated App Restrictions cmdlets listed in [Related Links](#related-links).

You must be at least a SharePoint Administrator to run this cmdlet.
Microsoft first-party and core applications are excluded from App Restrictions configuration and enforcement and never appear in a site list.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```
Get-SPOSiteRestrictedAppAccessControl -Identity https://contoso.sharepoint.com/sites/Finance
```

This example returns the complete Restricted App Access Control policy for the Finance site, bound by site URL.

### Example 2

```
Get-SPOSiteRestrictedAppAccessControl -Identity 8a1e30f6-2f52-4b9e-9d1b-2e9f6c1d40aa
```

This example returns the same policy for a site bound by site ID. The returned object carries `SiteUrl`, so it identifies its own site even when you don't know the URL.

### Example 3

```
$policy = Get-SPOSiteRestrictedAppAccessControl -Identity https://contoso.sharepoint.com/sites/Finance
if ($policy.Mode -eq "Allow") {
    $policy.AllowList
} else {
    $policy.DenyList
}
```

This example returns only the list that the active mode enforces. The other list is still stored and preserved, but it has no runtime effect until you change the mode.

### Example 4

```
$policy = Get-SPOSiteRestrictedAppAccessControl -Identity https://contoso.sharepoint.com/sites/Finance
if ($policy.Enabled -and $policy.Mode -eq "Allow" -and $policy.AllowList.Count -eq 0) {
    Write-Host "Enforcement is on with an empty active allow list, which blocks all governed third-party and agentic apps."
}
```

This example identifies the state where enforcement is enabled, the active mode is `Allow`, and the active allow list is empty. In that state, all governed third-party and agentic apps are blocked from the site while the tenant switch is on.

## PARAMETERS

### -Identity

Specifies the site to read. You can specify either the site URL or the site ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 0
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### SPORestrictedAppAccessControlSitePolicy

Returns an `SPORestrictedAppAccessControlSitePolicy` object with the following properties.

| Property | Type | Description |
|---|---|---|
| `SiteUrl` | String | The URL of the site the policy belongs to. This property is carried so the returned object identifies its own site, which matters when sites are piped into the cmdlet and when you bound the site by ID. |
| `Enabled` | Boolean | Indicates whether site enforcement is turned on. Site enforcement is also gated by the tenant switch. |
| `Mode` | String | The active mode, `Allow` or `Deny`. Only the list selected by this mode is enforced. |
| `AllowList` | Guid[] | The persistent allow list, returned as one stable, duplicate-free list of application IDs and parent agent blueprint IDs. |
| `DenyList` | Guid[] | The persistent deny list, returned as one stable, duplicate-free list of application IDs and parent agent blueprint IDs. |

When the stored policy data is malformed, the cmdlet emits a warning and the returned object includes `IsPolicyDataMalformed = true`. Healthy output omits that property.

## NOTES

- Getters return authoritative uncached state.
- Both lists are always stored. Only the list selected by the active mode is enforced; the inactive list is preserved and has no runtime effect.
- Each list has a hard maximum of 100 entries, and the two lists combined have a hard maximum of 200 entries.
- A parent agent blueprint ID entry applies to the blueprint application itself and to every current or future agent app created from that blueprint.
- The tenant switch gates all site enforcement. While the tenant switch is on, the tenant deny list can't be overridden by a site allow list.
- Configuration and enablement are orthogonal: mode and list changes never turn enforcement on. The only combination the backend rejects is enabled with mode `None`.
- Use `Get-SPOTenantRestrictedAppAccessControl` to read the tenant-level policy.

## RELATED LINKS

[Set-SPOSiteRestrictedAppAccessControlMode](Set-SPOSiteRestrictedAppAccessControlMode.md)

[Set-SPOSiteRestrictedAppAccessControlList](Set-SPOSiteRestrictedAppAccessControlList.md)

[Enable-SPOSiteRestrictedAppAccessControl](Enable-SPOSiteRestrictedAppAccessControl.md)

[Disable-SPOSiteRestrictedAppAccessControl](Disable-SPOSiteRestrictedAppAccessControl.md)

[Clear-SPOSiteRestrictedAppAccessControlList](Clear-SPOSiteRestrictedAppAccessControlList.md)

[Clear-SPOSiteRestrictedAppAccessControlPolicy](Clear-SPOSiteRestrictedAppAccessControlPolicy.md)

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
