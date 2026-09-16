---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: microsoft.online.sharepoint.powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spetenantapplyfileversionpolicyjobprogress
applicable: SharePoint Online
title: Get-SPETenantApplyFileVersionPolicyJobProgress
schema: 2.0.0
author: guptapriyan
ms.author: guptapriyan
ms.reviewer:
manager: srikrg
---

# Get-SPETenantApplyFileVersionPolicyJobProgress

## SYNOPSIS

Gets the status for an apply file version policy job for a SharePoint Embedded (SPE) container type. SharePoint Advanced Management license or Copilot license is required to run this cmdlet.

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

## SYNTAX

```
Get-SPETenantApplyFileVersionPolicyJobProgress -ContainerTypeId <Guid> [<CommonParameters>]
```

## DESCRIPTION

Gets the status for an apply file version policy job that was queued for the specified SharePoint Embedded (SPE) container type.

## EXAMPLES

### Example 1
```powershell
Get-SPETenantApplyFileVersionPolicyJobProgress -ContainerTypeId <ContainerTypeId>
```

Example 1 gets the status for the apply file version policy job of the specified container type.

## PARAMETERS

### -ContainerTypeId
The ID of the SharePoint Embedded container type whose job status is retrieved.

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

### CommonParameters
This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-SPETenantApplyFileVersionPolicyJob](New-SPETenantApplyFileVersionPolicyJob.md)

[Remove-SPETenantApplyFileVersionPolicyJob](Remove-SPETenantApplyFileVersionPolicyJob.md)

[SharePoint Advanced Management](/sharepoint/sharepoint-advanced-management-licensing)

[Microsoft 365 Copilot](/microsoft-365/copilot/microsoft-365-copilot-licensing)
