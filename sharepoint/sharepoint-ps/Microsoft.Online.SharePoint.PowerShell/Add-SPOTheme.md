---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spotheme
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

```
Add-SPOTheme [-Identity] <SpoThemePipeBind> -Palette <SpoThemePalettePipeBind> -IsInverted <Boolean>
 [-Overwrite] [<CommonParameters>]
```

## DESCRIPTION

The **Add-SPOTheme** cmdlet creates a new theme or updates an existing theme. The color palette settings can be passed as either a hash table or a dictionary.

Adding a theme does not apply the theme to any sites. It adds the theme to your tenant store, and then the theme is available in the list of themes under the **Change the look** option for modern pages.

## EXAMPLES

### Example 1

In this example, a new theme named `"Custom Cyan"` is created, with color palette settings that are various shades of cyan. Note that the settings are passed as a hash table.

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

> [!NOTE]
> Prior to the December 2017 release of the SPO Management Shell, the **Add-SPOTheme** cmdlet required that color palette settings be passed as a dictionary. We recommend that you use the latest version of the SPO Management Shell, or use the `HashToDictionary` function to convert a hash table to a dictionary if needed.

### Example 2

If you want to update an existing theme (to modify some of its color settings, for example), use the same syntax as shown previously, but add the `-Overwrite` flag to the **Add-SPOTheme** cmdlet.

```powershell
Add-SPOTheme -Identity "Custom Cyan" -Palette $themepalette -IsInverted $false -Overwrite
```

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

### -IsInverted

> Applicable: SharePoint Online

Specifies whether the theme is inverted, with a dark background and a light foreground.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -Palette

> Applicable: SharePoint Online

Specifies the palette of colors in the theme, as a dictionary of theme slot values.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoThemePalettePipeBind
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

### Microsoft.Online.SharePoint.PowerShell.SpoThemePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
