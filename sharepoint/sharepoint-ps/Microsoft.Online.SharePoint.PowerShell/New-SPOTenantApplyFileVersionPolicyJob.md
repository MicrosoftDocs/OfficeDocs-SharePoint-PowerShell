---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: microsoft.online.sharepoint.powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/new-spotenantapplyfileversionpolicyjob
applicable: SharePoint Online
title: New-SPOTenantApplyFileVersionPolicyJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# New-SPOTenantApplyFileVersionPolicyJob

## SYNOPSIS

Queues a job to apply the tenant-level file version policy across all sites. SharePoint Advanced Management license or Copilot license is required to run this cmdlet.

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

## SYNTAX

```
New-SPOTenantApplyFileVersionPolicyJob [-TrimVersions] [-SetVersionPolicy] [-CollectVersionData]
 [-VersionPolicy <SPOFileVersionPolicySettings>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Queues a job to apply the tenant-level file version policy across all sites. The job trims existing file versions and/or sets version policy for existing document libraries based on the version policy configured at the tenant level.

The following site types are excluded from processing:

- Read-only sites
- Locked sites
- Archived sites
- Sites with version policy broken inheritance

> [!NOTE]
> - Versions deleted using this cmdlet will be permanently deleted and cannot be recovered from the recycle bin.
> - Use `Get-SPOTenantVersionPolicy` to confirm the tenant-level file version policy before running the cmdlet to make sure it matches your intended configuration. You can also use the `Get-SPOTenant` cmdlet and check the `EnableAutoExpirationVersionTrim`, `MajorVersionLimit`, `ExpireVersionsAfterDays`, and `VersionPolicyFileTypeOverride` properties.
> - If the tenant-level version policy changes while the job is in progress, the job will apply the updated policy to the remaining sites that have not yet been processed. Sites that were already processed will not be re-evaluated or updated.
> - Only one job is allowed per tenant.
> - Use `-CollectVersionData` first and wait for the job to complete before running `Get-SPOTenantApplyFileVersionPolicyJobImpact` to estimate the impact of a policy without deleting any versions.

## EXAMPLES

### Example 1
```powershell
New-SPOTenantApplyFileVersionPolicyJob -TrimVersions -SetVersionPolicy
```

Example 1 starts a tenant apply file version policy job to trim existing versions and set version policy for existing document libraries across all sites.

### Example 2
```powershell
New-SPOTenantApplyFileVersionPolicyJob -TrimVersions
```

Example 2 starts a tenant apply file version policy job to trim existing versions for files in document libraries across all sites.

### Example 3
```powershell
New-SPOTenantApplyFileVersionPolicyJob -SetVersionPolicy
```

Example 3 starts a tenant apply file version policy job to set version policy for existing document libraries across all sites.

### Example 4
```powershell
New-SPOTenantApplyFileVersionPolicyJob -CollectVersionData
```

Example 4 starts a job to collect version data across all sites. Once the job completes, use `Get-SPOTenantApplyFileVersionPolicyJobImpact` to estimate the impact of a version policy without deleting any versions.

### Example 5
```powershell
$policy = Get-SPOTenantVersionPolicy | Get-SPOVersionPolicyWithChanges -MajorVersionLimit 100
New-SPOTenantApplyFileVersionPolicyJob -TrimVersions -VersionPolicy $policy
```

Example 5 retrieves the current tenant version policy, modifies the major version limit to 100 locally, then starts a trim job using that modified policy. The tenant-level policy is updated before the job begins.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetVersionPolicy
Sets version policy for existing document libraries across all sites based on the tenant-level file version policy. The version policy applies to new versions created in these existing document libraries.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectVersionData
Collects version data across all sites for use with `Get-SPOTenantApplyFileVersionPolicyJobImpact`. Use this switch to run a data-collection pass before deciding whether and how to trim versions. The job does not delete any versions when only this switch is specified.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrimVersions
Trims existing versions for files in document libraries across all sites based on the tenant-level file version policy.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VersionPolicy
The new version policy to apply to the tenant before starting the job. When specified, the tenant-level policy is updated to match this object prior to running the job actions (`-TrimVersions`, `-SetVersionPolicy`, `-CollectVersionData`).

Use `Get-SPOTenantVersionPolicy` and `Get-SPOVersionPolicyWithChanges` to build this value.

```yaml
Type: SPOFileVersionPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
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

### System.Object
## NOTES

## RELATED LINKS

[Get-SPOTenantApplyFileVersionPolicyJobProgress](Get-SPOTenantApplyFileVersionPolicyJobProgress.md)

[Get-SPOTenantApplyFileVersionPolicyJobImpact](Get-SPOTenantApplyFileVersionPolicyJobImpact.md)

[Remove-SPOTenantApplyFileVersionPolicyJob](Remove-SPOTenantApplyFileVersionPolicyJob.md)

[Get-SPOTenantVersionPolicy](Get-SPOTenantVersionPolicy.md)

[Get-SPOVersionPolicyWithChanges](Get-SPOVersionPolicyWithChanges.md)

[Get-SPOTenant](Get-SPOTenant.md)

[SharePoint Advanced Management](/sharepoint/sharepoint-advanced-management-licensing)

[Microsoft 365 Copilot](/microsoft-365/copilot/microsoft-365-copilot-licensing)