---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/clear-spositerestrictedappaccesscontrollist
applicable: SharePoint Online
title: Clear-SPOSiteRestrictedAppAccessControlList
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Clear-SPOSiteRestrictedAppAccessControlList removes all entries from a site's allow or deny list in SharePoint Online. Learn syntax, examples, and parameters.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Clear-SPOSiteRestrictedAppAccessControlList

## SYNOPSIS

Removes every entry from one app restrictions list on a site, preserving the other list, the active mode, and site enablement.

## SYNTAX

```
Clear-SPOSiteRestrictedAppAccessControlList -Identity <String> -ListType <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use the `Clear-SPOSiteRestrictedAppAccessControlList` cmdlet to clear the allow list or the deny list on a single site. Clearing one list always clears it, and preserves the other list, the active mode, and site enablement. To remove both lists and the mode and clear the stored site policy, use `Clear-SPOSiteRestrictedAppAccessControlPolicy` instead.

A site stores both lists, but only the list selected by the active mode participates in enforcement:

- **Allow** mode enforces the allow list. Subjects in the allow list are allowed and all other governed apps are denied.
- **Deny** mode enforces the deny list. Subjects in the deny list are denied and all other governed apps are allowed.

When the cleared list is the one the active mode enforces, the cmdlet emits a warning before confirmation. Clearing the active allow list means no third-party applications can access the site, because an empty active allow list blocks all governed third-party and agentic apps. Clearing the active deny list means all of them can. The warning also states whether the change takes effect immediately or when enforcement is next enabled.

Clearing an inactive list doesn't change current enforcement, but it still supports `-WhatIf` and `-Confirm`, and it's audited.

Configuration and enablement are orthogonal. List changes never turn enforcement on, so clearing a list on a site that isn't enabled leaves the site disabled and stages the change for the next time enforcement is enabled with `Enable-SPOSiteRestrictedAppAccessControl`. This avoids the dangerous case where adding a single ID to an unconfigured site would immediately activate an allow list and block every other application.

The tenant switch gates all site enforcement. A site policy has no effect while the tenant switch is off, and the tenant deny list can't be overridden by a site allow list, so clearing a site deny list never restores access for an application that the tenant denies.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions.

Site App Restrictions administration is isolated from the general-purpose `Get-SPOSite` and `Set-SPOSite` cmdlets. App Restrictions is fully decoupled from `SiteProperties`, so `Get-SPOSite` doesn't load site policy data and `Set-SPOSite` can't change it. Use the dedicated App Restrictions cmdlets listed in [Related Links](#related-links).

You must be at least a SharePoint Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```
Clear-SPOSiteRestrictedAppAccessControlList -Identity "https://contoso.sharepoint.com/sites/Finance" -ListType DenyList
```

This example clears the deny list on the Finance site. It preserves the allow list, the active mode, and site enablement. If `Deny` is the active mode, the cmdlet warns that clearing the active deny list means all governed third-party applications can access the site.

### Example 2

```
Clear-SPOSiteRestrictedAppAccessControlList -Identity "e1b2c3d4-5678-4abc-9def-0123456789ab" -ListType AllowList -WhatIf
```

This example identifies the site by site ID and previews clearing the allow list without changing the policy. Every site App Restrictions cmdlet accepts `-Identity` as either a site URL or a site ID.

### Example 3

```
$url = "https://contoso.sharepoint.com/sites/Finance"
Clear-SPOSiteRestrictedAppAccessControlList -Identity $url -ListType AllowList
Set-SPOSiteRestrictedAppAccessControlList -Identity $url -ListType AllowList -AddRestrictedAppIds "11111111-1111-1111-1111-111111111111"
```

This example rebuilds an allow list from scratch. Because list changes are configuration-only, neither command changes whether the site is enabled.

### Example 4

```
Clear-SPOSiteRestrictedAppAccessControlList -Identity "https://contoso.sharepoint.com/sites/Finance" -ListType DenyList -Confirm:$false
```

This example clears the deny list without an interactive confirmation prompt, for use in automation. Using `-Confirm:$false` doesn't bypass validation, authorization, auditing, or first-party protection.

## PARAMETERS

### -Identity

Specifies the site to change. Provide either the site URL or the site ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: []
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListType

Specifies which list to clear. Entry mutations must explicitly identify the target list. The valid values are:

- `AllowList`
- `DenyList`

```yaml
Type: String
Parameter Sets: (All)
Aliases: []
Accepted values: AllowList, DenyList
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

- Clearing one list preserves the other list, the active mode, and site enablement.
- Clearing the list that the active mode enforces changes the effective decision for the site: an empty active allow list blocks all governed third-party and agentic apps, and an empty active deny list allows all of them. The cmdlet warns before confirmation and states whether the change takes effect immediately or when enforcement is next enabled.
- Clearing an inactive list doesn't change current enforcement, but the operation still supports `-WhatIf` and `-Confirm` and is audited.
- List changes never turn enforcement on. Site enforcement is turned on only by `Enable-SPOSiteRestrictedAppAccessControl`.
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

[Clear-SPOSiteRestrictedAppAccessControlPolicy](Clear-SPOSiteRestrictedAppAccessControlPolicy.md)

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
