---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainer
applicable: SharePoint Online
title: Get-SPOContainer
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# Get-SPOContainer

## SYNOPSIS

Returns one or more Containers in a SharePoint repository services application. 

## SYNTAX

### ParamSet1

```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>] [<CommonParameters>]
```

### ParamSet2
```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>] [-Paged]
```

### ParamSet3
```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>] [-Paged] [-PagingToken <Token String>]
```

### ParamSet4

```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>] [[-Identity] <ContainerId>]
```

### ParamSet5

```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>] [[-Identity] <ContainerSiteURL>]  
```

## DESCRIPTION

The `Get-SPOContainer` cmdlet retrieves and returns a list of Containers and details of an individual Container created under a SharePoint repository services application. This command is available only in SharePoint Online Management Shell version 16.0.24211.12000 or higher to run this cmdlet.

You must be a SharePoint Online Administrator or Global Administrator to run this cmdlet.

> [!NOTE]  
> Containers in the Recycle Bin will not be retrieved by using the `Get-SPOContainer` cmdlet. 
> The OwningApplicationId for Microsoft Loop is `a187e399-0c36-4b98-8f04-1edc167a0996`.
> The OwningApplicationId for Microsoft Designer is `5e2795e3-ce8c-4cfb-b302-35fe5cd01597`.

## EXAMPLES

### Example 1

```powershell
Get-SPOContainer -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 | FT 
```

Example 1 returns a tabular list of Containers created under the SharePoint repository services application with the `OwningApplicationId` of  `423poi45-jikl-9bnm-b302-1234ghy56789`.

To retrieve Containers for the Microsoft Loop app, use OwningApplicationId: `a187e399-0c36-4b98-8f04-1edc167a0996`. 

To retrieve Containers for the Microsoft Designer app, use OwningApplicationId: `5e2795e3-ce8c-4cfb-b302-35fe5cd01597`.

### Example 2

```powershell
Get-SPOContainer -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 -Identity b66f5b2e-4cbd-4754-9ad3-8291c2c81ade 
```

Example 2 returns the detailed properties of the Container with associated `ContainerId`.

 
### Example 3

```powershell
Get-SPOContainer -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 -Identity https://contoso.sharepoint.com/storagecontainers/CSP_b66f5b2e-4cbd-4754-9ad3-8291c2c81ade 
```

Example 3 gives the detailed properties of a Container using the site URL of a Container.

### Example 4

```powershell
Get-SPOContainer -OwningApplicationId <OwningApplicationId> -Identity <ContainerId> -Paged | FT
```

Example 4 uses the `-Paged` command to retrieve a paging token.

### Example 5

```powershell
Get-SPOContainer -OwningApplicationId <OwningApplicationId> -Identity <ContainerId> -Paged -PagingToken <Token String> | FT 
```

Example 5 uses the `PagingToken` to view more Containers.

## PARAMETERS

### -OwningApplicationId

This parameter specifies the ID of the SharePoint repository services application. Use the `Get-SPOApplication` command to retrieve the OwningApplicationId.
 
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

### -Identity

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

### -Paged

This parameter can be used when there are more than 5,000 Containers in a given SharePoint repository services application. Using `-Paged` will provide a `<Paging Token>` that will display the next 200 Containers.

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


### -PagingToken

Use this parameter to provide the `<Paging Token>` provided to view the remaining Containers as shown in Example 5. If there are no more Containers to display, the commandlet output will return the message `End of Containers view.` Otherwise, use the given `<Paging Token>` to retrieve the next batch of up to 200 containers.

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

