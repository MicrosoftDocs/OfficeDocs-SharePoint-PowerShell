---
external help file: sharepointonline.xml
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

```powershell
Get-SPOListFileVersionExpirationReportJobProgress [-Site] <SpoSitePipeBind> [-List] <SpoListPipeBind> [-ReportUrl <String>] [<CommonParameters>]
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

### -Site

Specifies the URL of the site.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -List

The document library name or Id.

```yaml
Type: SPOListPipeBind
Parameter Sets: (All)

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportUrl

The URL of the report to get the job status on.

```yaml
Type: string
Parameter Sets: (All)

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[New-SPOListFileVersionExpirationReportJob](New-SPOListFileVersionExpirationReportJob.md)
