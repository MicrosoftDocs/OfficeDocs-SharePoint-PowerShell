---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: 
applicable: SharePoint Online
title: Start-SPOEnterpriseAppInsightsReport
schema: 2.0.0
author: sumikumar
ms.author: sumikumar
ms.reviewer:
manager: hikakar
---
 
# Start-SPOEnterpriseAppInsightsReport

## SYNOPSIS

This cmdlet enables admin to trigger the build of a new Enterprise Application Insights report for the last N days.

## SYNTAX

```powershell
Start-SPOEnterpriseAppInsightsReport [-Force <SwitchParameter>] [-ReportPeriodInDays <Int>] 
```

## Description

After this cmdlet is executed, the Enterprise Application Insights report generation request for the last N days gets queued in the pipeline and the below metadata is displayed with the following properties:
| Property             | Description                              |
| :------------------- | :--------------------------------------- |
| Id | The unique Id of the report.                    |
| CreatedDateTimeInUtc | The Date and Time the report creation was triggered in UTC.                   |
| Status | The Status of the report.               |
| ReportPeriodInDays | The report duration in days.       |

## Example

### -----------------------EXAMPLE 1-----------------------------

```powershell
Start-SPOEnterpriseAppInsightsReport
```

Example 1 generates the Enterprise Application Insights report for a default duration of 1 day as the parameter `–ReportPeriodInDays` is not provided.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Start-SPOEnterpriseAppInsightsReport –ReportPeriodInDays 14
```
Example 2 generates the Enterprise Application Insights report for a specified duration of 14 days.

## PARAMETERS

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

### -ReportPeriodInDays

It is an optional parameter, and it specifies the duration of the Enterprise Application Insights report in days. The possible values of ReportPeriodInDays are: 1, 7, 14, 28. If this parameter is not provided, it generates the report for a default duration of 1 day.

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

## CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Related Links

[Get started with SharePoint Online Management Shell](https://learn.microsoft.com/en-us/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOEnterpriseAppInsightsReport](https://learn.microsoft.com/en-us/powershell/sharepoint/sharepoint-online/get-spoenterpriseappinsightsreport)