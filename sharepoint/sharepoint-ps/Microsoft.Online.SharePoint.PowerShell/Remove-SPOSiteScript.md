---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spositescript
applicable: SharePoint Online
title: Remove-SPOSiteScript
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Remove-SPOSiteScript

## SYNOPSIS

Removes a site script.

## SYNTAX

```
Remove-SPOSiteScript [-Identity] <SPOSiteScriptPipeBind> [<CommonParameters>]
```

## EXAMPLES

### Example 1

This example shows how to remove a site design.

```powershell
Remove-SPOSiteScript 5ea28194-6fe7-4e2c-ba84-c409368278e2
```

## DESCRIPTION

Removes a site script.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

The ID of the site script to remove.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteScriptPipeBind
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

### Microsoft.Online.SharePoint.PowerShell.SPOSiteScriptPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
