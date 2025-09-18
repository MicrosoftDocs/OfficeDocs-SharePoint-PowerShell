---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-SPOM365AgentAccessInsightsReport 
applicable: SharePoint Online
title: Get-SPOM365AgentAccessInsightsReport
schema: 2.0.0
author: starringGTM
ms.author: gchaudhary
ms.reviewer:
---

# Get-SPOM365AgentAccessInsightsReport

## SYNOPSIS

This cmdlet enables the administrator to check status of all active and available analytics reports when no report ID is present and to view or download a report if report ID is present.

> [!NOTE]
> The feature associated with this cmdlet will be rolling out soon.

## SYNTAX

```
Get-SPOM365AgentAccessInsightsReport [-ReportId <Guid>] [-Action <ActionType>]
 [-Content <M365AgentsOnSites>] [<CommonParameters>]
```

## DESCRIPTION

If this cmdlet is executed without any parameters, it displays the status of all active and completed reports.
> [!NOTE]
> All reports adhere to any retention timeline as per [Data Access Governance](/sharepoint/data-access-governance-reports).

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOM365AgentAccessInsightsReport
```

Example 1 enables administrator to view the status of all active and completed analytics reports.

### EXAMPLE 2

```powershell
Get-SPOM365AgentAccessInsightsReport –ReportId 9d946216-afe7-49f5-8267-7b662435c70b
```

Example 2 enables administrator to view the Microsoft 365 agent insight report of the given report ID.

### EXAMPLE 3

```powershell
Get-SPOM365AgentAccessInsightsReport – ReportId 9d946216-afe7-49f5-8267-7b662435c70b -Action Download
```

Example 3 enables administrator to download the Microsoft 365 agent insight report of the given report ID to the same path from where the command was run.

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

It specifies the kind of report to view or download.

If this cmdlet is executed with `-Content` as `M365AgentsOnSites`, a report with list of all sites on which a agent is created along with the names of the agent created in the specified number of days will be displayed.

If this cmdlet is executed with `-ReportId` as parameter and `-Content` as `SiteDistribution`, a report showing Microsoft 365 agents distribution across sites in the specified number of days will be displayed.

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

It specifies the unique ID of the report to be viewed or downloaded.

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
