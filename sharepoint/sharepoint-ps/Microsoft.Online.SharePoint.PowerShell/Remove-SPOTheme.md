---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/remove-spotheme
applicable: SharePoint Online
title: Remove-SPOTheme
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Remove-SPOTheme

## SYNOPSIS

Removes a theme from the theme gallery.

## SYNTAX

```
Remove-SPOTheme [-Identity] <SpoThemePipeBind> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Remove-SPOTheme** cmdlet removes a theme from your tenant store.

## EXAMPLES

### Example 1

This example removes the `"Custom Cyan"` theme that was used in the previous examples for the **Add-SPOTheme** and **Get-SPOTheme** cmdlets.

```powershell
Remove-SPOTheme -Identity "Custom Cyan"
```

## PARAMETERS

### -Identity

Name of the theme to remove.

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

### -Confirm

Prompts you for confirmation before running the cmdlet.

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
