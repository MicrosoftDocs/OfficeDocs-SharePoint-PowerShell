---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: microsoft.online.sharepoint.powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/remove-spetenantapplyfileversionpolicyjob
applicable: SharePoint Online
title: Remove-SPETenantApplyFileVersionPolicyJob
schema: 2.0.0
author: guptapriyan
ms.author: guptapriyan
ms.reviewer:
manager: srikrg
---

# Remove-SPETenantApplyFileVersionPolicyJob

## SYNOPSIS

Stops further processing of an apply file version policy job that is in progress for a SharePoint Embedded (SPE) container type. SharePoint Advanced Management license or Copilot license is required to run this cmdlet.

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

## SYNTAX

```
Remove-SPETenantApplyFileVersionPolicyJob -ContainerTypeId <Guid> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Stops further processing of an apply file version policy job that is in progress for the specified SharePoint Embedded (SPE) container type.

> [!NOTE]
> - If the job was queued by using `New-SPETenantApplyFileVersionPolicyJob` with the `TrimVersions` parameter, this stops creating new sub-jobs that trim versions for containers. This does not affect versions that were already permanently deleted while the job was running.
> - If the job was queued by using `New-SPETenantApplyFileVersionPolicyJob` with the `SetVersionPolicy` parameter, this stops creating new sub-jobs that apply the new version policy to existing containers. The version policies that were already applied remain in place and will not be reverted.

## EXAMPLES

### Example 1
```powershell
Remove-SPETenantApplyFileVersionPolicyJob -ContainerTypeId <ContainerTypeId>
```

Example 1 cancels further processing of the apply file version policy job for the specified container type.

## PARAMETERS

### -ContainerTypeId
The ID of the SharePoint Embedded container type whose job is canceled.

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

[New-SPETenantApplyFileVersionPolicyJob](New-SPETenantApplyFileVersionPolicyJob.md)

[Get-SPETenantApplyFileVersionPolicyJobProgress](Get-SPETenantApplyFileVersionPolicyJobProgress.md)

[SharePoint Advanced Management](/sharepoint/sharepoint-advanced-management-licensing)

[Microsoft 365 Copilot](/microsoft-365/copilot/microsoft-365-copilot-licensing)
