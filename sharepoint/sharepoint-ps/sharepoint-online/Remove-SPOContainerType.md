---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainertype
applicable: SharePoint Online
title: Remove-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: ShreyasSar26
ms.reviewer:
---

# Remove-SPOContainerType

## SYNOPSIS
This cmdlet removes the containertype specified from the tenant. 

## SYNTAX

### ParamSet1

```powershell
Remove-SPOContainerType -ContainerTypeId <ContainerTypeId>
```
<!-- TODO -->

## DESCRIPTION

The Remove-SPOContainerType cmdlet deletes only the trial containertype in the tenant. To delete a container type in trial status, you must remove all containers of the container type first, including from the deleted container collection. To remove containers, refer to Consuming Tenant Admin. Once all the containers are deleted, trial containertype can be deleted using the PowerShell cmdlet.
You must be a SharePoint Online Administrator or Global Administrator to run this cmdlet.

## EXAMPLES

### Example 1

```powershell
Remove-SPOContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604a8
```
Example output of the Remove-SPOContainerType cmdlet
```powershell
Are you sure you want to perform this action?
Performing the operation "Remove-SPOContainerType".
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y
Success 
Trial container type is deleted.
```
Example 1 places the Container with the `ContainerId` `4f0af585-8dcc-0000-223d-661eb2c604a8` into the Recycle Bin. The Container will be permanently deleted from the Recycle Bin after 93 days unless the deleted Container is [restored](./Restore-SPODeletedContainer.md) before permanent deletion. 

## PARAMETERS

### -ContainerTypeId

This parameter specifies the ID of the containertype corresponding to the SharePoint Embedded application. Use the Get-SPOContainertype command to retrieve the ContainerTypeId.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).
