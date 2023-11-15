---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
# online version: https://learn.microsoft.com/powershell/module/sharepoint-online/
applicable: SharePoint Online
title: Get-SPOContainer
schema: 2.0.0
author: cindy-lay
ms.author: cindylay
ms.reviewer:
---

# Get-SPOContainer

## SYNOPSIS

Returns one or more SharePoint repository services containers within the relevant tenant. 

## SYNTAX
<!-- 
Get-SPOSite [-Detailed] [-Filter <String>] [-IncludePersonalSite <Boolean>] [-Limit <String>]
 [-Template <String>] [-GroupIdDefined] [-ArchiveStatus <String>] [<CommonParameters>] -->

## List of Containers 

### ParamSet1

```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>]
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
 
You need to be a SharePoint Online administrator or Global Administrator to run the cmdlet.


> [!NOTE]  
> OwningApplicationID for Microsoft Loop is a187e399-0c36-4b98-8f04-1edc167a0996

> OwningApplicationID for Microsoft Designer is 5e2795e3-ce8c-4cfb-b302-35fe5cd01597
 
 
<!-- > [!NOTE]  
> Containers in the Recycle Bin will not be retrieved by using the Get-SPOContainer cmdlet.  -->

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPOContainer -OwningApplicationID 423poi45-jikl-9bnm-b302-1234ghy56789 | FT 
``````

Example 1 returns a tabular list of containers created under SharePoint repository services application  

To retrieve containers for the Loop app, use OwningApplicationId: a187e399-0c36-4b98-8f04-1edc167a0996 

To retrieve containers for the Designer app, use OwningApplicationId: 5e2795e3-ce8c-4cfb-b302-35fe5cd01597 

To retrieve ApplicationID of other SharePoint repository services applications registered your tenant, use Get-SPOApplication command. 

### -----------------------EXAMPLE 2-----------------------------

```powershell
Get-SPOContainer -OwningApplicationID 423poi45-jikl-9bnm-b302-1234ghy56789 -Identity b66f5b2e-4cbd-4754-9ad3-8291c2c81ade 
```

Example 2 gives the detailed properties of a container using the Identity of the container.  

 
### -----------------------EXAMPLE 3-----------------------------

```powershell
Get-SPOContainer -OwningApplicationID 423poi45-jikl-9bnm-b302-1234ghy56789 -Identity https://contoso.sharepoint.com/storageContainers/CSP_b66f5b2e-4cbd-4754-9ad3-8291c2c81ade 
```

Example 3 gives the detailed properties of a container using site URL of a container.


## PARAMETERS

### -OwningApplicationId

This parameter specifies the ID of the SharePoint repository services Application. Use `Get-SPOApplication` command to retrive OwningApplicationID
 
```yaml
Type: String
Parameter Sets: ParamSet1, ParamSet2, ParamSet3, ParamSet4, ParamSet5
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### -Identity

Use this parameter to specify the Container in the given OwningApplicationId
 
```yaml
Type: String
Parameter Sets: ParamSet4, ParamSet5
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### -Paged

This parameter can be used when there are more than 5000 containers in a given application. `-Paged` provides a `<Paging Token>` that will display 5000 containers at a time.

```yaml
Type: String
Parameter Sets: ParamSet1, ParamSet2, ParamSet3
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


```powershell
Get-SPOContainer -OwningApplicationID <OwningApplicationId> -Identity <ContainerId> -Paged | FT
```

If there are no more containers to display, the commandlet output will return the message `End of containers view.` Otherwise, the commandlet will return a `<Paging Token>` to retrieve the next set of 5000 containers.

## Using the Paging Token

### -PagingToken

Use the <Paging Token> 

```yaml
Type: String
Parameter Sets: <Paging Token
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```powershell
Get-SPOContainer -OwningApplicationID <OwningApplicationId> -Identity <ContainerId> -Paged -PagingToken <Token String> | FT 
```



### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

