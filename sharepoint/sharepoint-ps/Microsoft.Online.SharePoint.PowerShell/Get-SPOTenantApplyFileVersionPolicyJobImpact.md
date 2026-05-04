---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: microsoft.online.sharepoint.powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spotenantapplyfileversionpolicyjobimpact
applicable: SharePoint Online
title: Get-SPOTenantApplyFileVersionPolicyJobImpact
schema: 2.0.0
author: blarrywangmsft
ms.author: blarrywang
ms.reviewer:
manager: seanmc
---

# Get-SPOTenantApplyFileVersionPolicyJobImpact

## SYNOPSIS

Estimates how many versions would be trimmed and how much storage would be freed by applying a given version policy to the tenant's collected version dataset. SharePoint Advanced Management license or Copilot license is required to run this cmdlet.

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

## SYNTAX

```
Get-SPOTenantApplyFileVersionPolicyJobImpact -VersionPolicy <SPOFileVersionPolicySettings> [<CommonParameters>]
```

## DESCRIPTION

Queries the version dataset collected by a previously completed `New-SPOTenantApplyFileVersionPolicyJob -CollectVersionData` job and returns an estimated impact object showing how many versions would be deleted and how much storage would be freed if the specified version policy were applied.

> [!NOTE]
> - A completed job that was started with `-CollectVersionData` is required before running this cmdlet. Use `Get-SPOTenantApplyFileVersionPolicyJobProgress` to confirm the job has completed.
> - The estimate is based on a snapshot collected during the job and may not reflect changes made to the tenant after the job ran.

## EXAMPLES

### Example 1
```powershell
$policy = Get-SPOTenantVersionPolicy
Get-SPOTenantApplyFileVersionPolicyJobImpact -VersionPolicy $policy
```

Estimates the impact of trimming using the current tenant version policy against the collected dataset.

### Example 2
```powershell
$policy = Get-SPOTenantVersionPolicy | Get-SPOVersionPolicyWithChanges -MajorVersionLimit 50
Get-SPOTenantApplyFileVersionPolicyJobImpact -VersionPolicy $policy
```

Estimates the impact of a more aggressive policy (50 major versions) compared to the current tenant policy.

### Example 3
```powershell
New-SPOTenantApplyFileVersionPolicyJob -CollectVersionData
# Wait for the job to complete, then estimate impact before trimming.
$impact = Get-SPOTenantVersionPolicy | Get-SPOTenantApplyFileVersionPolicyJobImpact -VersionPolicy $_
Write-Host "Estimated versions to trim: $($impact.TrimCount)"
Write-Host "Estimated storage freed: $($impact.TrimStorageGB) GB"
```

Runs a data-collection job, waits for it to complete, then evaluates the impact of the current policy before committing to a trim operation.

## PARAMETERS

### -VersionPolicy
The version policy to evaluate. Use `Get-SPOTenantVersionPolicy` and `Get-SPOVersionPolicyWithChanges` to build this value.

```yaml
Type: SPOFileVersionPolicySettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### Microsoft.Online.SharePoint.TenantAdministration.SPOTenantVersionPolicyImpact

The returned object has the following properties:

| Property | Type | Description |
|---|---|---|
| TrimCount | Int32 | Estimated number of versions that would be deleted. |
| TrimStorageGB | Double | Estimated storage freed by trimming, in gigabytes. |

## NOTES

## RELATED LINKS

[New-SPOTenantApplyFileVersionPolicyJob](New-SPOTenantApplyFileVersionPolicyJob.md)

[Get-SPOTenantApplyFileVersionPolicyJobProgress](Get-SPOTenantApplyFileVersionPolicyJobProgress.md)

[Get-SPOTenantVersionPolicy](Get-SPOTenantVersionPolicy.md)

[Get-SPOVersionPolicyWithChanges](Get-SPOVersionPolicyWithChanges.md)

[SharePoint Advanced Management](/sharepoint/sharepoint-advanced-management-licensing)

[Microsoft 365 Copilot](/microsoft-365/copilot/microsoft-365-copilot-licensing)
