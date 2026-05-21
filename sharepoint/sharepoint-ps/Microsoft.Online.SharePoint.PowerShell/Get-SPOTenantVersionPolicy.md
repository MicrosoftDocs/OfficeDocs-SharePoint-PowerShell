---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: microsoft.online.sharepoint.powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spotenantversionpolicy
applicable: SharePoint Online
title: Get-SPOTenantVersionPolicy
schema: 2.0.0
author: blarrywangmsft
ms.author: blarrywang
ms.reviewer:
---

# Get-SPOTenantVersionPolicy

## SYNOPSIS

Returns the current tenant-level file version policy as an `SPOFileVersionPolicySettings` object.

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
