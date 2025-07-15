---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spolistdesign
schema: 2.0.0
author: SaladiHarini
ms.author: hasaladi
ms.reviewer:
title: Remove-SPOListDesign
---

# Remove-SPOListDesign

## SYNOPSIS
Removes a list design. It no longer appears in the UI for creating a new list.

## SYNTAX

```
Remove-SPOListDesign [-Identity] <SPOListDesignPipeBind> [<CommonParameters>]
```

## DESCRIPTION
Removes a list design. It no longer appears in the UI for creating a new list.

## EXAMPLES

### Example 1

```powershell
PS > Remove-SPOListDesign -Identity 44252d09-62c4-4913-9eb0-a2a8b8d7f863
```
This example shows how to remove a list design.

## PARAMETERS

### -Identity
The ID of the list design to remove.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOListDesignPipeBind
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

### Microsoft.Online.SharePoint.PowerShell.SPOListDesignPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
