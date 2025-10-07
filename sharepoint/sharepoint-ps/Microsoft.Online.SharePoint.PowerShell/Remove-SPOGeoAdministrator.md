---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/remove-spogeoadministrator
applicable: SharePoint Online
title: Remove-SPOGeoAdministrator
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Remove-SPOGeoAdministrator

## SYNOPSIS

Removes a new SharePoint user or security Group in the current Multi-Geo Tenant.

## SYNTAX

### User (Default)

```
Remove-SPOGeoAdministrator [-UserPrincipalName] <String> [<CommonParameters>]
```

### Group

```
Remove-SPOGeoAdministrator [-GroupAlias] <String> [<CommonParameters>]
```

### ObjectId

```
Remove-SPOGeoAdministrator [-ObjectId] <Guid> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet contains a single parameter set.
You may only use parameters from one parameter set and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The `Remove-SPOGeoAdministrator` cmdlet matches a user or a security group and remove the GeoAdministrator privileges in the SharePoint Organization.

You must be at least a SharePoint Online administrator, and you must have a Multi-Geo Tenant to run the `Remove-SPOGeoAdministrator` cmdlet successfully.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Remove-SPOGeoAdministrator contosoadmin
```

Remove the GeoAdministrator privileges to the user contosoadmin of the SharePoint Online multi-geo tenant.

### Example 2

```powershell
Remove-SPOGeoAdministrator -LoginName contosoadmin
```

Same as example 1, but using the LoginName parameter explicitly.

## PARAMETERS

### -GroupAlias

> Applicable: SharePoint Online

The login name of the security group to be removed.

```yaml
Type: System.String
Parameter Sets: Group
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId

> Applicable: SharePoint Online

The ID of the user or security group to be removed.

```yaml
Type: System.Guid
Parameter Sets: ObjectId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName

> Applicable: SharePoint Online

The login name of the user to be removed.

```yaml
Type: System.String
Parameter Sets: User
Aliases:

Required: True
Position: 0
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

[Add-SPOGeoAdministrator](Add-SPOGeoAdministrator.md)

[Get-SPOGeoAdministrator](Get-SPOGeoAdministrator.md)
