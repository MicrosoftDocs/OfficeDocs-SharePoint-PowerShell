---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/enable-spotenantrestrictedappaccesscontrol
applicable: SharePoint Online
title: Enable-SPOTenantRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Learn how to use Enable-SPOTenantRestrictedAppAccessControl to activate the master enforcement switch for Application Restrictions across your SharePoint Online tenant.
ms.date: 10/13/2026
ms.topic: reference
---

# Enable-SPOTenantRestrictedAppAccessControl

## SYNOPSIS

Turns on the tenant Application Restrictions enforcement switch for your organization.

## SYNTAX

```powershell
Enable-SPOTenantRestrictedAppAccessControl [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Enable-SPOTenantRestrictedAppAccessControl` cmdlet to turn on the tenant enforcement switch for Application Restrictions.

Application Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and Application Restrictions.

The tenant switch is the master enforcement switch for Application Restrictions. While it's off, the tenant deny list isn't enforced, and no site-level policy is enforced. Turning on the switch starts tenant deny-list enforcement and site-level enforcement only for site policies whose site-level `Enabled` flag is `True`. Disabled site policies don't begin enforcing. Review the stored tenant deny list with `Get-SPOTenantRestrictedAppAccessControl` and review enabled site policies before you enable the switch.

Enabling the switch doesn't change the stored deny list. Configuration and enablement are orthogonal: this cmdlet changes only the switch, and list changes made with `Set-SPOTenantRestrictedAppAccessControlList` never flip the switch. Enforcement resumes with the configuration that was preserved while the switch was off.

An enabled switch with an empty tenant deny list is a valid state, but the tenant deny list denies nothing until an application ID is added.

The tenant scope is deny-only and has a single list, so there's no mode cmdlet and no `-ListType` parameter at tenant scope.

Tenant Application Restrictions administration is isolated from the general-purpose `Get-SPOTenant` and `Set-SPOTenant` cmdlets. Application Restrictions isn't exposed as a `Tenant` property, so `Get-SPOTenant` doesn't return the policy and `Set-SPOTenant` can't change it.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Enable-SPOTenantRestrictedAppAccessControl
```

This example turns on the tenant enforcement switch. Tenant deny-list enforcement starts, along with site-level enforcement for site policies whose site-level `Enabled` flag is `True`. Disabled site policies don't begin enforcing. The cmdlet warns about this effect and then prompts for confirmation.

### Example 2

```powershell
Get-SPOTenantRestrictedAppAccessControl
Enable-SPOTenantRestrictedAppAccessControl
```

This example reviews the stored tenant policy first so you can see which application IDs are on the deny list, and then turns on enforcement. Site-level enforcement starts only for site policies whose site-level `Enabled` flag is `True`.

### Example 3

```powershell
Enable-SPOTenantRestrictedAppAccessControl -WhatIf
```

This example shows what would happen if the tenant switch were turned on, without changing the stored tenant policy.

### Example 4

```powershell
Enable-SPOTenantRestrictedAppAccessControl -Confirm:$false
```

This example turns on the tenant switch without prompting for confirmation, which is useful in automation. Suppressing the prompt doesn't bypass validation, authorization, auditing, or first-party protection.

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

- Turning on the tenant switch starts tenant deny-list enforcement and site-level enforcement only for site policies whose site-level `Enabled` flag is `True`. Disabled site policies don't begin enforcing.
- The tenant switch is the master enforcement switch. While it's off, the tenant deny list and all site-level policies aren't enforced.
- Enabling the switch doesn't change the stored deny list. Configuration and enablement are orthogonal.
- An enabled switch with an empty deny list is allowed, but the tenant deny list denies nothing until an application ID is added.
- Microsoft first-party and core applications are excluded from Application Restrictions configuration and enforcement.
- Use `Enable-SPOSiteRestrictedAppAccessControl` to turn on enforcement for an individual site.

## RELATED LINKS

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Set-SPOTenantRestrictedAppAccessControlList](Set-SPOTenantRestrictedAppAccessControlList.md)

[Disable-SPOTenantRestrictedAppAccessControl](Disable-SPOTenantRestrictedAppAccessControl.md)

[Clear-SPOTenantRestrictedAppAccessControlPolicy](Clear-SPOTenantRestrictedAppAccessControlPolicy.md)

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
