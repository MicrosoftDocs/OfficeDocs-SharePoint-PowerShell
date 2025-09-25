---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spositefileversionbatchdeletejobprogress
applicable: SharePoint Online
title: Get-SPOSiteFileVersionBatchDeleteJobProgress
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Get-SPOSiteFileVersionBatchDeleteJobProgress

## SYNOPSIS

Gets the progress of a trim job for a site collection.

## SYNTAX

```
Get-SPOSiteFileVersionBatchDeleteJobProgress [-Identity] <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

Gets the progress of a trim job for a site collection.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOSiteFileVersionBatchDeleteJobProgress -Identity https://contoso.sharepoint.com/sites/site1
```

Example 1 gets the progress of a trim job for a site collection.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the URL of the site collection.

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

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Remove-SPOSiteFileVersionBatchDeleteJob](Remove-SPOSiteFileVersionBatchDeleteJob.md)

[New-SPOSiteFileVersionBatchDeleteJob](New-SPOSiteFileVersionBatchDeleteJob.md)
