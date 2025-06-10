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

This cmdlet helps to view the status of the insights on Information Barrier (IB).

## SYNTAX

```powershell
Get-SPOInformationBarriersInsightsReport [-ReportId <Guid>] [-Section <SectionType>] [-Action <ActionType>] [-Service <ServiceType>] [-FullDetails] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet helps to view the details of the specific parameters from the insights report.

## EXAMPLES

### Example 1

```powershell
PS C:\> Get-SPOInformationBarriersInsightsReport -reportId ec65a1cf-9b1a-48c2-a1b4-f923ac4c0776

Content: Explicit, Implicit, Open, OwnerModerated, ModeDistribution
State: Completed
Id: ec65a1cf-9b1a-48c2-a1b4-f923ac4c0776
StartTimeInUtc: 4/25/2023 4:10:16 PM
CompleteTimeInUtc: 4/25/2023 4:10:25 PM
QueuedTimeInUtc: 4/25/2023 4:06:47 PM
```

In the above example, the insights report results are displayed for SharePoint sites included in the organization with an ID of ec65a1cf-9b1a-48c2-a1b4-f923ac4c0776. The values in the Content line represent the modes that have results in the report. If a mode (applicable to SharePoint) isn't listed, there aren't any SharePoint sites in the organization with that mode.

### Example 2

```powershell
PS C:\> Get-SPOInformationBarriersInsightsReport -reportId ec65a1cf-9b1a-48c2-a1b4-f923ac4c0776 -service OneDrive

Content: Explicit, Mixed, Open, OwnerModerated, ModeDistribution
State: Completed
Id: ec65a1cf-9b1a-48c2-a1b4-f923ac4c0776
StartTimeInUtc: 4/25/2023 4:10:16 PM
CompleteTimeInUtc: 4/25/2023 4:10:25 PM
QueuedTimeInUtc: 4/25/2023 4:06:47 PM
```

The above cmdlet helps to view summary of the modes with results for OneDrive sites from the generated report ID. In the above example, the insights report results are displayed for OneDrive accounts included in the organization with an ID of ec65a1cf-9b1a-48c2-a1b4-f923ac4c0776. The values in the Content line represent the modes that have results in the report. If a mode (applicable to OneDrive) isn't listed, there aren't any OneDrive accounts in the organization with that mode.

## PARAMETERS

### -Action

This parameter helps to view or download the results of the insights report.

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Start-SPOInformationBarriersInsightsReport](./Start-SPOInformationBarriersInsightsReport.md)
