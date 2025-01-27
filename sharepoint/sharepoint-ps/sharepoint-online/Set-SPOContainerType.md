---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spocontainertype
applicable: SharePoint Online
title: Set-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---
 
# Set-SPOContainerType
 
## SYNOPSIS
 
Sets or updates one or more property values of a trial or standard container type.
 
## SYNTAX
 
### ParamSet1
 
```powershell
Set-SPOContainerType -ContainerTypeId <ContainerTypeId> -OwningApplicationId <OwningApplicationId> -ContainerTypeName <ContainerTypeName>
```
### ParamSet2
```powershell
Set-SPOContainerType -ContainerTypeId <ContainerTypeId> -AzureSubscriptionId <AzureSubscriptionId> -ResourceGroup <ResourceGroup>
```
 
## DESCRIPTION
This cmdlet is used to reset the parameters associated with a container type - both trial and standard. The cmdlet can be used to change the basic information of a container type such as container type name, owning application ID or the billing information of the container type.

You must be a SharePoint Embedded Administrator to run the cmdlet.

While you only need to be a SharePoint Embedded Administrator to change the basic information of a container type, you need owner or contributor access on the existing billing subscription associated with the container type and also on the new billing subscription, to change the billing information of the container type. 

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES
 
### Example 1
 
```powershell
Set-SPOContainerType -ContainerTypeId da1d89b3-b4cf-4c0a-8e1c-0d131c57544f -OwningApplicationId 12a9d93c-18d7-46a0-b43e-28d20addd56a - ContainerTypeName 'Red Container Type' 
```
 
Example 1 sets the container type name as 'Red Container Type'

 
### Example 2
 
```powershell
Set-SPOContainerType -ContainerTypeId da1d89b3-b4cf-4c0a-8e1c-0d131c57544f –Azure Subscription 12a9d93c-18d7-46a0-b43e-28d20addd56a -ResourceGroup RG200
```
 
In Example 2, the billing profile of the container type is updated.

### Example 3
 
```powershell
Set-SPOContainerType -ContainerTypeId 01f62754-0873-4ec6-ab4a-3eed48ba8be7 -OwningApplicationId 994b9586-253e-4a77-b51 - ContainerTypeName 'Blue Container Type' 
```
In Example 3, the trial container type name is updated as 'Blue Container Type' 


 
## PARAMETERS
 

### -ContainerTypeName

This parameter names your container type for your SharePoint Embedded application.

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

### -OwningApplicationId

This parameter specifies the ID of the SharePoint Embedded application.  

```yaml
Type: String
Parameter Sets: 
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
Parameter Sets: (All)
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
## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[New-SPOContainerType](./New-SPOContainerType.md)

[Get-SPOContainerType](./Get-SPOContainerType.md)

[Remove-SPOContainerType](./Remove-SPOContainerType.md)
