---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spouseronedrivelocation
applicable: SharePoint Online
title: Get-SPOUserOneDriveLocation
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
ms.date: 07/16/2025
---

# Get-SPOUserOneDriveLocation

## SYNOPSIS

This cmdlet will return the user principal name, current location, and corresponding OneDrive for Business url, and the site ID. This cmdlet only supports Multi-Geo OneDrive sites.

## SYNTAX

```
Get-SPOUserOneDriveLocation -UserPrincipalName <String> [<CommonParameters>]
```

## DESCRIPTION

This command will return information about the OneDrive location for the specified user.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOUserOneDriveLocation -UserPrincipalName admin@contoso.com
```

Get the current location the user's OneDrive location, url, and site ID.

## PARAMETERS

### -UserPrincipalName

> Applicable: SharePoint Online

UserPrincipalName or UPN defined for the specific user on the SPO tenant.

```yaml
Type: System.String
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
