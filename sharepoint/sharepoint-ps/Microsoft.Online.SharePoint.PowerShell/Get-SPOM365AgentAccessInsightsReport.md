---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-SPOM365AgentAccessInsightsReport 
applicable: SharePoint Online
title: Get-SPOM365AgentAccessInsightsReport
schema: 2.0.0
author: gchaudhary
ms.author: gchaudhary
ms.reviewer:
manager: lokeshgoel
---

# Get-SPOM365AgentAccessInsightsReport

## SYNOPSIS

This cmdlet enables the administrator to check status of all active and available reports when no report ID is present and to view or download a report if report ID is present.

> [!NOTE]
> The feature associated with this cmdlet will be rolling out soon.

## SYNTAX

```
Get-SPOM365AgentAccessInsightsReport [-ReportId <Guid>] [-Action <ActionType>]
 [-Content <SPOCopilotAgentInsightType>] [<CommonParameters>]
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

### EXAMPLE 1

```powershell
Get-SPOM365AgentAccessInsightsReport
```

Example 1 enables administrator to view the status of all active and completed reports.

### EXAMPLE 2

```powershell
Get-SPOM365AgentAccessInsightsReport –ReportId 9d946216-afe7-49f5-8267-7b662435c70b
```

Example 2 enables administrator to view the M365 agent insight report of ReportId: `9d946216-afe7-49f5-8267-7b662435c70b`.

### EXAMPLE 3

```powershell
Get-SPOM365AgentAccessInsightsReport – ReportId 9d946216-afe7-49f5-8267-7b662435c70b -Action Download
```

Example 3 enables administrator to download the M365 agent insight report of ReportId: `9d946216-afe7-49f5-8267-7b662435c70b` to the same path from where the command was run.

## PARAMETERS

### -Action

> Applicable: SharePoint Online

It determines whether a report would be viewed or downloaded. If the value of `-Action` is set as `View`, it will display the output on the PowerShell screen. Else if the value of `-Action` is set as `Download`, it will download the full report in CSV format to the same path from where the command was run.

```yaml
Type: ActionType
Parameter Sets: (All)
Aliases:
Accepted values: View, Download

Required: False
Position: Named
Default value: View
Accept pipeline input: False
Accept wildcard characters: False
```

### -Content

> Applicable: SharePoint Online

It specifies the kind of report to view or download. There are 2 kinds of sub-reports: M365AgentsOnSites, SiteDistribution.

If this cmdlet is executed with `-Content` as `M365AgentsOnSites`, a report with list of all sites on which a agent is created along with the names of the agent created in the specified number of days will be displayed with the following properties:

| Property                        | Description                                                     |
|:--------------------------------|:----------------------------------------------------------------|
| Site ID                         | The unique identifier (GUID) of the SharePoint site.            |
| Site name                       | The name of the SharePoint site.                                |
| URL                             | The URL of the SharePoint site.                                 |
| Type                            | The type of the SharePoint site.                                |
| Site owner                      | Name of the owner of the SharePoint site.                       |
| Request Volume                  | Total requests made by agents to the site.                      |
| Agents Found                    | Total agents found accessing the site.                          |
| Restrict site access enabled    | Restrict site access status (Yes/No) of the SharePoint site.    |
| Restrict site discovery enabled | Restrict site discovery status (Yes/No) of the SharePoint site. |
| External sharing                | External Sharing status (Yes/No) of the SharePoint site.        |
| Sensitivity                     | The sensitivity label of the SharePoint site.                   |
| Agents Details                  | The list of agent details.                                      |

The list of Agent Details would have follwing properties for each agent. This list would have a cap of 20 agents per site.

| Property                        | Description                                                     |
|:--------------------------------|:----------------------------------------------------------------|
| Agent ID                        | The unique identifier of the agent.                             |
| Agent Name                      | The name of the agent.                                          |
| Agent Type                      | The type of the agent (e.g., Declarative, Custom, etc.)         |
| Request Volume                  | Total requests made by this agent to the site.                  |

If this cmdlet is executed with `-ReportId` as parameter and `-Content` as `SiteDistribution`, a report showing M365 agents distribution across sites in the specified number of days will be displayed with the following properties:

| Property       | Description                                                                                  |
|:---------------|:---------------------------------------------------------------------------------------------|
| Site template  | The Site template of the SharePoint site.                                                    |
| Sites          | Number of sites corresponding to that particular site template.                              |
| M365 agents    | Number of M365 agents on the SharePoint site corresponding to that particular site template. |

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SPOM365AgentInsightType
Parameter Sets: (All)
Aliases:
Accepted values: M365AgentsOnSites, SiteDistribution

Required: False
Position: Named
Default value: M365AgentsOnSites
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportId

> Applicable: SharePoint Online

It specifies the unique Id of the report to be viewed or downloaded.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Start-SPOM365AgentAccessInsightsReport](./Start-SPOM365AgentAccessInsightsReport.md)
