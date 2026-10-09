---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/enable-spotenantrestrictedappaccesscontrol
applicable: SharePoint Online
title: Enable-SPOTenantRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Learn how to use Enable-SPOTenantRestrictedAppAccessControl to activate the master enforcement switch for App Restrictions across your SharePoint Online tenant.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Enable-SPOTenantRestrictedAppAccessControl

## SYNOPSIS

Turns on the tenant App Restrictions enforcement switch for your organization.

## SYNTAX

```
Enable-SPOTenantRestrictedAppAccessControl [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Enable-SPOTenantRestrictedAppAccessControl` cmdlet to turn on the tenant enforcement switch for Restricted App Access Control.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions.

The tenant switch is the master enforcement switch for the feature. While it's off, no App Restrictions policy is enforced, including the tenant deny list and every configured site policy. This cmdlet warns that enforcement begins tenant-wide, including all configured site policies. Review the stored tenant deny list with `Get-SPOTenantRestrictedAppAccessControl` and review your site policies before you enable the switch.

Enabling the switch doesn't change the stored deny list. Configuration and enablement are orthogonal: this cmdlet changes only the switch, and list changes made with `Set-SPOTenantRestrictedAppAccessControlList` never flip the switch. Enforcement resumes with the configuration that was preserved while the switch was off.

An enabled switch with an empty tenant deny list is a valid state, but the tenant deny list denies nothing until an application ID is added.

The tenant scope is deny-only and has a single list, so there's no mode cmdlet and no `-ListType` parameter at tenant scope.

Tenant App Restrictions administration is isolated from the general-purpose `Get-SPOTenant` and `Set-SPOTenant` cmdlets. App Restrictions isn't exposed as a `Tenant` property, so `Get-SPOTenant` doesn't return the policy and `Set-SPOTenant` can't change it.

You must be at least a SharePoint Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```
Enable-SPOTenantRestrictedAppAccessControl
```

This example turns on the tenant enforcement switch. The cmdlet warns that enforcement begins tenant-wide, including all configured site policies, and then prompts for confirmation.

### Example 2

```
Get-SPOTenantRestrictedAppAccessControl
Enable-SPOTenantRestrictedAppAccessControl
```

This example reviews the stored tenant policy first, so you can see which application IDs are on the deny list, and then turns on enforcement.

### Example 3

```
Enable-SPOTenantRestrictedAppAccessControl -WhatIf
```

This example shows what would happen if the tenant switch were turned on, without changing the stored tenant policy.

### Example 4

```
Enable-SPOTenantRestrictedAppAccessControl -Confirm:$false
```

This example turns on the tenant switch without prompting for confirmation, which is useful in automation. Suppressing the prompt doesn't bypass validation, authorization, or auditing.

## PARAMETERS

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

- The cmdlet warns that enforcement begins tenant-wide, including all configured site policies.
- The tenant switch is the master enforcement switch. While it's off, no App Restrictions policy is enforced, including the tenant deny list and all site policies.
- Enabling the switch doesn't change the stored deny list. Configuration and enablement are orthogonal.
- An enabled switch with an empty deny list is allowed, but the tenant deny list denies nothing until an application ID is added.
- Microsoft first-party and core applications are excluded from App Restrictions configuration and enforcement.
- Use `Enable-SPOSiteRestrictedAppAccessControl` to turn on enforcement for an individual site.

## RELATED LINKS

[Get-SPOTenantRestrictedAppAccessControl](Get-SPOTenantRestrictedAppAccessControl.md)

[Set-SPOTenantRestrictedAppAccessControlList](Set-SPOTenantRestrictedAppAccessControlList.md)

[Disable-SPOTenantRestrictedAppAccessControl](Disable-SPOTenantRestrictedAppAccessControl.md)

[Clear-SPOTenantRestrictedAppAccessControlPolicy](Clear-SPOTenantRestrictedAppAccessControlPolicy.md)

[Get-SPOSiteRestrictedAppAccessControl](Get-SPOSiteRestrictedAppAccessControl.md)

[Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)
