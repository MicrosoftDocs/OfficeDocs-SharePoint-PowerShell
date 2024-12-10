---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/start-spocopilotagentinsightsreport
applicable: SharePoint Online
title: Start-SPOCopilotAgentInsightsReport
schema: 2.0.0
author: bhagatshweta
ms.author: bhagatshweta
ms.reviewer:
manager: hikakar
---
 
# Start-SPOCopilotAgentInsightsReport

## SYNOPSIS

This cmdlet enables administrator to trigger the build of a new Copilot Agent Insight report for the last N days.

## SYNTAX

```powershell
Start-SPOCopilotAgentInsightsReport [-ReportPeriodInDays <Int>] [-Force <SwitchParameter>]
```

## DESCRIPTION

After this cmdlet is executed, the Copilot Agent Insight report generation request for the last N days gets queued in the pipeline and the below metadata is displayed with the following properties:

| Property             | Description                                                 |
|:---------------------|:------------------------------------------------------------|
| Id                   | The unique Id of the report.                                |
| CreatedDateTimeInUtc | The date and time the report creation was triggered in UTC. |
| Status               | The status of the report.                                   |
| ReportPeriodInDays   | The report duration in days.                                |

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Start-SPOCopilotAgentInsightsReport
```

Example 1 generates the Copilot agent insights report for a default duration of 1 day as the parameter `–ReportPeriodInDays` is not provided.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Start-SPOCopilotAgentInsightsReport –ReportPeriodInDays 14
```

Example 2 generates the Copilot Agent insights report for a specified duration of 14 days.

## PARAMETERS

### -ReportPeriodInDays

It is an optional parameter, and it specifies the duration of the Copilot Agent insights report in days. The possible values of ReportPeriodInDays are: 1, 7, 14, 28. If this parameter is not provided, it generates the report for a default duration of 1 day.

```yaml
Type: Int
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False 
```

### -Force

It is an optional parameter which is used to bypass confirmation prompts and execute the command without interruptions.

```yaml
Type: SwitchParameter
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

## Related Links

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOCopilotAgentInsightsReport](./Get-SPOCopilotAgentInsightsReport.md)