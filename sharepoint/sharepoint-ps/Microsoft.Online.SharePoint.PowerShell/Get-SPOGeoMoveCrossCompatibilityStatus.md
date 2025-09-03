---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spogeomovecrosscompatibilitystatus
applicable: SharePoint Online
title: Get-SPOGeoMoveCrossCompatibilityStatus
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Get-SPOGeoMoveCrossCompatibilityStatus

## SYNOPSIS

This cmdlet returns the compatibility status between geographic locations.

## SYNTAX

```
Get-SPOGeoMoveCrossCompatibilityStatus [<CommonParameters>]
```

## DESCRIPTION

This cmdlet returns the compatibility between sites and locations for a move in a multi-geo SharePoint Online tenant.
The following statuses can be returned:
- **Compatible** - The sites and locations are currently compatible and a move can be performed.
- **Incompatible** - The sites or locations are currently not compatible and a move cannot be performed at this point in time.
- **Warning** - The sites or locations are currently not compatible. Although a move can be performed, it is recommended to postpone until they are compatible.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOGeoMoveCrossCompatibilityStatus
```

Get the compatibility status for all locations.

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

[Get-SPOAppErrors](Get-SPOAppErrors.md)
