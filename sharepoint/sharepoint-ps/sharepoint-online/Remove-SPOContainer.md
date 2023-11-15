---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: 
applicable: SharePoint Online
title: Remove-SPOContainer
schema: 2.0.0
author: cindy-lay
ms.author: cindylay
ms.reviewer:
---


# Remove-SPOContainer

## SYNOPSIS
When admins delete a Container, it is moved into the deleted container collection. A deleted container can be restored from the collection within 93 days. If a container is deleted from the collection, or it exceeds the 93-day retention period, it is permanently deleted.Deleting a container deletes everything within it, including all documents and files.


## SYNTAX


## List of Containers 

### ParamSet1

```powershell
Remove-SPOContainer [–Identity <ContainerID>​]
```


## DESCRIPTION

The `Remove-SPOContainer` cmdlet removes a container and puts it in the recycle bin. You need to be a SharePoint Online administrator or Global Administrator to run the cmdlet.


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
Remove-SPOContainer -Identity 423poi45-jikl-9bnm-b302-1234ghy56789 -Identity https://contoso.sharepoint.com/storageContainers/CSP_b66f5b2e-4cbd-4754-9ad3-8291c2c81ade 
```

Example 3 gives the detailed properties of a container using site URL of a container.


## PARAMETERS

### -Identity

Use this parameter to specify the Container in the given tenant
 
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



### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).


## NOTES

## RELATED LINKS
[Restore-SPODeletedContainer](./Restore-SPODeletedContainer.md)
[Remove-SPODeletedContainer](./Remove-SPODeletedContainer.md)