---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spohidedefaultthemes
applicable: SharePoint Online
title: Get-SPOHideDefaultThemes
schema: 2.0.0
author: trent-green
ms.author: speedta
ms.reviewer:
---

# Get-SPOHideDefaultThemes

## SYNOPSIS

Queries the current SPOHideDefaultThemes setting. SPO stands for SharePoint Online.

## SYNTAX

```
Get-SPOHideDefaultThemes [<CommonParameters>]
```

## DESCRIPTION

The **Get-SPOHideDefaultThemes** cmdlet retrieves the current **Set-SPOHideDefaultThemes** setting. You might want to use this cmdlet in a PowerShell script to read the setting and then take different actions based on whether the default themes are hidden. This cmdlet does not have any parameters.

> [!NOTE]
> This cmdlet was named **Get-HideDefaultThemes** until the December 2017 release of the SPO Management Shell. We recommend that you use the latest version of the PowerShell cmdlets.

## EXAMPLES

### Example 1

```powershell
Get-SPOHideDefaultThemes
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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Set-SPOHideDefaultThemes](Set-SPOHideDefaultThemes.md)
