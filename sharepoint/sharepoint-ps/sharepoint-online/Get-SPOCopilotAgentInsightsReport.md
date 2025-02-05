---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocopilotagentinsightsreport
applicable: SharePoint Online
title: Get-SPOCopilotAgentInsightsReport
schema: 2.0.0
author: bhagatshweta
ms.author: bhagatshweta
ms.reviewer:
manager: hikakar
---

# Get-SPOCopilotAgentInsightsReport

## SYNOPSIS

This cmdlet enables the administrator to check status of all active and available reports when no report ID is present and to view or download a report if report ID is present.

> [!NOTE]
> The feature associated with this cmdlet will be rolling out soon.

## SYNTAX

```powershell
Get-SPOCopilotAgentInsightsReport [-ReportId <Guid>] [-Content <SPOCopilotAgentInsightType>] [-Action <ActionType>]
```

## DESCRIPTION

If this cmdlet is executed without any parameters, it displays the status of all active and completed reports with the following properties:

| Property             | Description                                                      |
|:---------------------|:-----------------------------------------------------------------|
| Id                   | The unique Id of the report.                                     |
| CreatedDateTimeInUtc | The date and time in UTC when the report creation was triggered. |
| Status               | The status of the report.                                        |
| ReportPeriodInDays   | The report duration in days.                                     |

> [!NOTE]
> All reports adhere to any retention timeline as per [Data Access Governance](/sharepoint/data-access-governance-reports).

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPOCopilotAgentInsightsReport
```

Example 1 enables administrator to view the status of all active and completed reports.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Get-SPOCopilotAgentInsightsReport –ReportId 9d946216-afe7-49f5-8267-7b662435c70b
```

Example 2 enables administrator to view the Copilot agent insight report of ReportId: `9d946216-afe7-49f5-8267-7b662435c70b`.

### -----------------------EXAMPLE 3-----------------------------

```powershell
Get-SPOCopilotAgentInsightsReport – ReportId 9d946216-afe7-49f5-8267-7b662435c70b -Action Download
```

Example 3 enables administrator to download the Copilot agent insight report of ReportId: `9d946216-afe7-49f5-8267-7b662435c70b` to the same path from where the command was run.

## PARAMETERS

### -ReportId

It specifies the unique Id of the report to be viewed or downloaded.

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

### -Content

It specifies the kind of report to view or download. There are 3 kinds of sub-reports: CopilotAgentsOnSites, TopSites, SiteDistribution.

If this cmdlet is executed with `-Content` as `CopilotAgentsOnSites`, a report with list of all sites on which a Copilot agent is created along with the names of the Copilot agent created in the specified number of days will be displayed with the following properties:

| Property                        | Description                                                     |
|:--------------------------------|:----------------------------------------------------------------|
| Site name                       | The name of the SharePoint site.                                |
| URL                             | The URL of the SharePoint site.                                 |
| Template                        | The Site template of the SharePoint site.                       |
| Site owner                      | Name of the owner of the SharePoint site.                       |
| Copilot name                    | Name of Copilot agent on the SharePoint site.                   |
| Sensitivity                     | The sensitivity label of the SharePoint site.                   |
| Restrict site access enabled    | Restrict site access status (Yes/No) of the SharePoint site.    |
| Restrict site discovery enabled | Restrict site discovery status (Yes/No) of the SharePoint site. |
| External sharing                | External Sharing status (Yes/No) of the SharePoint site.        |

If this cmdlet is executed with `-ReportId` as parameter and `-Content` as `TopSites`, the top 100 records summarizing the number of Copilot agents on sites created in the specified number of days will be displayed with the following properties:

| Property                        | Description                                                     |
|:--------------------------------|:----------------------------------------------------------------|
| Site name                       | The name of the SharePoint site.                                |
| URL                             | The URL of the SharePoint site.                                 |
| Template                        | The Site template of the SharePoint site.                       |
| Site owner                      | Name of the owner of the SharePoint site.                       |
| Copilot agents                  | Number of Copilot agents on the SharePoint site.                |
| Sensitivity                     | The sensitivity label of the SharePoint site.                   |
| Restrict site access enabled    | Restrict site access status (Yes/No) of the SharePoint site.    |
| Restrict site discovery enabled | Restrict site discovery status (Yes/No) of the SharePoint site. |
| External sharing                | External Sharing status (Yes/No) of the SharePoint site.        |

If this cmdlet is executed with `-ReportId` as parameter and `-Content` as `SiteDistribution`, a report showing Copilot distribution across sites in the specified number of days will be displayed with the following properties:

| Property       | Description                                                                                  |
|:---------------|:---------------------------------------------------------------------------------------------|
| Site template  | The Site template of the SharePoint site.                                                    |
| Sites          | Number of sites corresponding to that particular site template.                              |
| Copilot agents | Number of Copilot agents on the SharePoint site corresponding to that particular site template. |

```yaml
Type: SPOCopilotAgentInsightType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named 
Default value: CopilotAgentsOnSites
Accept pipeline input: False
Accept wildcard characters: False
```

### -Action

It determines whether a report would be viewed or downloaded. If the value of `-Action` is set as `View`, it will display the output on the PowerShell screen. Else if the value of `-Action` is set as `Download`, it will download the full report in CSV format to the same path from where the command was run.

```yaml
Type: ActionType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: View
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Start-SPOCopilotAgentInsightsReport](./Start-SPOCopilotAgentInsightsReport.md)