---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spocrossgeousers
applicable: SharePoint Online
title: Get-SPOCrossGeoUsers
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Get-SPOCrossGeoUsers

## SYNOPSIS

Returns the SharePoint Online users in a multi-geo tenant that match the criteria.

## SYNTAX

```
Get-SPOCrossGeoUsers -ValidDataLocation <Boolean> [<CommonParameters>]
```

## DESCRIPTION

The Get-SPOCrossGeoUsers cmdlet is used to return the SharePoint Online users that match a given criteria. The ValidDataLocation parameter is a switch used to validate the location of the data. This cmdlet requires a connection to a multi-geo tenant to run correctly. You must have the SharePoint Online Admin role to execute this cmdlet.

## EXAMPLES

### EXAMPLE 1

```Powershell
Get-SPOCrossGeoUsers -ValidDataLocation $true
```

Returns all of the SharePoint Online users in a multi-geo tenant and validates the data location.

### EXAMPLE 2

```Powershell
Get-SPOCrossGeoUsers
```

Returns all of the SharePoint Online users in a multi-geo tenant without validating data location.

### EXAMPLE 3

```Powershell
Get-SPOCrossGeoUsers -ValidDataLocation $true | where {$_.UserPrincipalName -eq 'jane@contoso.com'}
```

Returns a single user from SharePoint Online in a multi-geo tenant and validates the data location.

## PARAMETERS

### -ValidDataLocation

> Applicable: SharePoint Online

Use this parameter to validate the location of the data. The acceptable values for this parameter are:

- $False
- $True

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[ConvertTo-SPOMigrationTargetedPackage](ConvertTo-SPOMigrationTargetedPackage.md)
