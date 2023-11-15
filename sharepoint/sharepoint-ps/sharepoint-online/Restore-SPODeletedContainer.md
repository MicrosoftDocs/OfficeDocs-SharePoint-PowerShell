---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: 
applicable: SharePoint Online
title: Recover-SPOContainer
schema: 2.0.0
author: cindy-lay
ms.author: cindylay
ms.reviewer:
---

# Restore-SPODeletedContainer​

## SYNOPSIS

Recovers the specified SharePoint repository services container from the Recycle Bin. 

## SYNTAX


### ParamSet1

```powershell
Restore-SPODeletedContainer [–Identity <ContainerID>​] [<CommonParameters>]
```

<!--
### ParamSet2
```powershell
Restore-SPODeletedContainer [-Identity <ContainerURL>]
```

### ParamSet3
```powershell
Restore-SPODeletedContainer [–Identity <ContainerSiteURL>]
```
-->

## DESCRIPTION

The `Restore-SPODeletedContainer` cmdlet recovers a container from the recycle bin. You need to be a SharePoint Online administrator or Global Administrator to run the cmdlet.


> [!NOTE]  
> OwningApplicationID for Microsoft Loop is a187e399-0c36-4b98-8f04-1edc167a0996

> OwningApplicationID for Microsoft Designer is 5e2795e3-ce8c-4cfb-b302-35fe5cd01597
 
 
<!-- > [!NOTE]  
> Containers in the Recycle Bin will not be retrieved by using the Remove-SPOContainer cmdlet.  -->

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Remove-SPOContainer -OwningApplicationID 423poi45-jikl-9bnm-b302-1234ghy56789 | FT 
``````

Example 1 returns a tabular list of containers created under SharePoint repository services application  

To retrieve containers for the Loop app, use OwningApplicationId: a187e399-0c36-4b98-8f04-1edc167a0996 

To retrieve containers for the Designer app, use OwningApplicationId: 5e2795e3-ce8c-4cfb-b302-35fe5cd01597 

To retrieve ApplicationID of other SharePoint repository services applications registered your tenant, use Remove-SPOApplication command. 

### -----------------------EXAMPLE 2-----------------------------

```powershell
Remove-SPOContainer -OwningApplicationID 423poi45-jikl-9bnm-b302-1234ghy56789 -Identity b66f5b2e-4cbd-4754-9ad3-8291c2c81ade 
```

Example 2 gives the detailed properties of a container using the Identity of the container.  

 
### -----------------------EXAMPLE 3-----------------------------

```powershell
Remove-SPOContainer -OwningApplicationID 423poi45-jikl-9bnm-b302-1234ghy56789 -Identity https://contoso.sharepoint.com/storageContainers/CSP_b66f5b2e-4cbd-4754-9ad3-8291c2c81ade 
```

Example 3 gives the detailed properties of a container using site URL of a container.


## PARAMETERS

### -OwningApplicationId

This parameter specifies the ID of the SharePoint repository services Application. Use `Remove-SPOApplication` command to retrive OwningApplicationID
 
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
Remove-SPOContainer -OwningApplicationID <OwningApplicationId> -Identity <ContainerId> -Paged | FT
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
Remove-SPOContainer -OwningApplicationID <OwningApplicationId> -Identity <ContainerId> -Paged -PagingToken <Token String> | FT 
```



### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).


## NOTES

## RELATED LINKS
[Get-SPODeletedContainer](./Get-SPODeletedContainer.md)
