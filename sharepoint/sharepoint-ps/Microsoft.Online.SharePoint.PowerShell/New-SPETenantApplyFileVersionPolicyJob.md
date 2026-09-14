---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: microsoft.online.sharepoint.powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/new-spetenantapplyfileversionpolicyjob
applicable: SharePoint Online
title: New-SPETenantApplyFileVersionPolicyJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# New-SPETenantApplyFileVersionPolicyJob

## SYNOPSIS

Queues a job to apply a file version policy across all containers of a SharePoint Embedded (SPE) container type. SharePoint Advanced Management license or Copilot license is required to run this cmdlet.

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

## SYNTAX

### WithExistingVersionPolicy (Default)
```
New-SPETenantApplyFileVersionPolicyJob -ContainerTypeId <Guid> [-TrimVersions] [-SetVersionPolicy]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### WithVersionPolicy
```
New-SPETenantApplyFileVersionPolicyJob -ContainerTypeId <Guid> [-TrimVersions]
 -VersionPolicy <SPOFileVersionPolicySettings> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CollectData
```
New-SPETenantApplyFileVersionPolicyJob -ContainerTypeId <Guid> [-CollectVersionData]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Queues a job to apply a file version policy across all containers that belong to the specified SharePoint Embedded (SPE) container type. The job trims existing file versions and/or sets version policy for existing containers based on the version policy supplied for the container type.

> [!NOTE]
> - Versions deleted using this cmdlet will be permanently deleted and cannot be recovered from the recycle bin.
> - Only one job is allowed per container type.
> - Use `-CollectVersionData` first and wait for the job to complete before running `Get-SPETenantApplyFileVersionPolicyJobImpact` to estimate the impact of a policy without deleting any versions.
> - `-VersionPolicy`, `-SetVersionPolicy`/`-TrimVersions`, and `-CollectVersionData` belong to mutually exclusive parameter sets and cannot be combined.
> - When `-VersionPolicy` is specified, the container-type version policy is updated. Optionally add `-TrimVersions` to also trim existing versions.

## EXAMPLES

### Example 1
```powershell
New-SPETenantApplyFileVersionPolicyJob -ContainerTypeId <ContainerTypeId> -TrimVersions -SetVersionPolicy
```

Example 1 starts a job to trim existing versions and set version policy for existing containers of the specified container type.

### Example 2
```powershell
New-SPETenantApplyFileVersionPolicyJob -ContainerTypeId <ContainerTypeId> -TrimVersions
```

Example 2 starts a job to trim existing versions for files in containers of the specified container type.

### Example 3
```powershell
New-SPETenantApplyFileVersionPolicyJob -ContainerTypeId <ContainerTypeId> -SetVersionPolicy
```

Example 3 starts a job to set version policy for existing containers of the specified container type.

### Example 4
```powershell
New-SPETenantApplyFileVersionPolicyJob -ContainerTypeId <ContainerTypeId> -CollectVersionData
```

Example 4 starts a job to collect version data across all containers of the specified container type. Once the job completes, use `Get-SPETenantApplyFileVersionPolicyJobImpact` to estimate the impact of a version policy without deleting any versions.

### Example 5
```powershell
$policy = Get-SPOTenantVersionPolicy | Get-SPOVersionPolicyWithChanges -MajorVersionLimit 100
New-SPETenantApplyFileVersionPolicyJob -ContainerTypeId <ContainerTypeId> -TrimVersions -VersionPolicy $policy
```

Example 5 builds a version policy that limits to 100 major versions locally, then starts a trim job that applies that policy to the specified container type.

## PARAMETERS

### -ContainerTypeId
The ID of the SharePoint Embedded container type to which the job applies.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Sets version policy for existing containers of the container type based on the container-type file version policy. The version policy applies to new versions created in these existing containers.

```yaml
Type: SwitchParameter
Parameter Sets: WithExistingVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectVersionData
Collects version data across all containers of the container type for use with `Get-SPETenantApplyFileVersionPolicyJobImpact`. Use this switch to run a data-collection pass before deciding whether and how to trim versions. The job does not delete any versions. Cannot be combined with `-VersionPolicy` or `-SetVersionPolicy`.

```yaml
Type: SwitchParameter
Parameter Sets: CollectData
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrimVersions
Trims existing versions for files in containers of the container type based on the container-type file version policy.

```yaml
Type: SwitchParameter
Parameter Sets: WithExistingVersionPolicy, WithVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VersionPolicy
The version policy to apply to the container type before starting the job. When specified, the container-type version policy is updated and propagated to its containers. Optionally combine with `-TrimVersions` to also trim existing versions.

Use `Get-SPOTenantVersionPolicy` and `Get-SPOVersionPolicyWithChanges` to build this value.

```yaml
Type: SPOFileVersionPolicySettings
Parameter Sets: WithVersionPolicy
Aliases:

Required: True
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

[Get-SPETenantApplyFileVersionPolicyJobProgress](Get-SPETenantApplyFileVersionPolicyJobProgress.md)

[Get-SPETenantApplyFileVersionPolicyJobImpact](Get-SPETenantApplyFileVersionPolicyJobImpact.md)

[Remove-SPETenantApplyFileVersionPolicyJob](Remove-SPETenantApplyFileVersionPolicyJob.md)

[Get-SPOTenantVersionPolicy](Get-SPOTenantVersionPolicy.md)

[Get-SPOVersionPolicyWithChanges](Get-SPOVersionPolicyWithChanges.md)

[SharePoint Advanced Management](/sharepoint/sharepoint-advanced-management-licensing)

[Microsoft 365 Copilot](/microsoft-365/copilot/microsoft-365-copilot-licensing)
