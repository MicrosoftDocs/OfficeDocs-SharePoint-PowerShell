---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spotheme
applicable: SharePoint Online
title: Get-SPOTheme
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Get-SPOTheme

## SYNOPSIS

## SYNTAX

```
Get-SPOTheme [[-Name] <String>] [<CommonParameters>]
```

## DESCRIPTION

The **Get-SPOTheme** cmdlet returns the settings for a named existing theme, or for all uploaded themes if no name is provided.

## EXAMPLES

### Example 1

This example shows how to use the **Get-SPOTheme** cmdlet to return the settings for the `"Custom Cyan"` theme created in the example for the **Add-SPOTheme** cmdlet. Note that this example uses the PowerShell `ConvertTo-Json` filter to display the theme in JSON format.

```powershell
Get-SPOTheme -Name "Custom Cyan" | ConvertTo-Json 4
```

When the theme is in the new format:
```Output
{
    "Name":  "Teal theme",
    "Palette": null,
    "ColorPairs": {
        "light": [
            {"accentColor": "#0078D4", "backgroundColor": "#FFFFFF"},
            {"accentColor": "#FFFFFF", "backgroundColor": "#0078D4"}
        ]
    },
     "IsInverted":  false
}
```
When the theme is in the legacy format:
```Output
{
    "Name":  "Custom Cyan",
    "Palette":  {
                    "themeLight":  "#affefe",
                    "themeTertiary":  "#76ffff",
                    "black":  "#000000",
                    "neutralSecondary":  "#666666",
                    "neutralTertiaryAlt":  "#c8c8c8",
                    "themeSecondary":  "#39ffff",
                    "themeDarker":  "#005252",
                    "primaryBackground":  "#fff",
                    "neutralQuaternary":  "#d0d0d0",
                    "neutralPrimaryAlt":  "#3c3c3c",
                    "neutralPrimary":  "#333",
                    "themeDark":  "#009090",
                    "themeLighter":  "#daffff",
                    "neutralTertiary":  "#a6a6a6",
                    "neutralQuaternaryAlt":  "#dadada",
                    "themeLighterAlt":  "#f3fcfc",
                    "white":  "#fff",
                    "neutralSecondaryAlt":  "#767676",
                    "neutralLighter":  "#f4f4f4",
                    "neutralLight":  "#eaeaea",
                    "neutralDark":  "#212121",
                    "themeDarkAlt":  "#00c4c4",
                    "neutralLighterAlt":  "#f8f8f8",
                    "primaryText":  "#333",
                    "themePrimary":  "#00ffff"
                },
    "ColorPairs": null,
    "IsInverted":  false
}
```

### Example 2

To return all uploaded themes, use the **Get-SPOTheme** command with no arguments.

```powershell
Get-SPOTheme
```

## PARAMETERS

### -Name

> Applicable: SharePoint Online

The name of the theme.

```yaml
Type: System.String
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

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
