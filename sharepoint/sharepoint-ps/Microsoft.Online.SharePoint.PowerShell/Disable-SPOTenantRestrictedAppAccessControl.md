---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/disable-spotenantrestrictedappaccesscontrol
applicable: SharePoint Online
title: Disable-SPOTenantRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Disable-SPOTenantRestrictedAppAccessControl turns off tenant-wide App Restrictions enforcement while keeping your deny list intact. Learn the syntax and examples.
ms.date: 10/09/2026
ms.topic: concept-article
---

# Disable-SPOTenantRestrictedAppAccessControl

## SYNOPSIS

Turns off the tenant App Restrictions enforcement switch, while preserving the tenant deny list.

## SYNTAX

```
Disable-SPOTenantRestrictedAppAccessControl [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the `Disable-SPOTenantRestrictedAppAccessControl` cmdlet to turn off the tenant enforcement switch for App Restrictions without discarding your configuration.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions.

The tenant switch is the master enforcement switch for the feature. This cmdlet warns that the tenant switch gates all site-level enforcement, so turning it off stops every configured site policy from enforcing, not just the tenant deny list.

The tenant deny list is preserved. Stored tenant and site configuration remains in place, so enforcement resumes with the same configuration when you run `Enable-SPOTenantRestrictedAppAccessControl` again. If you want to disable the switch *and* clear the tenant deny list, use `Clear-SPOTenantRestrictedAppAccessControlPolicy` instead.

Configuration and enablement are orthogonal: this cmdlet changes only the switch, and list changes made with `Set-SPOTenantRestrictedAppAccessControlList` never flip the switch.

The tenant scope is deny-only and has a single list, so there's no mode cmdlet and no `-ListType` parameter at tenant scope.

App Restrictions administration is isolated from the general-purpose `Get-SPOTenant` and `Set-SPOTenant` cmdlets. App Restrictions isn't exposed as a `Tenant` property, so `Get-SPOTenant` doesn't return the policy and `Set-SPOTenant` can't change it.

You must be at least a SharePoint Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```
Disable-SPOTenantRestrictedAppAccessControl
```

This example turns off the tenant enforcement switch and preserves the tenant deny list. The cmdlet warns that the tenant switch gates all site-level enforcement, and then prompts for confirmation.

### Example 2

```
Disable-SPOTenantRestrictedAppAccessControl -WhatIf
```

This example shows what would happen if the tenant switch were turned off, without changing the stored tenant policy.

### Example 3

```
Disable-SPOTenantRestrictedAppAccessControl -Confirm:$false
Get-SPOTenantRestrictedAppAccessControl
```

This example turns off the tenant switch without prompting, which is useful in automation, and then reads the tenant policy to confirm that `Enabled` is `False` and that `RestrictedAppIds` still contains the preserved deny list. Suppressing the prompt doesn't bypass validation, authorization, or auditing.

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

- The cmdlet warns that the tenant switch gates all site-level enforcement, so turning it off stops every configured site policy from enforcing, not just the tenant deny list.
- The tenant deny list is preserved, and stored tenant and site configuration is preserved, so enforcement resumes with the same configuration when the switch is turned on again.
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
