---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainer
applicable: SharePoint Online
title: New-SPOContainerType
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# New-SPOContainerType

## SYNOPSIS

Creates a new ContainerType in a SharePoint Embedded application. 

## SYNTAX

### ParamSet1

```powershell
New-SPOContainerType -ContainerTypeName [<ContainerTypeName>] -OwningApplicationId [<OwningApplicationId>] -AzureSubscriptionId [<AzureSubscriptionId>] -ResourceGroup [<ResourceGroup>] -Region [<Region>]​ [<CommonParameters>]
```

### ParamSet2
```powershell
New-SPOContainerType –TrialContainerType -ContainerTypeName [<ContainerTypeName>] -OwningApplicationId [<OwningApplicationId>]
```
 
## DESCRIPTION

The `New-SPOContainerType` cmdlet... <!-- TODO -->
This command is available only in SharePoint Online Management Shell version 16.0.24211.12000 or higher to run this cmdlet.

You must be a SharePoint Online Administrator or Global Administrator to run this cmdlet.


## EXAMPLES

### Example 1

```powershell
New-SPOContainerType -ContainerTypeName [<ContainerTypeName>] -OwningApplicationId [<OwningApplicationId>] -AzureSubscriptionId [<AzureSubscriptionId>] -ResourceGroup [<ResourceGroup>] -Region [<Region>]​ [<CommonParameters>]
```

Example 1  

### Example 2

```powershell
New-SPOContainerType –TrialContainerType -ContainerTypeName [<ContainerTypeName>] -OwningApplicationId [<OwningApplicationId>]
```

Example 2  

 
 

## PARAMETERS

### -ContainerTypeName <!-- TODO -->

This parameter names your ContainerType for your SharePoint Embedded Application
 
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

### -OwningApplicationId <!-- TODO -->

Use this parameter to specify the Container in the given OwningApplicationId.
 
```yaml
Type: String
Parameter Sets: ParamSet4, ParamSet5
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureSubscriptionId <!-- TODO -->

This parameter can be used when there are more than 5,000 Containers in a given SharePoint Embedded application. Using `-Paged` will provide a `<Paging Token>` that will display the next 5,000 Containers.

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


### -ResourceGroup <!-- TODO -->

Use this parameter to provide the `<Paging Token>` provided to view the remaining Containers as shown in Example 5. If there are no more Containers to display, the commandlet output will return the message `End of Containers view.` Otherwise, use the given `<Paging Token>` to retrieve the next batch of up to 5,000 ontainers.

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

### -Region <!-- TODO -->

Use this parameter to provide the `<Paging Token>` provided to view the remaining Containers as shown in Example 5. If there are no more Containers to display, the commandlet output will return the message `End of Containers view.` Otherwise, use the given `<Paging Token>` to retrieve the next batch of up to 5,000 ontainers.

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

###  –TrialContainerType <!-- TODO -->
Use this parameter to provide the `<Paging Token>` provided to view the remaining Containers as shown in Example 5. If there are no more Containers to display, the commandlet output will return the message `End of Containers view.` Otherwise, use the given `<Paging Token>` to retrieve the next batch of up to 5,000 ontainers.

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


### CommonParameters 

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

