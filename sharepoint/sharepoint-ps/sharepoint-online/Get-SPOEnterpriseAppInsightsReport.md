---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spoenterpriseappinsightsreport
applicable: SharePoint Online
title: Get-SPOEnterpriseAppInsightsReport
schema: 2.0.0
author: sumikumar
ms.author: sumikumar
ms.reviewer:
manager: hikakar
---

# Get-SPOEnterpriseAppInsightsReport

## SYNOPSIS

This cmdlet enables the administrator to check status of all active and available reports when no report ID is present and to view or download a report if report ID is present.

## SYNTAX

```powershell
Get-SPOEnterpriseAppInsightsReport [-ReportId <Guid>] [-Action <ActionType>]
```

## DESCRIPTION

If this cmdlet is executed without any parameters, it displays the status of all active and completed reports with the following properties:

| Property             | Description                                                 |
|:---------------------|:------------------------------------------------------------|
| Id                   | The unique Id of the report.                                |
| CreatedDateTimeInUtc | The date and time the report creation was triggered in UTC. |
| Status               | The status of the report.                                   |
| ReportPeriodInDays   | The report duration in days.                                |

If this cmdlet is executed with `-ReportId` as parameter, the top 100 records of the report from the last N days will be displayed with the following properties:

| Property        | Description                                                                |
|:----------------|:---------------------------------------------------------------------------|
| SiteName        | The name of the SharePoint site.                                           |
| SiteURL         | The URL of the SharePoint site.                                            |
| SiteSensitivity | The sensitivity label of the SharePoint site.                              |
| AppID           | The AppID of the 3P application.                                           |
| AppPermissions  | The permissions granted to the 3P application.                             |
| RequestVoulme   | The number of times the 3P application accessed the given SharePoint site. |

If this cmdlet is executed with both the parameters, i.e. `-ReportId` and `-Action`, and if the value of `-Action` is set as `View`, it will display the same result as described above. If the value of `-Action` is set to `Download`, it will download the full report in CSV format to the same path from where the command was run.
  
> [!NOTE]
> All reports adhere to any retention timeline as per [Data Access Governance](/sharepoint/data-access-governance-reports).

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPOEnterpriseAppInsightsReport
```

Example 1 enables administrator to view the status of all active and completed reports.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Get-SPOEnterpriseAppInsightsReport –ReportId 9d946216-afe7-49f5-8267-7b662435c70b
```

Example 2 enables administrator to view the enterprise application insights report of ReportId: `9d946216-afe7-49f5-8267-7b662435c70b`

### -----------------------EXAMPLE 3-----------------------------

```powershell
Get-SPOEnterpriseAppInsightsReport – ReportId 9d946216-afe7-49f5-8267-7b662435c70b -Action Download
```

Example 3 enables administrator to download the enterprise application insights report of ReportId: `9d946216-afe7-49f5-8267-7b662435c70b` to the same path from where the command was run.

## PARAMETERS

### -ReportId

It is an optional parameter, and it specifies the unique Id of the report to be viewed or downloaded.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Action

It is an optional parameter, and it specifies whether to view or download a specific report.

```yaml
Type: ActionType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Start-SPOEnterpriseAppInsightsReport](./Start-SPOEnterpriseAppInsightsReport.md)