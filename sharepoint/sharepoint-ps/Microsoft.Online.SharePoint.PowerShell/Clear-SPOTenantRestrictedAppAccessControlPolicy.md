---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/clear-spotenantrestrictedappaccesscontrolpolicy
applicable: SharePoint Online
title: Clear-SPOTenantRestrictedAppAccessControlPolicy
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Clear-SPOTenantRestrictedAppAccessControlPolicy disables tenant App Restrictions enforcement and clears the deny list. Learn syntax, parameters, and examples.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Clear-SPOTenantRestrictedAppAccessControlPolicy

## SYNOPSIS

Turns off the tenant App Restrictions enforcement switch and clears the tenant-wide deny list.

## SYNTAX

```
Clear-SPOTenantRestrictedAppAccessControlPolicy [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Clear-SPOTenantRestrictedAppAccessControlPolicy` cmdlet to reset the tenant Restricted App Access Control policy. The cmdlet disables the tenant enforcement switch and clears the tenant-wide deny list in one operation.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions.

This cmdlet warns that the tenant switch gates all site-level enforcement, so turning it off stops every configured site policy from enforcing, not just the tenant deny list.

The tenant scope is deny-only with a single list, so there's no separate clear-list cmdlet. Clearing the only list while leaving the switch on would be indistinguishable from the feature being off, so `Clear-SPOTenantRestrictedAppAccessControlPolicy` covers that intent.

Use this cmdlet when you want to remove the tenant configuration entirely. If you want to stop enforcement but keep the deny list for later, use `Disable-SPOTenantRestrictedAppAccessControl` instead. If you want to remove only selected application IDs, use `Set-SPOTenantRestrictedAppAccessControlList` with `-RemoveRestrictedAppIds`.

Removing IDs doesn't require Microsoft Graph, so stale or deleted applications on the tenant deny list are cleared along with the rest of the list.

Tenant App Restrictions administration is isolated from the general-purpose `Get-SPOTenant` and `Set-SPOTenant` cmdlets. App Restrictions isn't exposed as a `Tenant` property, so `Get-SPOTenant` doesn't return the policy and `Set-SPOTenant` can't change it.

You must be at least a SharePoint Administrator or to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## Examples

### Example 1

```
Clear-SPOTenantRestrictedAppAccessControlPolicy
```

This example turns off the tenant enforcement switch and clears the tenant deny list. The cmdlet warns that the tenant switch gates all site-level enforcement, and then prompts for confirmation.

### Example 2

```
Clear-SPOTenantRestrictedAppAccessControlPolicy -WhatIf
```

This example shows what would happen if the tenant policy were cleared, without changing the stored tenant policy.

### Example 3

```powershell
Get-SPOTenantRestrictedAppAccessControl
Clear-SPOTenantRestrictedAppAccessControlPolicy -Confirm:$false
Get-SPOTenantRestrictedAppAccessControl
```

This example records the current tenant policy, clears it without prompting for confirmation, and then reads the policy again to confirm that `Enabled` is `False` and that `RestrictedAppIds` is empty. Suppressing the prompt doesn't bypass validation, authorization, or auditing.

## Parameters

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

This cmdlet doesn't return an output object. Use `Get-SPOTenantRestrictedAppAccessControl` to confirm the resulting tenant policy.

## NOTES

- This cmdlet disables the tenant switch and clears the tenant deny list. To stop enforcement while preserving the deny list, use `Disable-SPOTenantRestrictedAppAccessControl`.
- The cmdlet warns that the tenant switch gates all site-level enforcement, so turning it off stops every configured site policy from enforcing, not just the tenant deny list.
- The tenant scope is deny-only with a single list, so there's no separate clear-list cmdlet at tenant scope.
- Clearing doesn't call Microsoft Graph, so stale or deleted application IDs are removed with the rest of the list.
- This cmdlet doesn't remove site policy configuration. Use `Clear-SPOSiteRestrictedAppAccessControlPolicy` to clear the policy for an individual site.

## Related links

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Set-SPOTenantRestrictedAppAccessControlList](Set-SPOTenantRestrictedAppAccessControlList.md)

[Enable-SPOTenantRestrictedAppAccessControl](Enable-SPOTenantRestrictedAppAccessControl.md)

[Disable-SPOTenantRestrictedAppAccessControl](Disable-SPOTenantRestrictedAppAccessControl.md)

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
