---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spolistfileversionexpirationreportjobprogress
applicable: SharePoint Online
title: Get-SPOListFileVersionExpirationReportJobProgress
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Get-SPOListFileVersionExpirationReportJobProgress

## SYNOPSIS

Gets the status for a file version expiration report generation job for a document library.

## SYNTAX

```
Get-SPOListFileVersionExpirationReportJobProgress [-Site] <SpoSitePipeBind> -List <SPOListPipeBind>
 -ReportUrl <String> [<CommonParameters>]
```

## DESCRIPTION

Gets the status for a file version expiration report generation job for a document library.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOListFileVersionExpirationReportJobProgress -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -ReportUrl "https://contoso.sharepoint.com/sites/sites1/reports/MyReports/VersionReport.csv"
```

Example 1 gets the status for a file version expiration report generation job for a document library called "Documents".

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

### -ReportUrl

The URL of the report to get the job status on.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

[New-SPOListFileVersionExpirationReportJob](New-SPOListFileVersionExpirationReportJob.md)
