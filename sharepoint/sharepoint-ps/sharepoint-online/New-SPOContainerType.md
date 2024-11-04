---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/new-spocontainertype
applicable: SharePoint Online
title: New-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: ShreyasSar26
ms.reviewer:
---

# New-SPOContainerType

## SYNOPSIS

This cmdlet creates a new container type of standard or trial status. The standard container type can be created with the regular billing structure or direct to customer billing structure.

## SYNTAX

### ParamSet1

```powershell
New-SPOContainerType –ContainerTypeName <ContainerTypeName> -OwningApplicationId <OwningApplicationId> -AzureSubscriptionId <AzureSubscriptionId> -ResourceGroup <ResourceGroup> -Region <Region>
```

### ParamSet2

```powershell
New-SPOContainerType -ContainerTypeName <ContainerTypeName> -OwningApplicationId <OwningApplicationId> -IsPassThroughBilling
```

### ParamSet3
```powershell
New-SPOContainerType –TrialContainerType -ContainerTypeName <ContainerTypeName> -OwningApplicationId <OwningApplicationId>
```

## DESCRIPTION

This cmdlet creates a new container type of the standard or trial status. A trial container type does not have a billing profile associated with it and has a validity of 30 days. A standard container type has a billing profile associated with it. With the use of '-IsPassThroughBilling', we can create a direct to customer billed container type.

You must be a SharePoint Embedded Administrator to run this cmdlet.


## EXAMPLES

### Example 1

```powershell
New-SPOContainerType -ContainerTypeName ContosoLegal -OwningApplicationId a735e4af-b86e-0000-93ba-1faded6c39e1 -AzureSubscriptionId 564e9025-f7f5-xxx9-9ddd-4cdxxxx1755 -ResourceGroup prod-resources -Region EastUS
```
In Example 1, the cmdlet creates a new container type 'ContosoLegal' that is standard billed and is attached to the billing profile mentioned

### Example 2  
```powershell
New-SPOContainerType –TrialContainerType - ContosoLegal -OwningApplicationId a735e4af-b86e-0000-93ba-1faded6c39e1
```

In Example 2, the cmdlet creates a trial container type, 'ContosoLegal', valid for 30 days.

## PARAMETERS

### -ContainerTypeName

This parameter names your container type for your SharePoint Embedded Application.

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

###  –TrialContainerType
This parameter is used to specify that the cmdlet is used to create a trial container type and thereby the billing profile need not be provided.

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

###  –IsPassThroughBilling
This parameter is used to create a direct to customer billed container type.

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

[Get-SPOContainerType](sharepoint/sharepoint-ps/sharepoint-online/Get-SPOContainerType.md)

[Set-SPOContainerType](sharepoint/sharepoint-ps/sharepoint-online/Set-SPOContainerType.md)

[Remove-SPOContainerType](sharepoint/sharepoint-ps/sharepoint-online/Remove-SPOContainerType.md)
