---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spofontpackage
applicable: SharePoint Online
title: Remove-SPOFontPackage
schema: 2.0.0
author: luchaoqiu
ms.author: luchaoqiu
ms.reviewer:
---

# Remove-SPOFontPackage

## SYNOPSIS

Removes a brand font package from the SharePoint tenant.

## SYNTAX

```
Remove-SPOFontPackage [-Identity] <SPOFontPackagePipeBind> [<CommonParameters>]
```

## DESCRIPTION

The `Remove-SPOFontPackage` cmdlet removes a custom font package from the SharePoint tenant. After removal, the font package will no longer be available for use on SharePoint sites or Viva Connections.

> [!NOTE]
> Removing a font package does not delete the associated brand font files. Pages that already use the removed font package will continue to display the configured fonts, but you will no longer be able to modify the font package settings.

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOFontPackage -Identity 12345678-1234-1234-1234-123456789012
```

This example removes the font package with the specified GUID.

### EXAMPLE 2

```powershell
$fontPackage = Get-SPOFontPackage -Identity 12345678-1234-1234-1234-123456789012
Remove-SPOFontPackage -Identity $fontPackage
```

This example retrieves a font package and then removes it.

### EXAMPLE 3

```powershell
Get-SPOFontPackage | Where-Object {$_.IsHidden -eq $true} | Remove-SPOFontPackage
```

This example removes all hidden font packages from the SharePoint tenant.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the identity of the font package to remove. This can be the ID (GUID) of the font package, or a font package object.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOFontPackagePipeBind
Parameter Sets: (All)
Aliases:

Required: True
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

### None

## NOTES

## RELATED LINKS

[Add-SPOFontPackage](Add-SPOFontPackage.md)

[Get-SPOFontPackage](Get-SPOFontPackage.md)

[Set-SPOFontPackage](Set-SPOFontPackage.md)
