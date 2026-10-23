---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/clear-spotenantrestrictedappaccesscontrolpolicy
applicable: SharePoint Online
title: Clear-SPOTenantRestrictedAppAccessControlPolicy
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Clear-SPOTenantRestrictedAppAccessControlPolicy disables tenant Application Restrictions enforcement and clears the deny list. Learn syntax, parameters, and examples.
ms.date: 10/13/2026
ms.topic: reference
---

# Clear-SPOTenantRestrictedAppAccessControlPolicy

## SYNOPSIS

Turns off the tenant Application Restrictions enforcement switch and clears the tenant-wide deny list.

## SYNTAX

```powershell
Clear-SPOTenantRestrictedAppAccessControlPolicy [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Clear-SPOTenantRestrictedAppAccessControlPolicy` cmdlet to reset the tenant Application Restrictions policy. The cmdlet disables the tenant enforcement switch and clears the tenant-wide deny list in one operation.

Application Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and Application Restrictions.

The tenant switch gates the tenant deny list and all site-level enforcement. Turning it off stops enforcement for every site policy whose site-level `Enabled` flag is `True`, not only the tenant deny list. The cmdlet warns about this effect before confirmation.

The tenant scope is deny-only with a single list, so there's no separate clear-list cmdlet. To empty the deny list while keeping the tenant switch on for enabled site policies, remove its application IDs with `Set-SPOTenantRestrictedAppAccessControlList`. Use `Clear-SPOTenantRestrictedAppAccessControlPolicy` to remove the tenant policy entirely.

Use this cmdlet when you want to remove the tenant configuration entirely. If you want to stop enforcement but keep the deny list for later, use `Disable-SPOTenantRestrictedAppAccessControl` instead. If you want to remove only selected application IDs, use `Set-SPOTenantRestrictedAppAccessControlList` with `-RemoveRestrictedAppIds`.

Removing IDs doesn't require Microsoft Graph, so stale or deleted applications on the tenant deny list are cleared along with the rest of the list.

Tenant Application Restrictions administration is isolated from the general-purpose `Get-SPOTenant` and `Set-SPOTenant` cmdlets. Application Restrictions isn't exposed as a `Tenant` property, so `Get-SPOTenant` doesn't return the policy and `Set-SPOTenant` can't change it.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Clear-SPOTenantRestrictedAppAccessControlPolicy
```

This example turns off the tenant enforcement switch and clears the tenant deny list. The cmdlet warns that this also stops enforcement for every site policy whose site-level `Enabled` flag is `True`, and then prompts for confirmation.

### Example 2

```powershell
Clear-SPOTenantRestrictedAppAccessControlPolicy -WhatIf
```

This example shows what would happen if the tenant policy were cleared, without changing the stored tenant policy.

### Example 3

```powershell
Get-SPOTenantRestrictedAppAccessControl
Clear-SPOTenantRestrictedAppAccessControlPolicy -Confirm:$false
Get-SPOTenantRestrictedAppAccessControl
```

This example reads the current tenant policy, clears it without prompting for confirmation, and reads the policy again to confirm that `Enabled` is `False` and `RestrictedAppIds` is empty. Suppressing the prompt doesn't bypass validation, authorization, auditing, or first-party protection.

## PARAMETERS

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before running the cmdlet. This cmdlet uses `ConfirmImpact.High`, so it prompts by default. Use `-Confirm:$false` to suppress the prompt in automation. Suppressing the prompt doesn't bypass validation, authorization, auditing, or first-party protection.

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

### None

## OUTPUTS

### None

This cmdlet doesn't return an output object. Use `Get-SPOTenantRestrictedAppAccessControl` to confirm the resulting tenant policy.

## NOTES

- This cmdlet disables the tenant switch and clears the tenant deny list. To stop enforcement while preserving the deny list, use `Disable-SPOTenantRestrictedAppAccessControl`.
- The tenant switch gates the tenant deny list and all site-level enforcement. Turning it off stops enforcement for every site policy whose site-level `Enabled` flag is `True`, not only the tenant deny list. The cmdlet warns about this effect before confirmation.
- The tenant scope is deny-only with a single list, so there's no separate clear-list cmdlet at tenant scope.
- Clearing doesn't call Microsoft Graph, so stale or deleted application IDs are removed with the rest of the list.
- This cmdlet doesn't remove site policy configuration. Use `Clear-SPOSiteRestrictedAppAccessControlPolicy` to clear the policy for an individual site.

## RELATED LINKS

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Set-SPOTenantRestrictedAppAccessControlList](Set-SPOTenantRestrictedAppAccessControlList.md)

[Enable-SPOTenantRestrictedAppAccessControl](Enable-SPOTenantRestrictedAppAccessControl.md)

[Disable-SPOTenantRestrictedAppAccessControl](Disable-SPOTenantRestrictedAppAccessControl.md)

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
