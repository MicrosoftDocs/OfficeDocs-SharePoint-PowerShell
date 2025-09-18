---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/get-spositefileversionexpirationreportjobprogress
applicable: SharePoint Online
title: Get-SPOSiteFileVersionExpirationReportJobProgress
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Get-SPOSiteFileVersionExpirationReportJobProgress

## SYNOPSIS

Gets the status for a file version expiration report generation job for a site collection.

## SYNTAX

```
Get-SPOSiteFileVersionExpirationReportJobProgress [-Identity] <SpoSitePipeBind> -ReportUrl <String>
 [<CommonParameters>]
```

## DESCRIPTION

Gets the status for a file version expiration report generation job for a site collection.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOSiteFileVersionExpirationReportJobProgress -Identity https://contoso.sharepoint.com/sites/site1 -ReportUrl "https://contoso.sharepoint.com/sites/sites1/reports/MyReports/VersionReport.csv"
```

Example 1 gets the status for a file version expiration report generation job for a site collection.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[New-SPOSiteFileVersionExpirationReportJob](New-SPOSiteFileVersionExpirationReportJob.md)
