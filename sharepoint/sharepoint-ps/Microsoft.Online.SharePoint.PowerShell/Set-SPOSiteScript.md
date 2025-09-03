---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spositescript
applicable: SharePoint Online
title: Set-SPOSiteScript
schema: 2.0.0
author: trent-green
ms.author: speedta
ms.reviewer:
---

# Set-SPOSiteScript

## SYNOPSIS

Updates a previously uploaded site script.

## SYNTAX

```
Set-SPOSiteScript -Identity <SPOSiteScriptPipeBind> [-Title <String>] [-Content <String>]
 [-Description <String>] [-Version <Int32>] [<CommonParameters>]
```

## DESCRIPTION

Updates a previously uploaded site script.

## EXAMPLES

### Example 1

This example updates a previously created site script. Any site designs referencing it execute the updated script.

```powershell
$newnavscript = @'
{
    "$schema": "schema.json",
        "actions": [
            {
                "verb": "addNavLink",
                "url": "/Custom Library",
                "displayName": "Custom Library Updated",
                "isWebRelative": true
            },
            {
                "verb": "addNavLink",
                "url": "/Lists/Custom List",
                "displayName": "Custom List Updated",
                "isWebRelative": true
            },
            {
                "verb": "applyTheme",
                "themeName": "Contoso Explorers"
            }
        ],
            "bindata": { },
    "version": 2
};
'@

Set-SPOSiteScript -Identity edaec4ec-71e2-4026-ac1e-6686bb30190d -Content $newnavscript -Version 2

```

## PARAMETERS

### -Content

> Applicable: SharePoint Online

The JSON value that describes the script. For more information, see the [JSON reference](/sharepoint/dev/declarative-customization/site-design-json-schema).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Description

> Applicable: SharePoint Online

A description of the script.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Online

The id of the site design.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteScriptPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title

> Applicable: SharePoint Online

The display name of the site design.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version

> Applicable: SharePoint Online

A version number of the script.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
