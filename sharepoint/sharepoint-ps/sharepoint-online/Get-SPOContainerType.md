---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainertype
applicable: SharePoint Online
title: Get-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Get-SPOContainerType

## SYNOPSIS

Returns one or more container types created in the tenant. 

## SYNTAX

### ParamSet1

```powershell
Get-SPOContainerType 
```
### ParamSet2
```powershell
Get-SPOContainerType [-ContainerTypeId <ContainerTypeId>] 
```

## DESCRIPTION

This cmdlet returns all the container types present in the tenant or details of a specific container type when paired with the containertype ID parameter. 

You must be a SharePoint Embedded administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Get-SPOContainerType 
```

Example 1 retrieves all the container types present in the tenant and displays container type specific information.

### Example 2

```powershell
Get-SPOContainerType -ContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604e4 
```
Example 2 returns the detailed properties of container type 4f0af585-8dcc-0000-223d-661eb2c604e4 

## PARAMETERS

### -ContainerTypeId
 
This parameter specifies the ID of the container type corresponding to the SharePoint Embedded application.
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

[Remove-SPOContainerType](./Remove-SPOContainerType.md)
