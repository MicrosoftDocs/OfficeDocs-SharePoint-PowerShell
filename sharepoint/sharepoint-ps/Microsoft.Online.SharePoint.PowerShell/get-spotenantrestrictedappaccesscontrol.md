---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenantrestrictedappaccesscontrol
applicable: SharePoint Online
title: Get-SPOTenantRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: [ Add reviewer alias ]
description: Get-SPOTenantRestrictedAppAccessControl retrieves your tenant's App Restrictionsolicy, including enforcement status and the deny list. Learn how.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Get-SPOTenantRestrictedAppAccessControl

## SYNOPSIS

Returns the tenant-level App Restrictions policy, including the tenant enforcement switch and the tenant-wide deny list of restricted application IDs.

## SYNTAX

```powershell
Get-SPOTenantRestrictedAppAccessControl [<CommonParameters>]
```

## DESCRIPTION

Use the `Get-SPOTenantRestrictedAppAccessControl` cmdlet to read the complete tenant Restricted App Access Control policy for your organization.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions.

The tenant policy has two parts:

- **Enabled** - the master enforcement switch for App Restrictions. When this switch is off, no RAC for Apps policy is enforced, including the tenant deny list and any site-level policies. Stored tenant and site configuration is preserved, so enforcement resumes with the same configuration when the switch is turned on again.
- **RestrictedAppIds** - the tenant-wide emergency deny list. When the switch is on, applications in this list are denied and the list can't be overridden by a site-level allow list.

The tenant deny list can contain both concrete application IDs and parent agent blueprint IDs. A blueprint ID applies to the blueprint application itself and to every current or future agent app created from that blueprint. The cmdlet doesn't require you to distinguish between the two: `RestrictedAppIds` merges the internally typed entries into one stable, duplicate-free list of GUIDs. IDs are stored as lowercase canonical GUID strings and sorted, so output is stable between calls.

This cmdlet performs an uncached read and always returns the authoritative, latest stored policy rather than a cached copy.

Tenant App Restrictions administration is isolated from the general-purpose `Get-SPOTenant` and `Set-SPOTenant` cmdlets. App Restrictions isn't exposed as a `Tenant` property, so `Get-SPOTenant` doesn't return the policy and `Set-SPOTenant` can't change it. Use the dedicated App Restrictions cmdlets listed in [Related Links](#related-links).

You must be at least a SharePoint Administrator to run this cmdlet.

Microsoft first-party and core applications are excluded from App Restrictions configuration and enforcement and never appear in the tenant deny list.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Get-SPOTenantRestrictedAppAccessControl
```

This example returns the complete tenant Restricted App Access Control policy, showing whether enforcement is enabled and which application IDs are on the tenant deny list.

### Example 2

```powershell
(Get-SPOTenantRestrictedAppAccessControl).RestrictedAppIds
```

This example returns only the restricted application IDs from the tenant deny list.

### Example 3

```powershell
$policy = Get-SPOTenantRestrictedAppAccessControl
if (-not $policy.Enabled) {
    Write-Host "App Restrictions enforcement is off. Site policies aren't enforced."
}
```

This example stores the tenant policy in a variable and checks the master switch. Because the tenant switch gates all site-level enforcement, a disabled switch means no configured site policy is being enforced.

### Example 4

```powershell
$policy = Get-SPOTenantRestrictedAppAccessControl
if ($policy.Enabled -and $policy.RestrictedAppIds.Count -eq 0) {
    Write-Host "Enforcement is on, but the tenant deny list is empty and denies nothing."
}
```

This example identifies the state where enforcement is enabled but the tenant deny list is empty. This state is valid, and often occurs during cleanup, but the tenant deny list has no effect until an application ID is added.

## PARAMETERS

This cmdlet has no parameters.

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### SPORestrictedAppAccessControlTenantPolicy

Returns an `SPORestrictedAppAccessControlTenantPolicy` object with the following properties.

| Property | Type | Description |
|---|---|---|
| `Enabled` | Boolean | Indicates whether the tenant App Restrictions enforcement switch is on. When `False`, no App Restrictions policy is enforced, including the tenant deny list and all site policies. |
| `RestrictedAppIds` | Guid[] | The tenant-wide deny list, returned as one stable, duplicate-free list of application IDs and parent agent blueprint IDs. |

## NOTES

- The tenant switch is the master enforcement switch for the feature. Turning it off stops every configured site policy from enforcing, not just the tenant deny list.
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
