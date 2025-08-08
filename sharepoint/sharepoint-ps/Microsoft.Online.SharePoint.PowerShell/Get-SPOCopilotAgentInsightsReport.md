---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
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

```
Get-SPOCopilotAgentInsightsReport [-ReportId <Guid>] [-Action <ActionType>]
 [-Content <SPOCopilotAgentInsightType>] [<CommonParameters>]
```

## DESCRIPTION

If this cmdlet is executed without any parameters, it displays the status of all active and completed reports.

> [!NOTE]
> All reports adhere to any retention timeline as per [Data Access Governance](/sharepoint/data-access-governance-reports).

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOCopilotAgentInsightsReport
```

Example 1 enables administrator to view the status of all active and completed reports.

### EXAMPLE 2

```powershell
Get-SPOCopilotAgentInsightsReport –ReportId 9d946216-afe7-49f5-8267-7b662435c70b
```

Example 2 enables administrator to view the Copilot agent insight report of ReportId: `9d946216-afe7-49f5-8267-7b662435c70b`.

### EXAMPLE 3

```powershell
Get-SPOCopilotAgentInsightsReport – ReportId 9d946216-afe7-49f5-8267-7b662435c70b -Action Download
```

Example 3 enables administrator to download the Copilot agent insight report of ReportId: `9d946216-afe7-49f5-8267-7b662435c70b` to the same path from where the command was run.

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

It specifies the kind of report to view or download. There are 3 kinds of sub-reports: CopilotAgentsOnSites, TopSites, SiteDistribution.

If this cmdlet is executed with `-Content` as `CopilotAgentsOnSites`, a report with list of all sites on which a Copilot agent is created along with the names of the Copilot agent created in the specified number of days will be displayed.

If this cmdlet is executed with `-ReportId` as parameter and `-Content` as `TopSites`, the top 100 records summarizing the number of Copilot agents on sites created in the specified number of days will be displayed.

If this cmdlet is executed with `-ReportId` as parameter and `-Content` as `SiteDistribution`, a report showing Copilot distribution across sites in the specified number of days will be displayed.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SPOCopilotAgentInsightType
Parameter Sets: (All)
Aliases:
Accepted values: CopilotAgentsOnSites, TopSites, SiteDistribution

Required: False
Position: Named
Default value: CopilotAgentsOnSites
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

[Start-SPOCopilotAgentInsightsReport](./Start-SPOCopilotAgentInsightsReport.md)
