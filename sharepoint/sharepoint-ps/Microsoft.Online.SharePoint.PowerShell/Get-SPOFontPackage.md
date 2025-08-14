---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spofontpackage
applicable: SharePoint Online
title: Get-SPOFontPackage
schema: 2.0.0
author: luchaoqiu
ms.author: luchaoqiu
ms.reviewer:
---

# Get-SPOFontPackage

## SYNOPSIS

Returns one or all custom font packages from the SharePoint tenant.

## SYNTAX

```
Get-SPOFontPackage [[-Identity] <SPOFontPackagePipeBind>] [<CommonParameters>]
```

## DESCRIPTION

The `Get-SPOFontPackage` cmdlet retrieves one or more custom font packages from the SharePoint tenant. Custom font packages include those created through the SharePoint Brand Center app or by using the `Add-SPOFontPackage` cmdlet. You can retrieve a specific font package by providing its identity, or retrieve all font packages if no identity is specified.

Font packages contain custom typography definitions that can be applied to SharePoint sites and Viva Connections for branding purposes.

After running this cmdlet, the information for each font package will be displayed with the following properties:

| Property    | Type   | Description                                             |
| :---------- | :----- | :------------------------------------------------------|
| ID          | Guid   | Unique ID of the font package.                          |
| Title       | string | The display name of the font package.                   |
| IsHidden    | bool   | Whether the font package is hidden from the SharePointUI. |
| IsValid     | bool   | Whether the font package is valid and can be applied.   |
| PackageJson | string | The JSON specifying the settings of the font package.   |

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOFontPackage
```

This example returns all font packages in the tenant.

### EXAMPLE 2

```powershell
Get-SPOFontPackage -Identity 12345678-1234-1234-1234-123456789012
```

This example returns the font package with the specified GUID.

### EXAMPLE 3

```powershell
Get-SPOFontPackage | Where-Object {$_.IsHidden -eq $false}
```

This example returns all visible font packages (not hidden).

### EXAMPLE 4

```powershell
$fontPackage = Get-SPOFontPackage -Identity 12345678-1234-1234-1234-123456789012
$fontPackage.PackageJson
```

This example retrieves a specific font package and displays its JSON configuration.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the identity of the font package to retrieve. This can be the ID (GUID) of the font package, or a font package object. If not specified, all font packages will be retrieved.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOFontPackagePipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SPOFontPackagePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-SPOFontPackage](Add-SPOFontPackage.md)

[Set-SPOFontPackage](Set-SPOFontPackage.md)

[Remove-SPOFontPackage](Remove-SPOFontPackage.md)
