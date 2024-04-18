---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/new-spositefileversionexpirationreportjob
applicable: SharePoint Online
title: New-SPOSiteFileVersionExpirationReportJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
---

# New-SPOSiteFileVersionExpirationReportJob

## SYNOPSIS

Starts generating file version usage report for a site collection.

## SYNTAX

```powershell
New-SPOSiteFileVersionExpirationReportJob [-Identity] <SpoSitePipeBind>
 [-ReportUrl <String>]
 [<CommonParameters>]
```

## DESCRIPTION

Starts generating file version usage report for a site collection.

## EXAMPLES

### EXAMPLE 1

```powershell
New-SPOSiteFileVersionExpirationReportJob -Identity https://contoso.sharepoint.com/sites/site1 -ReportUrl "https://contoso.sharepoint.com/sites/sites1/reports/MyReports/VersionReport.csv"
```

Example 1 starts generating file version usage report on for the site collection, saving the result to a csv file within the site collection.

## PARAMETERS

### -Identity

Specifies the URL of the site collection.

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

[Getting started with SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Get-SPOSiteFileVersionExpirationReportJobProgress](Get-SPOSiteFileVersionExpirationReportJobProgress.md)