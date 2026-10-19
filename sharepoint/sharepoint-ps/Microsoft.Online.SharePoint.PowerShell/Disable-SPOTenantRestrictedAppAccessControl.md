---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/disable-spotenantrestrictedappaccesscontrol
applicable: SharePoint Online
title: Disable-SPOTenantRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Disable-SPOTenantRestrictedAppAccessControl turns off tenant-wide Application Restrictions enforcement while keeping your deny list intact. Learn the syntax and examples.
ms.date: 10/13/2026
ms.topic: reference
---

# Disable-SPOTenantRestrictedAppAccessControl

## SYNOPSIS

Turns off the tenant Application Restrictions enforcement switch while preserving the tenant deny list.

## SYNTAX

```powershell
Disable-SPOTenantRestrictedAppAccessControl [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Disable-SPOTenantRestrictedAppAccessControl` cmdlet to turn off the tenant enforcement switch for Application Restrictions without discarding your configuration.

Application Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and Application Restrictions.

The tenant switch is the master enforcement switch for Application Restrictions. It gates the tenant deny list and all site-level enforcement. Turning it off stops enforcement for every site policy whose site-level `Enabled` flag is `True`, not only the tenant deny list. The cmdlet warns about this effect before confirmation.

The tenant deny list is preserved. Stored tenant and site configuration remains in place, so enforcement resumes with the same configuration when you run `Enable-SPOTenantRestrictedAppAccessControl` again. If you want to disable the switch *and* clear the tenant deny list, use `Clear-SPOTenantRestrictedAppAccessControlPolicy` instead.

Configuration and enablement are orthogonal: this cmdlet changes only the switch, and list changes made with `Set-SPOTenantRestrictedAppAccessControlList` never flip the switch.

The tenant scope is deny-only and has a single list, so there's no mode cmdlet and no `-ListType` parameter at tenant scope.

Tenant Application Restrictions administration is isolated from the general-purpose `Get-SPOTenant` and `Set-SPOTenant` cmdlets. Application Restrictions isn't exposed as a `Tenant` property, so `Get-SPOTenant` doesn't return the policy and `Set-SPOTenant` can't change it.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Disable-SPOTenantRestrictedAppAccessControl
```

This example turns off the tenant enforcement switch and preserves the tenant deny list. The cmdlet warns that this also stops enforcement for every site policy whose site-level `Enabled` flag is `True`, and then prompts for confirmation.

### Example 2

```powershell
Disable-SPOTenantRestrictedAppAccessControl -WhatIf
```

This example shows what would happen if the tenant switch were turned off, without changing the stored tenant policy.

### Example 3

```powershell
Disable-SPOTenantRestrictedAppAccessControl -Confirm:$false
Get-SPOTenantRestrictedAppAccessControl
```

This example turns off the tenant switch without prompting, which is useful in automation, and then reads the tenant policy to confirm that `Enabled` is `False` and that `RestrictedAppIds` still contains the preserved deny list. Suppressing the prompt doesn't bypass validation, authorization, auditing, or first-party protection.

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

- The tenant switch gates the tenant deny list and all site-level enforcement. Turning it off stops enforcement for every site policy whose site-level `Enabled` flag is `True`, not only the tenant deny list.
- The tenant deny list and all stored tenant and site configuration are preserved. Enforcement resumes with the same configuration when the switch is turned on again.
- Configuration and enablement are orthogonal: this cmdlet doesn't change the deny list.
- To disable the switch and clear the tenant deny list in one operation, use `Clear-SPOTenantRestrictedAppAccessControlPolicy`.
- Use `Disable-SPOSiteRestrictedAppAccessControl` to turn off enforcement for an individual site.

## RELATED LINKS

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Set-SPOTenantRestrictedAppAccessControlList](Set-SPOTenantRestrictedAppAccessControlList.md)

[Enable-SPOTenantRestrictedAppAccessControl](Enable-SPOTenantRestrictedAppAccessControl.md)

[Clear-SPOTenantRestrictedAppAccessControlPolicy](Clear-SPOTenantRestrictedAppAccessControlPolicy.md)

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
