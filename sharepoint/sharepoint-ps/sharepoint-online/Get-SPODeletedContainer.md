---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spodeletedcontainer
applicable: SharePoint Online
title: Get-SPODeletedContainer
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# Get-SPODeletedContainer

## SYNOPSIS

Returns all deleted Containers in the Recycle Bin.

## SYNTAX

### ParamSet1

```powershell
Get-SPODeletedContainer [<CommonParameters>]
```

## DESCRIPTION

The `Get-SPODeletedContainer` cmdlet returns a list of all deleted File Storage Containers in the Recycle Bin. There is no `Identity` parameter needed. The list includes the `ContainerId`, `ContainerName`, and `CreatedDate`. Deleted Containers in the Recycle Bin are permanently deleted after 93 days. More details in [`Remove-SPOContainer`](./Remove-SPOContainer.md). You can restore a deleted Container with the cmdlet [`Restore-SPODeletedContainer`](./Restore-SPODeletedContainer.md).

You must be a SharePoint Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).

## EXAMPLES

### Example 1

```ps
Get-SPODeletedContainer
```

This example returns a list of the `ContainerId`, `ContainerName`, and `CreatedDate` of all deleted Containers in the Recycle Bin. 


## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Get-SPOContainer](Get-SPOContainer.md)

[Remove-SPOContainer](Remove-SPOContainer.md)

