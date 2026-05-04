---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: microsoft.online.sharepoint.powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spotenantversiopolicy
applicable: SharePoint Online
title: Get-SPOTenantVersionPolicy
schema: 2.0.0
author: blarrywangmsft
ms.author: blarrywang
ms.reviewer:
manager: seanmc
---

# Get-SPOTenantVersionPolicy

## SYNOPSIS

Returns the current tenant-level file version policy as an `SPOFileVersionPolicySettings` object. SharePoint Advanced Management license or Copilot license is required to run this cmdlet.

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

## SYNTAX

```
Get-SPOTenantVersionPolicy [<CommonParameters>]
```

## DESCRIPTION

Returns the current tenant-level file version policy, including the default policy settings and any per-file-type overrides, as an `SPOFileVersionPolicySettings` object.

The returned object is a local copy and can be modified using `Get-SPOVersionPolicyWithChanges`. Pass the modified policy to `New-SPOTenantApplyFileVersionPolicyJob` to apply it to the tenant, or to `Get-SPOTenantApplyFileVersionPolicyJobImpact` to estimate trimming impact without making changes.

## EXAMPLES

### Example 1
```powershell
Get-SPOTenantVersionPolicy
```

Returns the current tenant-level file version policy.

### Example 2
```powershell
$policy = Get-SPOTenantVersionPolicy
```

Stores the current tenant-level file version policy in a variable for further modification with `Get-SPOVersionPolicyWithChanges`.

### Example 3
```powershell
$policy = Get-SPOTenantVersionPolicy | Get-SPOVersionPolicyWithChanges -MajorVersionLimit 100
New-SPOTenantApplyFileVersionPolicyJob -TrimVersions -VersionPolicy $policy
```

Retrieves the current policy, changes the major version limit to 100, and starts a job to trim versions using that modified policy.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### Microsoft.Online.SharePoint.TenantAdministration.SPOFileVersionPolicySettings

## NOTES

## RELATED LINKS

[Get-SPOVersionPolicyWithChanges](Get-SPOVersionPolicyWithChanges.md)

[New-SPOTenantApplyFileVersionPolicyJob](New-SPOTenantApplyFileVersionPolicyJob.md)

[Get-SPOTenantApplyFileVersionPolicyJobImpact](Get-SPOTenantApplyFileVersionPolicyJobImpact.md)

[SharePoint Advanced Management](/sharepoint/sharepoint-advanced-management-licensing)

[Microsoft 365 Copilot](/microsoft-365/copilot/microsoft-365-copilot-licensing)
