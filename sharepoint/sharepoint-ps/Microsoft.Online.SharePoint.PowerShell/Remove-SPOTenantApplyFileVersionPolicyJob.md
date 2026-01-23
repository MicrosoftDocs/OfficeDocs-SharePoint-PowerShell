---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: microsoft.online.sharepoint.powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/remove-spotenantapplyfileversionpolicyjob
applicable: SharePoint Online
title: Remove-SPOTenantApplyFileVersionPolicyJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Remove-SPOTenantApplyFileVersionPolicyJob

## SYNOPSIS

Stops further processing of tenant apply file version policy job that is in progress. SharePoint Advanced Management license is required to run this cmdlet.

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

## SYNTAX

```
Remove-SPOTenantApplyFileVersionPolicyJob [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Stops further processing of tenant apply file version policy job that is in progress.

> [!NOTE]
> - If the tenant apply version job is queued by using the cmdlet `New-SPOTenantApplyFileVersionPolicyJob` with the `TrimVersions` parameter, this will stop creating new sub-jobs that trim versions for sites. This does not affect versions that were already permanently deleted while the job was running.
> - If the tenant apply version job is queued by using the cmdlet `New-SPOTenantApplyFileVersionPolicyJob` with the `SetVersionPolicy` parameter, this will stop creating new sub-jobs that apply the new version policy to existing document libraries for sites. The version policies that were already applied remain in place and will not be reverted.

## EXAMPLES

### Example 1
```powershell
Remove-SPOTenantApplyFileVersionPolicyJob
```

Example 1 cancels further processing of the tenant apply file version policy job.

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

[New-SPOTenantApplyFileVersionPolicyJob](New-SPOTenantApplyFileVersionPolicyJob.md)

[Get-SPOTenantApplyFileVersionPolicyJobProgress](Get-SPOTenantApplyFileVersionPolicyJobProgress.md)

[SharePoint Advanced Management](/sharepoint/sharepoint-advanced-management-licensing)
