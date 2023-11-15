---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: 
applicable: SharePoint Online
title: Remove-SPOContainerDeletedContainer
schema: 2.0.0
author: cindy-lay
ms.author: cindylay
ms.reviewer:
---


# Remove-SPODeletedContainer



## SYNOPSIS

Permanently deletes the specified SharePoint repository services container from the recycle bin. This action cannot be undone.

## SYNTAX



### ParamSet1

```powershell
Remove-SPODeletedContainer [–Identity <ContainerID>] [<CommonParameters>]
```



## DESCRIPTION

The `Remove-SPODeletedContainer` cmdlet permanently removes a SharePoint repository services deleted container from the Recycle Bin.

You must be a SharePoint Administrator or Global Administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).




## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Remove-SPODeletedContainer –Identity ADD_ID_HERE!!
``````

This example removes a SharePoint repository services deleted container with the ContainerID from the Recycle Bin and deletes it permanently.


### -----------------------EXAMPLE 2-----------------------------

```powershell
Remove-SPODeletedContainer –Identity ADD_URL_HERE!!
``````

This example removes a SharePoint repository services deleted container with the ContainerURL from the Recycle Bin and deletes it permanently.


### -----------------------EXAMPLE 1-----------------------------

```powershell
Remove-SPODeletedContainer –Identity ADD_SiteURL_HERE!!
``````

This example removes a SharePoint repository services deleted container with the ContainerSiteURL from the Recycle Bin and deletes it permanently.



## PARAMETERS


### -Identity

Specifies the `<ContainerID>`, `<ContainerURL>`, or `<ContainerSiteURL>` of the Container to be permanently deleted.
 
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


### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).


## INPUTS


## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Remove-SPOContainer](./Remove-SPOContainer.md)

