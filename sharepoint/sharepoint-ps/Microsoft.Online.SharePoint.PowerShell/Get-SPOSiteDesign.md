---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositedesign
applicable: SharePoint Online
title: Get-SPOSiteDesign
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOSiteDesign

## SYNOPSIS

Gets details about site designs that are on the SharePoint tenant. You can specify an ID of a specific site design to retrieve. If there are no parameters listed, details about all site designs are listed.

## SYNTAX

```
Get-SPOSiteDesign [[-Identity] <SPOSiteDesignPipeBind>] [<CommonParameters>]
```

## DESCRIPTION

Gets details about site designs that are on the SharePoint tenant. You can specify an ID of a specific site design to retrieve. If there are no parameters listed, details about all site designs are listed.

## EXAMPLES

### Example 1

This example and sample response show how to get site design details.

```powershell
Get-SPOSiteDesign 44252d09-62c4-4913-9eb0-a2a8b8d7f863

Id                  : 44252d09-62c4-4913-9eb0-a2a8b8d7f863
Title               : Contoso - Team Project
WebTemplate         : 64
SiteScriptIds       : {1306913c-8463-42ca-bd63-efad0fcdbba4}
Description         : Use this design to apply Contoso theme and create
                      custom lists and add to nav
```

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

The ID of the site design to retrieve.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPipeBind
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

### Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
