---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spositerestrictedappaccesscontrollist
applicable: SharePoint Online
title: Set-SPOSiteRestrictedAppAccessControlList
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Learn how to use Set-SPOSiteRestrictedAppAccessControlList to manage site-level allow and deny lists for App Restrictions in SharePoint Online.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Set-SPOSiteRestrictedAppAccessControlList

## SYNOPSIS

Adds application IDs to, or removes application IDs from, the allow list or the deny list of a site-level App Restrictions policy, in one atomic update.

## SYNTAX

```
Set-SPOSiteRestrictedAppAccessControlList [-Identity] <String> -ListType <String>
 [-AddRestrictedAppIds <Guid[]>] [-RemoveRestrictedAppIds <Guid[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use the `Set-SPOSiteRestrictedAppAccessControlList` cmdlet to change the contents of one site list. Additions and removals are applied in one atomic update that preserves site enablement and the active mode.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions.

Use `-ListType` to identify the target list explicitly. Both lists are always stored and can be managed regardless of which mode is active. Only the list selected by the active mode participates in runtime enforcement, so adding or removing entries in the inactive list doesn't change current enforcement. The inactive list is preserved for future mode changes.

The active mode determines what the change means at runtime. When the mode is `Allow`, applications in the allow list are allowed and all other governed apps are denied; an empty active allow list blocks all governed third-party and agentic apps. When the mode is `Deny`, applications in the deny list are denied and all other governed apps are allowed; an empty active deny list allows all governed apps.

At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, an ID can't appear in both, and removals are applied before additions.

You supply application IDs only. Each list can contain both concrete application IDs and parent agent blueprint IDs, and the backend classifies each added ID and stores its type internally. A parent agent blueprint ID applies to the blueprint application itself and to every current or future agent app created from that blueprint. In an active deny list, a blueprint ID blocks that complete app family. In an active allow list, it allows that complete app family through App Restrictions.

Adding IDs uses the same bulk Microsoft Graph classification and first-party exclusion as the tenant cmdlets. Microsoft first-party and core applications are rejected, IDs that can't be classified are rejected, and a bulk add is all-or-none, so no partial set of IDs is persisted.

Removing entries requires only `-ListType` and `-RemoveRestrictedAppIds`. Removal doesn't call Microsoft Graph, so deleted or stale application IDs can still be removed. If a supplied ID isn't present in the target list, the cmdlet returns a validation error.

Configuration and enablement are orthogonal: a list change never turns enforcement on. Site enforcement is turned on only by `Enable-SPOSiteRestrictedAppAccessControl`, so you can stage lists and then enable the site explicitly. This avoids the dangerous case where adding a single ID to an unconfigured site would immediately activate an allow list and block every other application. The only combination the backend rejects is enabled with mode `None`.

Site enforcement is also gated by the tenant switch. While the tenant switch is on, the tenant deny list takes precedence and can't be overridden by a site allow list.

Automation can use the standard `-Confirm:$false`. Suppressing the prompt doesn't bypass validation, authorization, auditing, or first-party protection.

Site App Restrictions administration is isolated from the general-purpose `Get-SPOSite` and `Set-SPOSite` cmdlets. `Get-SPOSite` doesn't load site policy data and `Set-SPOSite` can't change it. Use the dedicated App Restrictions cmdlets listed in [Related Links](#related-links).

You must be at least a SharePoint Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```
Set-SPOSiteRestrictedAppAccessControlList -Identity https://contoso.sharepoint.com/sites/Finance -ListType AllowList -AddRestrictedAppIds 11111111-1111-1111-1111-111111111111
```

This example adds one application ID to the allow list of the Finance site. The site's enablement and active mode are preserved. If the ID is a Microsoft first-party or core application, or if it can't be classified, the add is rejected.

### Example 2

```
Set-SPOSiteRestrictedAppAccessControlList -Identity https://contoso.sharepoint.com/sites/Finance -ListType DenyList -AddRestrictedAppIds 22222222-2222-2222-2222-222222222222,33333333-3333-3333-3333-333333333333 -RemoveRestrictedAppIds 44444444-4444-4444-4444-444444444444
```

This example adds two IDs to the deny list and removes one ID from the deny list in a single atomic update. Removals are applied before additions, and the bulk add is all-or-none.

### Example 3

```
Set-SPOSiteRestrictedAppAccessControlList -Identity 8a1e30f6-2f52-4b9e-9d1b-2e9f6c1d40aa -ListType AllowList -RemoveRestrictedAppIds 55555555-5555-5555-5555-555555555555 -Confirm:$false
```

This example removes a stale application ID from the allow list of a site bound by site ID, without prompting. Removal doesn't call Microsoft Graph, so IDs for deleted applications can still be removed. If the ID isn't present in the list, the cmdlet returns a validation error.

### Example 4

```
Set-SPOSiteRestrictedAppAccessControlList -Identity https://contoso.sharepoint.com/sites/Finance -ListType DenyList -AddRestrictedAppIds 66666666-6666-6666-6666-666666666666 -WhatIf
```

This example shows what would change without modifying the policy. Adding a parent agent blueprint ID to a deny list blocks the blueprint application and every current or future agent app created from it.

## PARAMETERS

### -Identity

Specifies the site to configure. You can specify either the site URL or the site ID.

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

### -ListType

Specifies the list to change. Valid values are `AllowList` and `DenyList`. Entry mutations must explicitly identify the target list.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Accepted values: AllowList, DenyList
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRestrictedAppIds

Specifies the application IDs to add to the list identified by `-ListType`. You supply application IDs only; the backend classifies each added ID as a regular application or a parent agent blueprint and stores the type internally.

Adds use the shared bulk Microsoft Graph classification. First-party or core applications and unclassifiable IDs are rejected, and a bulk add is all-or-none.

At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, and an ID can't appear in both.

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

Specifies the application IDs to remove from the list identified by `-ListType`. Removals are applied before additions.

Removing entries doesn't call Microsoft Graph, so deleted or stale application IDs can still be removed. If a supplied ID isn't present in the target list, the cmdlet returns a validation error.

At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, and an ID can't appear in both.

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

### System.String

## OUTPUTS

### None

## NOTES

- Additions and removals are applied in one atomic update that preserves site enablement and the active mode.
- At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, an ID can't appear in both, and removals are applied before additions.
- Each list has a hard maximum of 100 entries, and the two lists combined have a hard maximum of 200 entries. Both regular application IDs and parent agent blueprint IDs consume the same quota.
- Adding or removing entries in the list that the active mode doesn't enforce doesn't change current enforcement.
- Configuration and enablement are orthogonal. Site enforcement is turned on only by `Enable-SPOSiteRestrictedAppAccessControl`. The only combination the backend rejects is enabled with mode `None`.
- The tenant switch gates all site enforcement. While the tenant switch is on, the tenant deny list can't be overridden by a site allow list.
- Use `Get-SPOSiteRestrictedAppAccessControl` to confirm the resulting lists, and `Clear-SPOSiteRestrictedAppAccessControlList` to clear an entire list.

## RELATED LINKS

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Set-SPOSiteRestrictedAppAccessControlMode](Set-SPOSiteRestrictedAppAccessControlMode.md)

[Enable-SPOSiteRestrictedAppAccessControl](Enable-SPOSiteRestrictedAppAccessControl.md)

[Disable-SPOSiteRestrictedAppAccessControl](Disable-SPOSiteRestrictedAppAccessControl.md)

[Clear-SPOSiteRestrictedAppAccessControlList](Clear-SPOSiteRestrictedAppAccessControlList.md)

[Clear-SPOSiteRestrictedAppAccessControlPolicy](Clear-SPOSiteRestrictedAppAccessControlPolicy.md)

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
