---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spositedesign
applicable: SharePoint Online
title: Remove-SPOSiteDesign
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Remove-SPOSiteDesign

## SYNOPSIS

Removes a site design. It no longer appears in the UI for creating a new site.

## SYNTAX

```
Remove-SPOSiteDesign [-Identity] <SPOSiteDesignPipeBind> [<CommonParameters>]
```

## DESCRIPTION

Removes a site design. It no longer appears in the UI for creating a new site.

## EXAMPLES

### Example 1

This example shows how to remove a site design.

```powershell
Remove-SPOSiteDesign 21209d88-38de-4844-9823-f1f600a1179a
```

## PARAMETERS

### -Identity

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

The ID of the site design to remove.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPipeBind
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

### Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
