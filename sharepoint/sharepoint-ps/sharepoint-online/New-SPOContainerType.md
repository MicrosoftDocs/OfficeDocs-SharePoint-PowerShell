
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

This cmdlet creates a new containertype of standard or trial status. The standard containertype can be created with the regular billing structure or direct to customer billing structure.

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

The New-SPOContainerType cmdlet creates a new containertype of the standard or trial status. A trial containertype does not have a billing profile associated with it and have a validity of 30 days. A standard containertype has a billing profile associated with it. With the use of -IsPassThroughBilling, we can create a direct to customer billed containertype.
This command is available only in SharePoint Online Management Shell version 16.0.24211.12000 or higher to run this cmdlet.

You must be a SharePoint Online Administrator or Global Administrator to run this cmdlet.


## EXAMPLES

### Example 2

```powershell
New-SPOContainerType -ContainerTypeName ContosoLegal -OwningApplicationId a735e4af-b86e-0000-93ba-1faded6c39e1 -AzureSubscriptionId 564e9025-f7f5-xxx9-9ddd-4cdxxxx1755 -ResourceGroup prod-resources -Region EastUS
```
Example output of the New-SPOContainerType cmdlet
```powershell
Are you sure you want to perform this action?
Performing the operation "New-SPOContainerType".
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y
ContainerTypeId     : 4f0af585-8dcc-0000-223d-661eb2c604e4
ContainerTypeName   : ContosoLegal
OwningApplicationId : a735e4af-b86e-0000-93ba-1faded6c39e1
AzureSubscriptionId : 564e9025-f7f5-xxx9-9ddd-4cdxxxx1755
ResourceGroup       : prod-resources
Region              : EastUS
Classification      : Standard
CreationDate        : 7/2/2024
ExpiryDate          : 
```

Example 2  
```powershell
New-SPOContainerType –TrialContainerType - ContosoLegal -OwningApplicationId a735e4af-b86e-0000-93ba-1faded6c39e1
```

Example output of the New-SPOContainerType cmdlet

```powershell
Are you sure you want to perform this action?
Performing the operation "New-SPOContainerType".
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y
ContainerTypeId                              ContainerTypeName          OwningApplicationId               Classification
------------------------------------        --------------------   -------------------------------        -----------------
4f0af585-8dcc-0000-223d-661eb2c604e4            ContosoLegal       a735e4af-b86e-0000-93ba-1faded6c39e1         Trial
```



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

###  –IsPassThroughBilling <!-- TODO -->
Use this parameter to provide create a direct to customer billed containertype
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
