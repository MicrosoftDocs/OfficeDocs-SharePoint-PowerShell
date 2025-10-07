---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/set-spowebtheme
applicable: SharePoint Online
title: Set-SPOWebTheme
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Set-SPOWebTheme

## SYNOPSIS

Sets the theme for a SharePoint site.

## SYNTAX

```
Set-SPOWebTheme [-Theme] <SpoThemePipeBind> [-Web] <SpoSitePipeBind> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to set the custom theme for a Site

## EXAMPLES

### Example 1

```powershell
 Set-SPOWebTheme -Theme "Custom cyan" -Web https://contoso.sharepoint.com/sites/Contoso1
```

This example sets the "Custom Cyan" theme to the https://contoso.sharepoint.com/sites/Contoso1 site.

## PARAMETERS

### -Theme

> Applicable: SharePoint Online

Name of the theme or SPOTheme object

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoThemePipeBind
Parameter Sets: (All)
Aliases: Identity, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Web

> Applicable: SharePoint Online
Url of the site

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
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
