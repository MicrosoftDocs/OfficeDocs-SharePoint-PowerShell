---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/get-spositescriptfromlist
applicable: SharePoint Online
title: Get-SPOSiteScriptFromList
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Get-SPOSiteScriptFromList

## SYNOPSIS

Creates site script syntax from an existing SharePoint list.

## SYNTAX

```
Get-SPOSiteScriptFromList [-ListUrl] <String> [<CommonParameters>]
```

## DESCRIPTION

Uses an existing SharePoint list to output a JSON blob that can be used to create a site script for use in a site design.

## EXAMPLES

### Example 1

This example creates the site script output from an existing list - and writes it to a variable. This variable is then referenced to create a site script.

```powershell
$extracted = Get-SPOSiteScriptFromList -ListUrl "https://contoso.sharepoint.com/sites/strategy/customer-contacts"
Add-SPOSiteScript `
    -Title "Contoso Customer Tracker"
    -Description "This creates a customer contact list"
    -Content $extracted
```

## PARAMETERS

### -ListUrl

> Applicable: SharePoint Online

The url of the list to be referenced for the JSON output.

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

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
