---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositescript
applicable: SharePoint Online
title: Get-SPOSiteScript
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOSiteScript

## SYNOPSIS

Displays information about existing site scripts.

## SYNTAX

```
Get-SPOSiteScript [[-Identity] <SPOSiteScriptPipeBind>] [<CommonParameters>]
```

## DESCRIPTION

Displays information about existing site scripts. When no parameter is provided, this cmdlet returns the **Id**, **Title**, **Description**, and **Version** of each site script. When a site script ID is provided, this cmdlet also returns the **Content**, which is the JSON of the site script.

## EXAMPLES

### Example 1

This example shows how to get script information for a specific script ID.

```powershell
Get-SPOSiteScript 07702c07-0485-426f-b710-4704241caad9

Id          : 07702c07-0485-426f-b710-4704241caad9
Title       : Contoso theme
Description :
Content     : {
                  "$schema": "schema.json",
                      "actions": [
                          {
                             "verb": "applyTheme",
                             "themeName": "Custom Cyan"
                          }
                      ],
                          "bindata": { },
                  "version": 1
              }
Version     : 1
```

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

The ID of the site script to get information about.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteScriptPipeBind
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

### Microsoft.Online.SharePoint.PowerShell.SPOSiteScriptPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
