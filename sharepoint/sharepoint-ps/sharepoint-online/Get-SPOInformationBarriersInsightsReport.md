---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spoinformationbarriersinsightsreport
applicable: SharePoint Online
title: Get-SPOInformationBarriersInsightsReport
schema: 2.0.0
author: pvrk
ms.author: pullabhk
manager: 
ms.reviewer:
---

# Get-SPOInformationBarriersInsightsReport

## SYNOPSIS

Enables the SharePoint Administrator to check status of all active and completed reports of insights on Information Barriers (IB).

## SYNTAX

```powershell
Get-SPOInformationBarriersInsightsReport [-ReportId <Guid>] [-Section <SectionType>] [-Action <ActionType>] [-Service <ServiceType>] [-FullDetails] [<CommonParameters>]
```

## DESCRIPTION

If this cmdlet is executed without any parameters, it displays the status of all active and completed reports with the following properties:

|Property  |Description  |
|---------|---------|
|Content     | Display the [IB modes](/purview/information-barriers-insights-report) for sites present in the report.      |
|State     | The status of the report.   |
|Id     | The unique Id of the report.     |
|StartTimeInUtc     |  The date and time in UTC when the report creation was started.       |
|CompleteTimeInUtc     |  The date and time in UTC when the report creation was completed.       |
|QueuedTimeInUtc     |   TThe date and time in UTC when the report creation was triggered.      |

## EXAMPLES

### Example 1

```powershell
Get-SPOInformationBarriersInsightsReport -ReportId ec65a1cf-9b1a-48c2-a1b4-f923ac4c0776
```

In the above example, the insights report results are displayed for SharePoint sites included in the organization with given ID.

### Example 2

```powershell
Get-SPOInformationBarriersInsightsReport -ReportId ec65a1cf-9b1a-48c2-a1b4-f923ac4c0776 -service OneDrive
```

This example helps to view summary of the modes with results for OneDrive sites from the generated report ID. In the above example, the insights report results are displayed for OneDrive accounts included in the organization with an ID of ec65a1cf-9b1a-48c2-a1b4-f923ac4c0776. The values in the Content line represent the modes that have results in the report. If a mode (applicable to OneDrive) isn't listed, there aren't any OneDrive accounts in the organization with that mode.

## PARAMETERS

### -Action

Specifies whether the report is displayed in the console or downloaded as a file.

- If set to `View`, the report is displayed directly in the PowerShell window.
- If set to `Download`, the report is saved as a CSV file in the directory where the command is run.

```yaml
Type: ActionType
Parameter Sets: (All)
Aliases:
Accepted values: View, Download

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullDetails

It is an optional parameter and allows to download a CSV file containing up to 1 million records.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportId

It specifies the unique Id of the report to be viewed or downloaded.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Section

This parameters helps to view the details of the specified mode.

```yaml
Type: SectionType
Parameter Sets: (All)
Aliases:
Accepted values: Explicit, Implicit, Open, OwnerModerated, ModeDistribution, Mixed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Service

This parameter helps to identify the type of service to view the summary of the insight report of that specified service.

```yaml
Type: ServiceType
Parameter Sets: (All)
Aliases:
Accepted values: OneDrive, SharePoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Start-SPOInformationBarriersInsightsReport](./Start-SPOInformationBarriersInsightsReport.md)
