---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/set-spofontpackage
applicable: SharePoint Online
title: Set-SPOFontPackage
schema: 2.0.0
author: JQ1u
ms.author: luchaoqiu
ms.reviewer:
---

# Set-SPOFontPackage

## SYNOPSIS

Applies a brand font package to a SharePoint site or Viva Connections.

## SYNTAX

```
Set-SPOFontPackage [-Identity] <SPOFontPackagePipeBind> [-WebUrl] <String> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet applies a brand font package to a specified SharePoint site or Viva Connections. Use this cmdlet to customize the typography and branding of SharePoint sites by applying predefined font packages.

## EXAMPLES

### EXAMPLE 1

```powershell
Set-SPOFontPackage -Identity 12345678-1234-1234-1234-123456789012 -WebUrl "https://contoso.sharepoint.com/sites/marketing"
```

This example applies the font package with the specified GUID to the marketing site.

### EXAMPLE 2

```powershell
$sites = @("https://contoso.sharepoint.com/sites/hr", "https://contoso.sharepoint.com/sites/finance")
$fontPackage = Get-SPOFontPackage -Identity 12345678-1234-1234-1234-123456789012
foreach ($site in $sites) {
    Set-SPOFontPackage -Identity $fontPackage -WebUrl $site
}
```

This example retrieves a font package and applies it to multiple sites.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the identity of the font package to apply. This can be the ID (GUID) of the font package, or a font package object.

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

### -WebUrl

> Applicable: SharePoint Online

Specifies the URL of the SharePoint site or Viva Connections where the font package will be applied.

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

### Microsoft.Online.SharePoint.PowerShell.SPOFontPackagePipeBind

## OUTPUTS

### None

## NOTES

## RELATED LINKS

[Add-SPOFontPackage](Add-SPOFontPackage.md)

[Get-SPOFontPackage](Get-SPOFontPackage.md)

[Remove-SPOFontPackage](Remove-SPOFontPackage.md)
