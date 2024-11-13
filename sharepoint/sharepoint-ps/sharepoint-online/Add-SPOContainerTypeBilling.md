---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spocontainertypebilling
applicable: SharePoint Online
title: Get-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Add-SPOContainerTypeBilling

## SYNOPSIS

Adds the mentioned billing profile details to a standard container type. 

## SYNTAX

### ParamSet1

```powershell
Add-SPOContainerTypeBilling [–ContainerTypeId <ContainerTypeId>] [-AzureSubscriptionId <AzureSubscriptionId>] [-ResourceGroup <ResourceGroup>] [-Region <Region>] 
```


## DESCRIPTION

This cmdlet attaches the Azure subscription ID, resource group and region with the container type ID provided.

You must be a SharePoint Embedded Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Add-SPOContainerTypeBilling - ContainerTypeId aa1d89b3-b4cf-4c0a-8e1c-0d131c57544a -AzureSubscriptionId 5a8a4d9f-9f8d-4cac-8a97-28ab04ff194c -ResourceGroup "RG100" -Region "(US) East US“ 
```

Example 1 attaches the billing profile of Azure subscription ID “5a8a4d9f-9f8d-4cac-8a97-28ab04ff194c”, resource group “RG100” and region “(US) East US” to the container type ID “aa1d89b3-b4cf-4c0a-8e1c-0d131c57544a” 


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

### -AzureSubscriptionId

This parameter describes the Azure subscription ID to which the container type needs to be associated.

```yaml
Type: String
Parameter Sets: 
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### -ResourceGroup

This parameter describes the resource group to be used for the associated container type.

```yaml
Type: String
Parameter Sets: 
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region

This parameter describes the region to which the billing profile of the container type is associated with.

```yaml
Type: String
Parameter Sets: ParamSet2, ParamSet3
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[New-SPOContainerType](./New-SPOContainerType.md)

[Get-SPOContainerType](./Get-SPOContainerType.md)

[Set-SPOContainerType](./Set-SPOContainerType.md)

[Remove-SPOContainerType](./Remove-SPOContainerType.md)
