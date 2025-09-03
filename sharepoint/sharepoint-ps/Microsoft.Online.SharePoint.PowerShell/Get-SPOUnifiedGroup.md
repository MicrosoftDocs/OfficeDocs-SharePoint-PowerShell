---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spounifiedgroup
applicable: SharePoint Online
title: Get-SPOUnifiedGroup
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
ms.date: 07/15/2025
---

# Get-SPOUnifiedGroup

## SYNOPSIS

Retrieves the Preferred Data Location for the specified Office 365 Group.

## SYNTAX

```
Get-SPOUnifiedGroup [-GroupAlias] <String> [<CommonParameters>]
```

## DESCRIPTION

Retrieves the Preferred Data Location (PDL) for the specified Office 365 Group. The customer tenant must be multi-geo enabled.

## EXAMPLES

### Example 1

```powershell
Get-SPOUnifiedGroup -GroupAlias EUTeam
```
Returns the PDL for the Office 365 Group named 'EUTeam'.

## PARAMETERS

### -GroupAlias

> Applicable: SharePoint Online

The alias of the Office 365 Group.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Move a SharePoint site to a different geo location](/office365/enterprise/move-sharepoint-between-geo-locations)
