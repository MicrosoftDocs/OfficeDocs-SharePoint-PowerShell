---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spolistversionpolicy
applicable: SharePoint Online
title: Get-SPOListVersionPolicy
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Get-SPOListVersionPolicy

## SYNOPSIS

Gets the version policy setting on the document library.

## SYNTAX

```powershell
Get-SPOListVersionPolicy [-Site] <SpoSitePipeBind> [-List] <SpoListPipeBind> [<CommonParameters>]
```

## DESCRIPTION

Gets the version policy setting on the document library.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents"
```

Example 1 gets the version policy setting on the document library called "Documents".

## PARAMETERS

### -Site

Specifies the URL of the site.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -List

The document library name or Id.

```yaml
Type: SPOListPipeBind
Parameter Sets: (All)

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Set-SPOListVersionPolicy](Set-SPOListVersionPolicy.md)
