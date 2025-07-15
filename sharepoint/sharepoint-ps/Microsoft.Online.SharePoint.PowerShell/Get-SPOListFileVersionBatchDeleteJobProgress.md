---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spolistfileversionbatchdeletejobprogress
applicable: SharePoint Online
title: Get-SPOListFileVersionBatchDeleteJobProgress
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Get-SPOListFileVersionBatchDeleteJobProgress

## SYNOPSIS

Gets the progress of a trim job for a site collection.

## SYNTAX

```
Get-SPOListFileVersionBatchDeleteJobProgress [-Site] <SpoSitePipeBind> -List <SPOListPipeBind>
 [<CommonParameters>]
```

## DESCRIPTION

Gets the progress of a trim job for a document library.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOListFileVersionBatchDeleteJobProgress -Site https://contoso.sharepoint.com/sites/site1 -List "Documents"
```

Example 1 gets the progress of a trim job for a document library called "Documents".

## PARAMETERS

### -List

The document library name or Id.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOListPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Site

> Applicable: SharePoint Online

Specifies the URL of the site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
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

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

### Microsoft.Online.SharePoint.PowerShell.SPOListPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Remove-SPOListFileVersionBatchDeleteJob](Remove-SPOListFileVersionBatchDeleteJob.md)

[New-SPOListFileVersionBatchDeleteJob](New-SPOListFileVersionBatchDeleteJob.md)
