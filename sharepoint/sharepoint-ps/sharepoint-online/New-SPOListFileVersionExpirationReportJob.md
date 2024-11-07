---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/new-spolistfileversionexpirationreportjob
applicable: SharePoint Online
title: New-SPOListFileVersionExpirationReportJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# New-SPOListFileVersionExpirationReportJob

## SYNOPSIS

Starts generating file version expiration report for a document library.

## SYNTAX

```powershell
New-SPOListFileVersionExpirationReportJob [-Site] <SpoSitePipeBind> [-List] <SpoListPipeBind> [-ReportUrl <String>] [<CommonParameters>]
```

## DESCRIPTION

Starts generating file version expiration report for a document library.

## EXAMPLES

### EXAMPLE 1

```powershell
New-SPOListFileVersionExpirationReportJob -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -ReportUrl "https://contoso.sharepoint.com/sites/sites1/reports/MyReports/VersionReport.csv"
```

Example 1 starts generating file version expiration report on for the document library called "Documents", saving the result to a csv file within the site.

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

The URL of the report to save to.

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

[Get-SPOListFileVersionExpirationReportJobProgress](Get-SPOListFileVersionExpirationReportJobProgress.md)
