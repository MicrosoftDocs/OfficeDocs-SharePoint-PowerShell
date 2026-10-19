---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spositerestrictedappaccesscontrollist
applicable: SharePoint Online
title: Set-SPOSiteRestrictedAppAccessControlList
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Learn how to use Set-SPOSiteRestrictedAppAccessControlList to manage site-level allow and deny lists for Application Restrictions in SharePoint Online.
ms.date: 10/13/2026
ms.topic: reference
---

# Set-SPOSiteRestrictedAppAccessControlList

## SYNOPSIS

Adds or removes application IDs in a site's Application Restrictions allow or deny list in one atomic update.

## SYNTAX

```powershell
Set-SPOSiteRestrictedAppAccessControlList [-Identity] <String> -ListType <String> [-AddRestrictedAppIds <Guid[]>] [-RemoveRestrictedAppIds <Guid[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Set-SPOSiteRestrictedAppAccessControlList` cmdlet to change the contents of one site list. Additions and removals are applied in one atomic update that preserves site enablement and the active mode.

Application Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and Application Restrictions.

Use `-ListType` to identify the target list explicitly. Both lists are always stored and can be managed regardless of which mode is active. Only the list selected by the active mode participates in runtime enforcement, so adding or removing entries in the inactive list doesn't change current enforcement. The inactive list is preserved for future mode changes.

The active mode determines what the change means at runtime. When the mode is `Allow`, applications in the allow list pass the Application Restrictions check and all other governed applications are denied by the site policy; an empty active allow list causes the site policy to deny all governed third-party and agentic applications. When the mode is `Deny`, applications in the deny list are denied by the site policy and all other governed applications pass the Application Restrictions check; an empty active deny list means the site policy denies none of them.

At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, an ID can't appear in both, and removals are applied before additions.

You supply application IDs only. Each list can contain both concrete application IDs and parent agent blueprint IDs, and the backend classifies each added ID and stores its type internally. A parent agent blueprint ID applies to the blueprint application itself and to every current or future agent app created from that blueprint. In an active deny list, a blueprint ID causes the site policy to deny that complete app family. In an active allow list, it lets that complete app family pass the Application Restrictions check. Existing Microsoft Entra consent and SharePoint authorization still apply.

Adding IDs uses the same bulk Microsoft Graph classification and first-party exclusion as the tenant cmdlets. Microsoft first-party and core applications are rejected, IDs that can't be classified are rejected, and a bulk add is all-or-none, so no partial set of IDs is persisted.

Removing entries requires only `-ListType` and `-RemoveRestrictedAppIds`. Removal doesn't call Microsoft Graph, so deleted or stale application IDs can still be removed. If a supplied ID isn't present in the target list, the cmdlet returns a validation error.

Configuration and enablement are orthogonal: a list change never turns enforcement on. Site enforcement is turned on only by `Enable-SPOSiteRestrictedAppAccessControl`, so you can stage lists and then enable the site explicitly. A mode must be explicitly configured before `Enable-SPOSiteRestrictedAppAccessControl` succeeds.

Site enforcement is also gated by the tenant switch. While the tenant switch is on, the tenant deny list takes precedence and can't be overridden by a site allow list.

Automation can use the standard `-Confirm:$false`. Suppressing the prompt doesn't bypass validation, authorization, auditing, or first-party protection.

Site Application Restrictions administration is isolated from the general-purpose `Get-SPOSite` and `Set-SPOSite` cmdlets. `Get-SPOSite` doesn't load site policy data and `Set-SPOSite` can't change it. Use the dedicated Application Restrictions cmdlets listed in [Related Links](#related-links).

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Set-SPOSiteRestrictedAppAccessControlList -Identity https://contoso.sharepoint.com/sites/Finance -ListType AllowList -AddRestrictedAppIds 11111111-1111-1111-1111-111111111111
```

This example adds one application ID to the allow list of the Finance site. The site's enablement and active mode are preserved. If the ID is a Microsoft first-party or core application, or if it can't be classified, the add is rejected.

### Example 2

```powershell
Set-SPOSiteRestrictedAppAccessControlList -Identity https://contoso.sharepoint.com/sites/Finance -ListType DenyList -AddRestrictedAppIds 22222222-2222-2222-2222-222222222222,33333333-3333-3333-3333-333333333333 -RemoveRestrictedAppIds 44444444-4444-4444-4444-444444444444
```

This example adds two application IDs and removes a third in one atomic update. The removal is applied before the additions. Site enablement and the active mode are unchanged.

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

### -ListType

> Applicable: SharePoint Online

Specifies the list to change. Valid values are `AllowList` and `DenyList`. Entry mutations must explicitly identify the target list.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AllowList, DenyList

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRestrictedAppIds

> Applicable: SharePoint Online

Specifies the application IDs to add to the list identified by `-ListType`. You supply application IDs only; the backend classifies each added ID as a regular application or a parent agent blueprint and stores the type internally.

Adds use the shared bulk Microsoft Graph classification. First-party or core applications and unclassifiable IDs are rejected, and a bulk add is all-or-none.

At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, and an ID can't appear in both.

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRestrictedAppIds

> Applicable: SharePoint Online

Specifies the application IDs to remove from the list identified by `-ListType`. Removals are applied before additions.

Removing entries doesn't call Microsoft Graph, so deleted or stale application IDs can still be removed. If a supplied ID isn't present in the target list, the cmdlet returns a validation error.

At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, and an ID can't appear in both.

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
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

### System.String

## OUTPUTS

### None

## NOTES

- Additions and removals are applied in one atomic update that preserves site enablement and the active mode.
- At least one of `-AddRestrictedAppIds` or `-RemoveRestrictedAppIds` is required, an ID can't appear in both, and removals are applied before additions.
- Each list has a hard maximum of 100 entries, and the two lists combined have a hard maximum of 200 entries. Both regular application IDs and parent agent blueprint IDs consume the same quota.
- Adding or removing entries in the list that the active mode doesn't enforce doesn't change current enforcement.
- Configuration and enablement are orthogonal. Site enforcement is turned on only by `Enable-SPOSiteRestrictedAppAccessControl`, and a mode must be explicitly configured before that cmdlet succeeds.
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
