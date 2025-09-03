---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spolistdesign
schema: 2.0.0
author: SaladiHarini
ms.author: hasaladi
title: Get-SPOListDesign
ms.date: 07/15/2025
---

# Get-SPOListDesign

## SYNOPSIS
Gets details about list designs that are on the SharePoint tenant. You can specify an ID of a specific list design to retrieve. If there are no parameters listed, details about all list designs are listed. 

## SYNTAX

```
Get-SPOListDesign [[-Identity] <SPOListDesignPipeBind>] [<CommonParameters>]
```

## DESCRIPTION
Gets details about list designs that are on the SharePoint tenant. You can specify an ID of a specific list design to retrieve. If there are no parameters listed, details about all list designs are listed. 

## EXAMPLES

### Example 1

```output
Get-SPOListDesign -Identity 44252d09-62c4-4913-9eb0-a2a8b8d7f863 

Id: 44252d09-62c4-4913-9eb0-a2a8b8d7f863  
Title: Contoso customer tracking  
SiteScriptIds: {1306913c-8463-42ca-bd63-efad0fcdbba4}  
Description: Tracks key customer data in a list 
ListColor: Orange 
ListIcon: BullseyeTarget
```

This example and sample response show how to get list design details. 

## PARAMETERS

### -Identity
The ID of the list design to retrieve. 

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOListDesignPipeBind
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

### Microsoft.Online.SharePoint.PowerShell.SPOListDesignPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
