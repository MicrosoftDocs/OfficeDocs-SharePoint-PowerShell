---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/remove-spofontfile
applicable: SharePoint Online
title: Remove-SPOFontFile
schema: 2.0.0
author: yingli915
ms.author: yingli3
ms.reviewer:
---

# Remove-SPOFontFile

## SYNOPSIS

Removes a **SharePoint** brand font file from the tenant's brand fonts library.

## SYNTAX

```
Remove-SPOFontFile [-Name] <string> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet removes a custom font file from the tenant's brand fonts library. The font file is deleted from the primary geo and all satellite geos. After removal, the font file will no longer be available for use **in SharePoint**.

> [!NOTE]
> This operation is only allowed on the primary geo location. Attempting to remove a font file from a satellite geo will result in a warning. Pages that already use the removed font file will remain readable and the font will automatically fall back to Segoe UI. The font packages that use the deleted font file will not be automatically updated or deleted.

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOFontFile -Name "Tahoma.ttf"
```

This example removes the SharePoint brand font file "Tahoma.ttf" from the brand fonts library across all geo locations.

## PARAMETERS

### -Name

> Applicable: SharePoint Online

Specifies the name of the font file to remove

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Online.SharePoint.PowerShell.BrandFontFileDeleteResult[]

Returns an array of BrandFontFileDeleteResult objects containing the deletion status for each geo location.

## RELATED LINKS

[Brand Fonts](https://learn.microsoft.com/en-us/sharepoint/brand-fonts)

[Add-SPOFontPackage](Add-SPOFontPackage.md)

[Remove-SPOFontPackage](Remove-SPOFontPackage.md)
