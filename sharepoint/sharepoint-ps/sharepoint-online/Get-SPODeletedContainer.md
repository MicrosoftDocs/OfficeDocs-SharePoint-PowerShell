---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: 
applicable: SharePoint Online
title: GET-SPOContainerDeletedContainer
schema: 2.0.0
author: cindy-lay
ms.author: cindylay
ms.reviewer:
---


# Get-SPODeletedContainer


## SYNOPSIS

Returns a list of all containers that have been deleted and placed in the deleted container collection.


## SYNTAX



### ParamSet1

```powershell
Get-SPODeletedContainer [<CommonParameters>]
```



## DESCRIPTION

The `Get-SPODeletedContainer` cmdlet returns a list of all containers that were deleted and live in the deleted container collection. This includes the `ContainerId`, `ContainerName`, and `CreatedDate`.

You must be a SharePoint Administrator or Global Administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).




## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```ps
Get-SPODeletedContainer
```

This example returns a list of the `ContainerId`, `ContainerName`, and `CreatedDate` of all containers in the deleted container collection.


## PARAMETERS



### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).


## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Get-SPOContainer](Get-SPOContainer.md)

[Remove-SPOContainer](Remove-SPOContainer.md)

