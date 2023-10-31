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

Returns one or more SharePoint Embedded containers. 

## SYNTAX

### ParamSet1

```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>] [<commonParameters] 
```


### ParamSet2

```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>] [[-Identity] <ContainerId>]  
```

### ParamSet3

```powershell
Get-SPOContainer [-OwningApplicationId <OwningApplicationId>] [[-Identity] <ContainerSiteURL>]  
```

## DESCRIPTION

The `Get-SPOContainer` cmdlet retrieves and returns a list of containers and the properties of the containers present under a SharePoint Embedded application. This command is available only in SharePoint Online Management Shell Version <> or later. You need to be a SharePoint Online administrator or Global Administrator and be a site collection administrator to run the cmdlet.  



> [!NOTE]  
> To retrieve containers for the Microsoft Loop app, use OwningApplicationId : a187e399-0c36-4b98-8f04-1edc167a0996 

> To retrieve containers for the Microsoft Designer app, use 
OwningApplicationId: 5e2795e3-ce8c-4cfb-b302-35fe5cd01597 

> To retrieve ApplicationID of other SharePoint Embedded applications registered your tenant, use Get-SPOApplication command. 

> [!NOTE]  
> The command returns a maximum of 5000 container by default.  

 
> [!NOTE]  
> Containers in the Recycle Bin will not be retrieved by using the Get-SPOContainer cmdlet. 

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPOContainer -OwningApplicationID 423poi45-jikl-9bnm-b302-1234ghy56789 | FT 
``````

Example 1 returns a tabular list of containers created under SharePoint Embedded application  

To retrieve containers for the Loop app, use OwningApplicationId: a187e399-0c36-4b98-8f04-1edc167a0996 

To retrieve containers for the Designer app, use OwningApplicationId: 5e2795e3-ce8c-4cfb-b302-35fe5cd01597 

To retrieve ApplicationID of other SharePoint Embedded applications registered your tenant, use Get-SPOApplication command. 

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


### -Paged

Specifies the maximum number of site collections to return. It can be any number. To retrieve all site collections, use ALL. The default value is 5000. If this parameter is provided, then some site collection properties will not be populated and may contain a default value.

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


### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

