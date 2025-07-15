---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spoorgassetslibrary
applicable: SharePoint Online
title: Get-SPOOrgAssetsLibrary
author: Maralesfahanpoor
ms.author: maesfaha
ms.reviewer:
manager: paulac
schema: 2.0.0
---

# Get-SPOOrgAssetsLibrary

## SYNOPSIS

Displays information about all libraries designated as locations for organization assets.

## SYNTAX

```
Get-SPOOrgAssetsLibrary [<CommonParameters>]
```

## DESCRIPTION

The Get-SPOOrgAssetsLibrary cmdlet displays information about all libraries designated as locations for organization assets.

Once this cmdlet is run, it will display the name and URL of the site where assets are originally stored, as well as the display name, server relative library URL, list ID, OrgAssetType and thumbnail URL for any associated libraries.

## EXAMPLES

### Example 1

This example displays the name and URL of the site where assets are originally stored. It also provides a list of any associated libraries and shows the respective display name, server relative library URL, list ID, OrgAssetType and thumbnail URL.

```powershell
Get-SPOOrgAssetsLibrary
```

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/add-spoorgassetslibrary)

[Set-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/set-spoorgassetslibrary)

[Remove-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/remove-spoorgassetslibrary)
