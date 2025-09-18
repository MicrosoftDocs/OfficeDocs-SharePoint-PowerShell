---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/add-spofontpackage
applicable: SharePoint Online
title: Add-SPOFontPackage
schema: 2.0.0
author: JQ1u
ms.author: luchaoqiu
ms.reviewer:
---

# Add-SPOFontPackage

## SYNOPSIS

Creates a new custom font package with fonts in the brand fonts library.

## SYNTAX

```
Add-SPOFontPackage -Title <String> -PackageJson <String> [-IsHidden <Boolean>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new brand font package for the tenant. Each font package must have a unique name. The font file must be added to the SharePoint Brand Center before creating a font package. For more information, see [Brand Fonts](/sharepoint/brand-fonts).

## EXAMPLES

### EXAMPLE 1

```powershell
$packageJson = @'
{
  "fontFaces": [
    {
      "fontFamily": "Tahoma",
      "path": "Tahoma.ttf",
      "fontType": "contentFont"
    }
  ],
  "fontSlots": {
    "title": {
      "fontFamily": "Tahoma",
      "fontFace": "Regular",
      "fontVariationSettings": {
        "wght": 100,
        "wdth": 100
      }
    },
    "heading": {
      "fontFamily": "Tahoma",
      "fontFace": "Regular",
      "fontVariationSettings": {
        "wght": 100,
        "wdth": 100
      }
    },
    "body": {
      "fontFamily": "Tahoma",
      "fontFace": "Regular",
      "fontVariationSettings": {
        "wght": 100,
        "wdth": 100
      }
    },
    "label": {
      "fontFamily": "Tahoma",
      "fontFace": "Regular",
      "fontVariationSettings": {
        "wght": 100,
        "wdth": 100
      }
    }
  }
}
'@

Add-SPOFontPackage -Title "Tahoma" -PackageJson $packageJson
```

This example creates a new font package named "Tahoma" with specified JSON configuration.

### EXAMPLE 2

```powershell
# With $packageJson from EXAMPLE 1
Add-SPOFontPackage -Title "Contoso Font Package" -PackageJson $packageJson -IsHidden $true
```

This example creates a hidden font package with specified JSON configuration.

## PARAMETERS

### -Title

> Applicable: SharePoint Online

Specifies the display name of the new font package.

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

### -PackageJson

> Applicable: SharePoint Online

Specifies the JSON configuration for the font package.

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

### -IsHidden

> Applicable: SharePoint Online

Specifies whether the font package should be hidden from users. When set to `$true`, the font package will not be visible in the **Change the look** options, but can still be applied using the `Set-SPOFontPackage` cmdlet.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOFontPackage](Get-SPOFontPackage.md)

[Set-SPOFontPackage](Set-SPOFontPackage.md)

[Remove-SPOFontPackage](Remove-SPOFontPackage.md)
