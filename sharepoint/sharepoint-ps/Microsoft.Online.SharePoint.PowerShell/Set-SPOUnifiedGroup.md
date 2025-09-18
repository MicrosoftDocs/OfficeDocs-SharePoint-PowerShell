---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/set-spounifiedgroup
applicable: SharePoint Online
title: Set-SPOUnifiedGroup
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Set-SPOUnifiedGroup

## SYNOPSIS

Sets the Preferred Data Location (PDL) for the specified Office 365 Group. The customer tenant must be multi-geo enabled.

## SYNTAX

```
Set-SPOUnifiedGroup [-GroupAlias] <String> [-PreferredDataLocation] <String> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to set the Preferred Data Location for an Office 365 Group.

## EXAMPLES

### Example 1

```powershell
Set-SPOUnifiedGroup -GroupAlias EUTeam -PreferredDataLocation EUR
```

Sets the PDL for the Office 365 Group named 'EUTeam' to EUR (Europe).

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

### -PreferredDataLocation

> Applicable: SharePoint Online

The Preferred Data Location for the Office 365 Group.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOUnifiedGroup](/powershell/module/sharepoint-online/get-spounifiedgroup)

[Move a SharePoint site to a different geo location](/office365/enterprise/move-sharepoint-between-geo-locations)
