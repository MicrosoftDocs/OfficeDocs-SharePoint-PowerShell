---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spocontainertype
applicable: SharePoint Online
title: Remove-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
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
 
This cmdlet deletes only the trial container type in the tenant. To delete a container type in trial status, you must remove all containers of the container type first, including from the deleted container collection. To remove containers, refer to [Remove-SPOContainer](./Remove-SPOContainer.md). Once all the containers are deleted, trial container type can be deleted using this cmdlet.

You must be a SharePoint Embedded Administrator to run this cmdlet.
 
## EXAMPLES
 
### Example 1
 
```powershell
Remove-SPOContainerTypeId -ContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604a8
```
In Example 1, the cmdlet asks for a confirmation on the remove action and on confirmation, deletes the trial container type.

Example 1 places the container with the given ID into the recycle bin. The container will be permanently deleted from the recycle bin after 93 days unless the deleted container is [restored](./Restore-SPODeletedContainer.md) before permanent deletion.
 
## PARAMETERS
 
### -ContainerTypeId
 
This parameter specifies the ID of the container type corresponding to the SharePoint Embedded application. Use the `Get-SPOContainertype` command to retrieve the ID.
 
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

[New-SPOContainerType](./New-SPOContainerType.md)

[Set-SPOContainerType](./Set-SPOContainerType.md)

[Remove-SPOContainerType](./Get-SPOContainerType.md)

