---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/stop-spositecontentmove
applicable: SharePoint Online
title: Stop-SPOSiteContentMove
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
ms.date: 07/15/2025
---

# Stop-SPOSiteContentMove

## SYNOPSIS

Stops a job to move a particular user or group of users to be moved across geo locations relative to the one that executes the command.

## SYNTAX

```
Stop-SPOSiteContentMove [-SourceSiteUrl] <String> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to stop a job to move a particular user or group of users to be moved across geo locations relative to the one that executes the command.

## EXAMPLES

### Example 1

```powershell
Stop-SPOSiteContentMove -SourceSiteUrl https://contoso.sharepoint.com/sites/Research
```

This example stops the move job for the specified site.

## PARAMETERS

### -SourceSiteUrl

Specifies the source URL of the site collection.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
