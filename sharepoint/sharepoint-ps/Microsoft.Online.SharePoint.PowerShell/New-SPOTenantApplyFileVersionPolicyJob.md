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
New-SPOTenantApplyFileVersionPolicyJob [-TrimVersions] [-SetVersionPolicy] [-WhatIf] [-Confirm] [<CommonParameters>]
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
> - Use `Get-SPOTenant` cmdlet and the `EnableAutoExpirationVersionTrim`, `MajorVersionLimit`, `ExpireVersionsAfterDays` and `VersionPolicyFileTypeOverride` properties to confirm the tenant-level file version policy before running the cmdlet to make sure it matches your intended configuration.
> - If the tenant-level version policy changes while the job is in progress, the job will apply the updated policy to the remaining sites that have not yet been processed. Sites that were already processed will not be re-evaluated or updated.
> - Allow only one job per tenant.

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

[Remove-SPOTenantApplyFileVersionPolicyJob](Remove-SPOTenantApplyFileVersionPolicyJob.md)

[Get-SPOTenant](Get-SPOTenant.md)

[SharePoint Advanced Management](/sharepoint/sharepoint-advanced-management-licensing)

[Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-licensing)