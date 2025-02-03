---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/new-spocontainertype
applicable: SharePoint Online
title: New-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# New-SPOContainerType

## SYNOPSIS

This cmdlet creates a new container type of standard or trial status. The standard container type can be created with the regular billing structure or direct to customer billing structure.

## SYNTAX

### ParamSet1

```powershell
New-SPOContainerType [-ContainerTypeName] <String> [-OwningApplicationId] <String> [-ApplicationRedirectUrl] <String> [<CommonParameters>]
```

### ParamSet2

```powershell
New-SPOContainerType [-ContainerTypeName] <String> [-OwningApplicationId] <String> [-ApplicationRedirectUrl] <String> [-IsPassThroughBilling] [<CommonParameters>]
```

### ParamSet3
```powershell
New-SPOContainerType [–TrialContainerType] [-ContainerTypeName] <String> [-OwningApplicationId] <String> [-ApplicationRedirectUrl] <String> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new standard or trial container type. A standard container type, by definition, has a billing profile associated with it and can be either regular billed or direct to consumer billed. A trial container type does not have a billing profile. In case of regular billing, the next step after creation is the addition of a billing profile using the [Add-SPOContainerTypeBilling](./Add-SPOContainerTypeBilling.md) cmdlet. With the use of `-IsPassThroughBilling`, you can create a direct to customer billed container type. There is no need to attach a billing profile in case this case. `–TrialContainerType` when used creates a trial container type that has a validity of 30 days. 

You must be a SharePoint Embedded Administrator to run this cmdlet.


## EXAMPLES

### Example 1

```powershell
New-SPOContainerType -ContainerTypeName ContosoLegal -OwningApplicationId a735e4af  
```
In Example 1, the cmdlet creates a new regular billed container type ContosoLegal.

### Example 2  
```powershell
New-SPOContainerType –IsPassThroughBilling –ContainerTypeName ContosoLegal -OwningApplicationId a735e4af
```

In Example 2, the cmdlet creates a direct to customer billed container type ContosoLegal. 

### Example 3   

```powershell 

New-SPOContainerType –TrialContainerType -ContainerTypeName ContosoLegal -OwningApplicationId a735e4af

``` 

In Example 3, the cmdlet creates a trial container type, ContosoLegal, valid for 30 days. 

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

[Add-SPOContainerTypeBilling](./Add-SPOContainerTypeBilling.md)

[Get-SPOContainerType](./Get-SPOContainerType.md)

[Set-SPOContainerType](./Set-SPOContainerType.md)

[Remove-SPOContainerType](./Remove-SPOContainerType.md)
