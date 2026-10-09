---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spotenantrestrictedappaccesscontrollist
applicable: SharePoint Online
title: Set-SPOTenantRestrictedAppAccessControlList
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Set-SPOTenantRestrictedAppAccessControlList lets you add or remove app IDs from the tenant deny list in one atomic update. Learn syntax and examples.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Set-SPOTenantRestrictedAppAccessControlList

## SYNOPSIS

Adds application IDs to and removes application IDs from the tenant-wide App Restrictions deny list in a single atomic update.

## SYNTAX

```powershell
Set-SPOTenantRestrictedAppAccessControlList [-AddRestrictedAppIds <Guid[]>]
 [-RemoveRestrictedAppIds <Guid[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Set-SPOTenantRestrictedAppAccessControlList` cmdlet to change the tenant-wide emergency deny list for Restricted App Access Control.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and RAC for Apps.

Both parameters are applied in one atomic update that preserves the tenant enforcement switch. At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, and the same ID can't appear in both parameters. Removals are applied before additions.

You supply application IDs only. You don't identify whether an ID is a regular application or a parent agent blueprint: the backend classifies each added ID and stores it in the appropriate internal list. A parent agent blueprint ID on the tenant deny list blocks the blueprint application itself and every current or future agent app created from that blueprint.

Added IDs are classified by using Microsoft Graph. Microsoft first-party and core applications and IDs that can't be classified are rejected, and a bulk add is all-or-none: if any supplied ID is rejected, no IDs are persisted. Removals don't use Microsoft Graph, so stale or deleted application IDs can always be removed.

The combined tenant deny list has a hard maximum of 100 application IDs.

Configuration and enablement are orthogonal: list changes never turn the tenant switch on or off. Use `Enable-SPOTenantRestrictedAppAccessControl` and `Disable-SPOTenantRestrictedAppAccessControl` to change enforcement.

Removing the last entry leaves an enabled switch with an empty deny list, which denies nothing. That state is allowed because it's legitimate during cleanup, but the cmdlet warns and points you to `Disable-SPOTenantRestrictedAppAccessControl` or `Clear-SPOTenantRestrictedAppAccessControlPolicy` for turning the feature off explicitly.

The tenant scope is deny-only and has a single list, so there's no mode cmdlet, no `-ListType` parameter, and no separate clear-list cmdlet.

Tenant App Restrictions administration is isolated from the general-purpose `Get-SPOTenant` and `Set-SPOTenant` cmdlets. App Restrictions isn't exposed as a `Tenant` property, so `Get-SPOTenant` doesn't return the policy and `Set-SPOTenant` can't change it.

You must be at least a SharePoint Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).

## EXAMPLES

### Example 1

```powershell
Set-SPOTenantRestrictedAppAccessControlList -AddRestrictedAppIds 11111111-1111-1111-1111-111111111111
```

This example adds one application ID to the tenant deny list. The backend classifies the ID and stores it as either a regular application or a parent agent blueprint. The tenant enforcement switch isn't changed.

### Example 2

```powershell
Set-SPOTenantRestrictedAppAccessControlList -AddRestrictedAppIds 11111111-1111-1111-1111-111111111111, 22222222-2222-2222-2222-222222222222 -RemoveRestrictedAppIds 33333333-3333-3333-3333-333333333333
```

This example adds two application IDs and removes a third in a single atomic update. The removal is applied before the additions. If either added ID is a first-party or core application, or can't be classified, the complete operation fails and nothing is persisted.

### Example 3

```powershell
Set-SPOTenantRestrictedAppAccessControlList -RemoveRestrictedAppIds 33333333-3333-3333-3333-333333333333 -Confirm:$false
```

This example removes an application ID without prompting for confirmation, which is useful in automation. Removals don't call Microsoft Graph, so an ID for a deleted or stale application can still be removed. Suppressing the prompt doesn't bypass validation, authorization, auditing, or first-party protection.

### Example 4

```powershell
Set-SPOTenantRestrictedAppAccessControlList -AddRestrictedAppIds 44444444-4444-4444-4444-444444444444 -WhatIf
```

This example shows what would happen if the application ID were added, without changing the stored tenant policy.

## PARAMETERS

### -AddRestrictedAppIds

Specifies the application IDs to add to the tenant deny list. Each supplied ID is classified by using Microsoft Graph and stored internally as either a regular application or a parent agent blueprint. First-party/core and unclassifiable IDs are rejected, and the add is all-or-none.

At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, and an ID can't appear in both parameters. The combined tenant deny list can't exceed 100 IDs.

```yaml
Type: Guid[]
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRestrictedAppIds

Specifies the application IDs to remove from the tenant deny list. Removals are applied before additions and don't use Microsoft Graph, so stale or deleted application IDs can always be removed.

At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, and an ID can't appear in both parameters.

```yaml
Type: Guid[]
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet. This cmdlet has a confirm impact of High, so it prompts by default. Automation can use `-Confirm:$false` to suppress the prompt. Suppressing the prompt doesn't bypass validation, authorization, auditing, or first-party protection.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: SharePoint Online
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

This cmdlet doesn't return an output object. Use `Get-SPOTenantRestrictedAppAccessControl` to read the resulting tenant policy.

## NOTES

- Adds and removes are applied as one atomic update. Removals are applied before additions.
- A bulk add is all-or-none. If any supplied ID is a first-party/core application or can't be classified, no IDs are persisted.
- The combined tenant deny list has a hard maximum of 100 application IDs.
- The administrator supplies IDs only. The backend classifies each added ID and stores it as either a regular application or a parent agent blueprint.
- A parent agent blueprint ID blocks the blueprint application and every current or future agent app created from it.
- Configuration and enablement are orthogonal: list changes never flip the tenant switch.
- Removing the last entry leaves an enabled switch with an empty deny list that denies nothing. The cmdlet warns and points to `Disable-SPOTenantRestrictedAppAccessControl` or `Clear-SPOTenantRestrictedAppAccessControlPolicy`.
- Use `Set-SPOSiteRestrictedAppAccessControlList` to change the lists for an individual site.

## RELATED LINKS

[Get-SPOTenantRestrictedAppAccessControl](/powershell/module/microsoft.online.sharepoint.powershell/Get-SPOTenantRestrictedAppAccessControl)

[Enable-SPOTenantRestrictedAppAccessControl](/powershell/module/microsoft.online.sharepoint.powershell/Enable-SPOTenantRestrictedAppAccessControl)

[Disable-SPOTenantRestrictedAppAccessControl](/powershell/module/microsoft.online.sharepoint.powershell/Disable-SPOTenantRestrictedAppAccessControl)

[Clear-SPOTenantRestrictedAppAccessControlPolicy](/powershell/module/microsoft.online.sharepoint.powershell/Clear-SPOTenantRestrictedAppAccessControlPolicy)

[Get-SPOSiteRestrictedAppAccessControl](/powershell/module/microsoft.online.sharepoint.powershell/Get-SPOSiteRestrictedAppAccessControl)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
