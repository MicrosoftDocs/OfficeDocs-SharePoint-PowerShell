---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenantrestrictedappaccesscontrol
applicable: SharePoint Online
title: Get-SPOTenantRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Get-SPOTenantRestrictedAppAccessControl retrieves the tenant Application Restrictions enforcement status and deny list.
ms.date: 10/13/2026
ms.topic: reference
---

# Get-SPOTenantRestrictedAppAccessControl

## SYNOPSIS

Returns the tenant-level Application Restrictions policy, including the tenant enforcement switch and the tenant-wide deny list of restricted application IDs.

## SYNTAX

```powershell
Get-SPOTenantRestrictedAppAccessControl [<CommonParameters>]
```

## DESCRIPTION

Use the `Get-SPOTenantRestrictedAppAccessControl` cmdlet to read the complete tenant Application Restrictions policy for your organization.

Application Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and Application Restrictions.

The tenant policy has two parts:

- **Enabled** - the master enforcement switch for Application Restrictions. When this switch is off, the tenant deny list and all site-level policies aren't enforced. Stored tenant and site configuration is preserved. When the switch is turned on again, the tenant deny list and site policies whose site-level `Enabled` flag is `True` resume enforcement with the same configuration.
- **RestrictedAppIds** - the tenant-wide deny list. When the switch is on, applications in this list are denied and the list can't be overridden by a site-level allow list.

The tenant deny list can contain both concrete application IDs and parent agent blueprint IDs. A blueprint ID applies to the blueprint application itself and to every current or future agent app created from that blueprint. The cmdlet doesn't require you to distinguish between the two: `RestrictedAppIds` merges the internally typed entries into one stable, duplicate-free `Guid[]`.

This cmdlet returns the authoritative, uncached policy state.

Tenant Application Restrictions administration is isolated from the general-purpose `Get-SPOTenant` and `Set-SPOTenant` cmdlets. Application Restrictions isn't exposed as a `Tenant` property, so `Get-SPOTenant` doesn't return the policy and `Set-SPOTenant` can't change it. Use the dedicated Application Restrictions cmdlets listed in [Related Links](#related-links).

Microsoft first-party and core applications are excluded from Application Restrictions configuration and enforcement and never appear in the tenant deny list.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Get-SPOTenantRestrictedAppAccessControl
```

This example returns the complete tenant Application Restrictions policy, showing whether enforcement is enabled and which application IDs are on the tenant deny list.

### Example 2

```powershell
(Get-SPOTenantRestrictedAppAccessControl).RestrictedAppIds
```

This example returns only the restricted application IDs from the tenant deny list.

### Example 3

```powershell
$policy = Get-SPOTenantRestrictedAppAccessControl
if (-not $policy.Enabled) {
    Write-Host "Application Restrictions enforcement is off. Site policies aren't enforced."
}
```

This example stores the tenant policy in a variable and checks the master switch. Because the tenant switch gates all site-level enforcement, a disabled switch means no site policy is being enforced, including policies whose site-level `Enabled` flag is `True`.

### Example 4

```powershell
$policy = Get-SPOTenantRestrictedAppAccessControl
if ($policy.Enabled -and $policy.RestrictedAppIds.Count -eq 0) {
    Write-Host "Enforcement is on, but the tenant deny list is empty and denies nothing."
}
```

This example identifies an enabled tenant switch with an empty tenant deny list. This state is valid. The tenant deny list denies nothing until an application ID is added; site policies whose site-level `Enabled` flag is `True` can still enforce.

## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### SPORestrictedAppAccessControlTenantPolicy

Returns an `SPORestrictedAppAccessControlTenantPolicy` object with the following properties.

| Property | Type | Description |
|---|---|---|
| `Enabled` | Boolean | Indicates whether the tenant Application Restrictions enforcement switch is on. When `False`, the tenant deny list and all site-level policies aren't enforced. |
| `RestrictedAppIds` | Guid[] | The tenant-wide deny list, returned as one stable, duplicate-free list of application IDs and parent agent blueprint IDs. |

## NOTES

- The tenant switch is the master enforcement switch for Application Restrictions. Turning it off stops enforcement for every site policy whose site-level `Enabled` flag is `True`, not only the tenant deny list.
- While the tenant switch is on, the tenant deny list takes precedence over site policy and can't be overridden by a site allow list.
- The tenant scope is deny-only and has a single list, so there's no mode and no list-type selection at tenant scope.
- The tenant deny list has a hard maximum of 100 application IDs.
- Configuration and enablement are independent: changing the deny list never turns the tenant switch on or off.
- Use `Get-SPOSiteRestrictedAppAccessControl` to read the policy for an individual site.

## RELATED LINKS

[Enable-SPOTenantRestrictedAppAccessControl](Enable-SPOTenantRestrictedAppAccessControl.md)

[Disable-SPOTenantRestrictedAppAccessControl](Disable-SPOTenantRestrictedAppAccessControl.md)

[Set-SPOTenantRestrictedAppAccessControlList](Set-SPOTenantRestrictedAppAccessControlList.md)

[Clear-SPOTenantRestrictedAppAccessControlPolicy](Clear-SPOTenantRestrictedAppAccessControlPolicy.md)

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
