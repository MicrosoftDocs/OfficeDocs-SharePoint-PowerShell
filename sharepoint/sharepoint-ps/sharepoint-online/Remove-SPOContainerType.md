---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spocontainertype
applicable: SharePoint Online
title: Remove-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: ShreyasSar26
ms.reviewer:
---
 
# Remove-SPOContainerType
 
## SYNOPSIS
This cmdlet removes the container type specified from the tenant.
 
## SYNTAX
 
### ParamSet1
 
```powershell
Remove-SPOContainerType -ContainerTypeId <ContainerTypeId>
```
 
## DESCRIPTION
 
This cmdlet deletes only the trial container type in the tenant. To delete a container type in trial status, you must remove all containers of the container type first, including from the deleted container collection. To remove containers, refer to Consuming Tenant Admin. Once all the containers are deleted, trial containertype can be deleted using the PowerShell cmdlet.
You must be a SharePoint Embedded Administrator to run this cmdlet.
 
## EXAMPLES
 
### Example 1
 
```powershell
Remove-SPOContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604a8
```
In Example 1, the cmdlet asks for a confirmation on the remove action and on confirmation, deletes the trial container type

Example 1 places the container with the `ContainerId` `4f0af585-8dcc-0000-223d-661eb2c604a8` into the Recycle Bin. The Container will be permanently deleted from the Recycle Bin after 93 days unless the deleted Container is [restored](./Restore-SPODeletedContainer.md) before permanent deletion.
 
## PARAMETERS
 
### -ContainerTypeId
 
This parameter specifies the ID of the container type corresponding to the SharePoint Embedded application. Use the 'Get-SPOContainertype' command to retrieve the ContainerTypeId.
 
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
## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[New-SPOContainerType](sharepoint/sharepoint-ps/sharepoint-online/New-SPOContainerType.md)

[Set-SPOContainerType](sharepoint/sharepoint-ps/sharepoint-online/Set-SPOContainerType.md)

[Remove-SPOContainerType](sharepoint/sharepoint-ps/sharepoint-online/Get-SPOContainerType.md)

