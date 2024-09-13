---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: 
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

This cmdlet enables the admin to check status of all active and available reports when no report ID is present and to View/Download a Report if report ID is present.

## SYNTAX

```powershell
Get-SPOEnterpriseAppInsightsReport [-ReportId <Guid>] [-Action <enum>]
```

## Description

If this cmdlet is executed without any parameters, it displays the status of all active and completed reports (adhering to any retention timeline as per DAG) with the following properties:
| Property             | Description                              |
| :------------------- | :--------------------------------------- |
| Id | The unique Id of the report.                    |
| CreatedDateTimeInUtc | The Date and Time the report creation was triggered in UTC.                   |
| Status | The Status of the report.               |
| ReportPeriodInDays | The report duration in days.       |

If this cmdlet is executed with `-ReportId` as parameter, the top 100 records of the report from the last N days will be displayed with the following properties:
| Property             | Description                              |
| :------------------- | :--------------------------------------- |
| SiteName | The name of the SharePoint Site.                    |
| SiteURL               | The URL of the SharePoint Site.                   |
| SiteSensitivity | The Sensitivity Label of the SharePoint Site.               |
| AppID | The AppID of the 3P App.       |
| AppPermissions| The Permissions granted to the 3P App. |
| RequestVoulme | The number of times the 3P accessed the given SharePoint Site.          |

If this cmdlet is executed with both the parameters, i.e. `-ReportId` and `-Action`, and if the value of `-Action` is set as `View`, it will display the same result as described above. If the value of `-Action` is set to `Download`, it will download the full report in CSV format.
  
## Example

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPOEnterpriseAppInsightsReport
```

Example 1 enables admin to view the status of all active and completed reports (adhering to any retention timeline as per DAG).

### -----------------------EXAMPLE 2-----------------------------

```powershell
Get-SPOEnterpriseAppInsightsReport –ReportId 9d946216-afe7-49f5-8267-7b662435c70b
```

Example 2 enables admin to view the Enterprise Application Insights report of ReportId: `9d946216-afe7-49f5-8267-7b662435c70b`

### -----------------------EXAMPLE 3-----------------------------

```powershell
Get-SPOEnterpriseAppInsightsReport – ReportId 9d946216-afe7-49f5-8267-7b662435c70b -Action Download
```

Example 3 enables admin to download the Enterprise Application Insights report of ReportId: `9d946216-afe7-49f5-8267-7b662435c70b`.

## PARAMETERS

### - ReportId

It is an optional parameter, and it specifies the unique Id of the report to be viewed/downloaded.

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

### - Action

It is an optional parameter, and it specifies whether to view or download a specific report.

```yaml
Type: enum
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Related Links

[Get started with SharePoint Online Management Shell](https://learn.microsoft.com/en-us/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Start-SPOEnterpriseAppInsightsReport](https://learn.microsoft.com/en-us/powershell/sharepoint/sharepoint-online/start-spoenterpriseappinsightsreport)