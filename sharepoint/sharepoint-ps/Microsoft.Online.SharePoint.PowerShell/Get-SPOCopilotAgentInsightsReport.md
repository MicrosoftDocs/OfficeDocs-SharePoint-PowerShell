---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spocopilotagentinsightsreport
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

Specifies the type of report to view or download. Valid values are:

- `CopilotAgentsOnSites`: Displays a report listing all sites where a Copilot agent was created within the specified number of days. Includes the names of the agents created.
- `TopSites`: Displays the top 100 sites with the highest number of Copilot agents created within the specified number of days.
- `SiteDistribution`: Displays a report showing how Copilot agents are distributed across sites within the specified number of days.

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
