---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/add-spotheme
applicable: SharePoint Online
title: Add-SPOTheme
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Add-SPOTheme

## SYNOPSIS

Creates a new custom theme, or overwrites an existing theme to modify its settings.

## SYNTAX

### NewThemeSet
```
Add-SPOTheme
    [-Identity] <SpoThemePipeBind>
    -ColorPairs <SpoThemeColorPairPipeBind>
    [-Overwrite]
    [<CommonParameters>]
```

### LegacyThemeSet
```
Add-SPOTheme
    [-Identity] <SpoThemePipeBind>
    -Palette <SpoThemePalettePipeBind>
    -IsInverted <Boolean>
    [-Overwrite]
    [<CommonParameters>]
```

## DESCRIPTION
This cmdlet creates a new theme or updates an existing theme. The color pairs settings can be passed as a hash table, while the color palette settings can be passed as either a hash table or a dictionary.

Adding a theme does not automatically apply it to any site. Instead, the theme becomes available in the list of themes under the **Change the look** option for modern SharePoint pages.

Choose the appropriate parameter set based on whether you're working with a legacy or modern theme format. For details about the new theme format, see [Site theme](/sharepoint/site-theme).

> [!NOTE]
> In multi-geo environments, themes added by an administrator in the primary geography are automatically propagated and available across the organization. This cmdlet is not supported for administrators in satellite geographies.

## Examples

### Example 1:

```powershell
$colorPairs = @{
  light = @(
    @{ "accentColor" = "#03787C"; "backgroundColor" = "#FFFFFF" }
    @{ "accentColor" = "#FFFFFF"; "backgroundColor" = "#03787C" }
    @{ "accentColor" = "#E3FFFD"; "backgroundColor" = "#03787C" }
    @{ "accentColor" = "#03787C"; "backgroundColor" = "#E3FFFD" }
    @{ "accentColor" = "#FFF9E3"; "backgroundColor" = "#03787C" }
    @{ "accentColor" = "#03787C"; "backgroundColor" = "#FFF9E3" }
    @{ "accentColor" = "#03787C"; "backgroundColor" = "#F5F5F5" }
    @{ "accentColor" = "#242424"; "backgroundColor" = "#F5F5F5" }
    @{ "accentColor" = "#155473"; "backgroundColor" = "#FFFFFF" }
    @{ "accentColor" = "#FFFFFF"; "backgroundColor" = "#155473" }
    @{ "accentColor" = "#155473"; "backgroundColor" = "#E3FFFD" }
    @{ "accentColor" = "#E3FFFD"; "backgroundColor" = "#155473" }
    @{ "accentColor" = "#FFF9E3"; "backgroundColor" = "#155473" }
    @{ "accentColor" = "#155473"; "backgroundColor" = "#FFF9E3" }
  )
}

Add-SPOTheme -Identity "Teal Theme" -ColorPairs $colorPairs
```

This example creates a theme named `"Teal Theme"` with color pair settings in various shades of teal.

### Example 2:

```powershell
Add-SPOTheme -Identity "Teal Theme" -ColorPairs $colorPairs -Overwrite
```

To update an existing theme in the new format, modify the color settings using the same syntax as when creating a theme. Add the `-Overwrite` flag to the Add-SPOTheme cmdlet.

### Example 3:

```powershell
$themepalette = @{
  "themePrimary" = "#00ffff";
  "themeLighterAlt" = "#f3fcfc";
  "themeLighter" = "#daffff";
  "themeLight" = "#affefe";
  "themeTertiary" = "#76ffff";
  "themeSecondary" = "#39ffff";
  "themeDarkAlt" = "#00c4c4";
  "themeDark" = "#009090";
  "themeDarker" = "#005252";
  "neutralLighterAlt" = "#f8f8f8";
  "neutralLighter" = "#f4f4f4";
  "neutralLight" = "#eaeaea";
  "neutralQuaternaryAlt" = "#dadada";
  "neutralQuaternary" = "#d0d0d0";
  "neutralTertiaryAlt" = "#c8c8c8";
  "neutralTertiary" = "#a6a6a6";
  "neutralSecondaryAlt" = "#767676";
  "neutralSecondary" = "#666666";
  "neutralPrimary" = "#333";
  "neutralPrimaryAlt" = "#3c3c3c";
  "neutralDark" = "#212121";
  "black" = "#000000";
  "white" = "#fff";
  "primaryBackground" = "#fff";
  "primaryText" = "#333"
 }

Add-SPOTheme -Identity "Custom Cyan" -Palette $themepalette -IsInverted $false
```

In this example, a theme named `"Custom Cyan"` is created, with color palette settings that are various shades of cyan. Note that the settings are passed as a hash table.

> [!NOTE]
> Prior to the December 2017 release of the SPO Management Shell, the **Add-SPOTheme** cmdlet required that color palette settings be passed as a dictionary. We recommend that you use the latest version of the SPO Management Shell, or use the `HashToDictionary` function to convert a hash table to a dictionary if needed.

### Example 4: Overwrite a legacy format theme 

```powershell
Add-SPOTheme -Identity "Custom Cyan" -Palette $themepalette -IsInverted $false -Overwrite
```

To update an existing legacy format theme and modify its color settings, use the same syntax as when creating the theme. Add the `-Overwrite` flag to the Add-SPOTheme cmdlet.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the name of the theme. This must uniquely identify the theme.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoThemePipeBind
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Overwrite

> Applicable: SharePoint Online

Overwrites a theme of the same name in case it exists.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ColorPairs

> Applicable: SharePoint Online

Specifies the theme's color pairs using a hash table of slot values. Supports up to 16 color pairs.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoThemeColorPairPipeBind
Parameter Sets: NewThemeSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Palette

> Applicable: SharePoint Online

Specifies the palette of colors in the theme, as a dictionary or hash table of theme slot values.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoThemePalettePipeBind
Parameter Sets: LegacyThemeSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

### -IsInverted

> Applicable: SharePoint Online

Specifies whether the theme is inverted, with a dark background and a light foreground.

```yaml
Type: System.Boolean
Parameter Sets: LegacyThemeSet
Aliases: None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoThemePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
[Site theme](/sharepoint/site-theme)
