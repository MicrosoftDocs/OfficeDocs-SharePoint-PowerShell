---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
applicable: SharePoint Online
title: Get-SPOContainer
schema: 2.0.0
author: akanksha-rakesh, cindy-lay
ms.author: arakesh, cindylay
ms.reviewer:
---

# Get-SPOContainer

## SYNOPSIS

Returns one or more containers in the SharePoint repository services application. 

## SYNTAX


## List of Containers 

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

## Container Details

### ParamSet4

```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>] [[-Identity] <ContainerId>]
```


### ParamSet5

```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>] [[-Identity] <ContainerSiteURL>]  
```

## DESCRIPTION

The `Get-SPOContainer` cmdlet retrieves and returns a list of containers and details of an individual container created under a SharePoint repository services application. This command is available only in SharePoint Online Management Shell version 16.0.24211.12000 or higher to run this cmdlet.

You need to be a SharePoint Online administrator or Global Administrator to run this cmdlet.

> [!NOTE]  
> Containers in the Recycle Bin will not be retrieved by using the [`Get-SPOContainer`](./Get-SPOContainer.md) cmdlet. 


> [!NOTE]
> The OwningApplicationId for Microsoft Loop is `a187e399-0c36-4b98-8f04-1edc167a0996`

> The OwningApplicationId for Microsoft Designer is `5e2795e3-ce8c-4cfb-b302-35fe5cd01597`
 
 

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPOContainer -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 | FT 
```

Example 1 returns a tabular list of containers created under the SharePoint repository services application.

To retrieve containers for the Loop app, use OwningApplicationId: `a187e399-0c36-4b98-8f04-1edc167a0996`. 

To retrieve containers for the Designer app, use OwningApplicationId: `5e2795e3-ce8c-4cfb-b302-35fe5cd01597`.

To retrieve ApplicationID of other SharePoint repository services applications registered your tenant, use Get-SPOApplication command. 

### -----------------------EXAMPLE 2-----------------------------

```powershell
Get-SPOContainer -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 -Identity b66f5b2e-4cbd-4754-9ad3-8291c2c81ade 
```

Example 2 returns the detailed properties of the container with associated `ContainerId`.

 
### -----------------------EXAMPLE 3-----------------------------

```powershell
Get-SPOContainer -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 -Identity https://contoso.sharepoint.com/storageContainers/CSP_b66f5b2e-4cbd-4754-9ad3-8291c2c81ade 
```

Example 3 gives the detailed properties of a container using site URL of a container.


### -----------------------EXAMPLE 4-----------------------------

```powershell
Get-SPOContainer -OwningApplicationId <OwningApplicationId> -Identity <ContainerId> -Paged | FT
```

Example 4 Uses the `-Paged` command to retrieve a paging token.

### -----------------------EXAMPLE 5-----------------------------

```powershell
Get-SPOContainer -OwningApplicationId <OwningApplicationId> -Identity <ContainerId> -Paged -PagingToken <Token String> | FT 
```

Example 5 uses the `PagingToken` to view more containers.

## PARAMETERS

### -OwningApplicationId

This parameter specifies the ID of the SharePoint repository services Application. Use `Get-SPOApplication` command to retrive OwningApplicationId.
 
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

This parameter can be used when there are more than 5000 containers in a given application. `-Paged` provides a `<Paging Token>` that will display 5000 containers at a time.

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


If there are no more containers to display, the commandlet output will return the message `End of containers view.` Otherwise, the commandlet will return a `<Paging Token>` to retrieve the next set of 5000 containers.

## Using the Paging Token

### -PagingToken

Use the <Paging Token> 

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

[Getting started with SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Get-SPOApplication](./Get-SPOApplication.md)


