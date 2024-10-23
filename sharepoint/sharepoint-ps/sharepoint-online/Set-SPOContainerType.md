---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spocontainertype
applicable: SharePoint Online
title: Set-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: ShreyasSar26
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
This cmdlet is used to reset the parameters associated with a container type - both trial and standard. The cmdlet can be used to change the container type name or the associated billing profile of the container type.
## EXAMPLES
 
### Example 1
 
```powershell
Set-SPOContainerType -ContainerTypeId DA1D89B3-B4CF-4C0A-8E1C-0D131C57544F -OwningApplicationId 12A9D93C-18D7-46A0-B43E-28D20ADDD56A - ContainerTypeName 'Red Container Type' 
```
 
Example 1 sets the container type name as 'Red Container Type'

 
### Example 2
 
```powershell
Set-SPOContainerType -ContainerTypeId DA1D89B3-B4CF-4C0A-8E1C-0D131C57544F –Azure Subscription 01F62754-0873-4EC6-AB4A-3EED48BA8BE7 -ResourceGroup RG200
```
 
In Example 2, the billing profile of the container type is updated with the latest information.

### Example 3
 
```powershell
Set-SPOContainerType -ContainerTypeId 01F62754-0873-4EC6-AB4A-3EED48BA8BE7 -OwningApplicationId 994B9586-253E-4A77-B51 - ContainerTypeName 'Blue Container Type' 
```
In Example 3, the trial container type name is updated as 'Blue Container Type' 


 
## PARAMETERS
 

### -ContainerTypeName

This parameter names your ContainerType for your SharePoint Embedded Application.

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

[New-SPOContainerType](sharepoint/sharepoint-ps/sharepoint-online/New-SPOContainerType.md)

[Get-SPOContainerType](sharepoint/sharepoint-ps/sharepoint-online/Get-SPOContainerType.md)

[Remove-SPOContainerType](sharepoint/sharepoint-ps/sharepoint-online/Remove-SPOContainerType.md)
