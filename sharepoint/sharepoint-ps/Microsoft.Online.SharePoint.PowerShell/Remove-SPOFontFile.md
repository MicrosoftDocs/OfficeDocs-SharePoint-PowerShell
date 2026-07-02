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

Removes a brand font file from the tenant's brand font library.

## SYNTAX

```
Remove-SPOFontFile [-Name] <string> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet removes a custom font file from the tenant's brand font library. The font file is deleted from the primary geo and all satellite geos. After removal, the font file will no longer be available for use.

The cmdlet returns a BrandFontFileDeleteResult object for each geo location, showing the GeoLocation, Status, and Message. Possible status values are: Removed, NotFound, or Failed.

> [!NOTE]
> This operation is only allowed on the primary geo location. Attempting to remove a font file from a satellite geo will result in a warning.

> [!NOTE]
> Pages that already use the removed font file will remain readable and the font will automatically fall back to Segoe UI. The font package itself is not automatically updated or deleted.

## EXAMPLES

### EXAMPLE 1

This example removes the font file "CustomFont.woff2" from the brand font library across all geo locations.

```powershell
Remove-SPOFontFile -Name "CustomFont.woff2"
```

```Output
GeoLocation Status   Message
----------- ------   -------
Primary     Removed  Success
EUR         Removed  Success
APC         Removed  Success
```

### EXAMPLE 2

This example shows the results when the removal operation encounters various conditions across geo locations.

```powershell
Remove-SPOFontFile -Name "AudiType-Italic.ttf" 
```

```Output
GeoLocation Status   Message
----------- ------   -------
Primary     Removed  Success
EUR         NotFound Font file 'AudiType-Italic.ttf' not found in Brand Fonts Library.
APC         Failed   Insufficient permissions to access the Org Asset Library site.
```

## PARAMETERS

### -Name

Specifies the name of the font file to remove (e.g., "MyFont.woff2").

```yaml
Type: String
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

### String

## OUTPUTS

### Microsoft.Online.SharePoint.PowerShell.BrandFontFileDeleteResult[]

Returns an array of BrandFontFileDeleteResult objects containing the deletion status for each geo location.

## NOTES

**Permissions required:** The user executing this cmdlet must be an **Org Asset Library (OAL) admin** on each geo location where the font file deletion is performed. Without sufficient permissions on a geo, the operation will fail for that location with an "Insufficient permissions" error.

**Tenant-level preconditions:** When the cmdlet encounters precondition errors at the tenant level, it returns a warning instead of per-geo results:
- Brand Center or Brand Fonts library is not configured
- The cmdlet is run against a satellite geo instead of the primary
- The BrandFontFileDeletion flight is disabled

**Font fallback:** Pages that already use the removed font file will remain readable and automatically fall back to Segoe UI.
