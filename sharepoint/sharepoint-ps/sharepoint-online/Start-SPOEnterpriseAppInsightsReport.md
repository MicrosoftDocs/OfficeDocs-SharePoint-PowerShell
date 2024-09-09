---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: 
applicable: SharePoint Online
title: Start-SPOEnterpriseAppInsightsReport
schema: 
author: sumikumar
ms.author: sumikumar
ms.reviewer:
manager: hikakar
---
 
# Start-SPOEnterpriseAppInsightsReport

## SYNOPSIS

This cmdlet enables admin to trigger the build of a new third party application insights report for the last N days.

## SYNTAX

```powershell
Start-SPOEnterpriseAppInsightsReport [-Force<SwitchParameter>] [-ReportPeriodInDays <Int>] 
```

## Description

After this cmdlet is executed, the report generation request for the last N days gets queued in the pipeline and the below metadata is displayed with the following properties:
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

Example 1 generates the report for a default duration of 1 day as the parameter ```–ReportPeriodInDays``` is not provided.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Start-SPOEnterpriseAppInsightsReport –ReportPeriodInDays 14
```
Example 2 generates the report for a specified duration of 14 days.

## PARAMETERS

### -Force

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportPeriodInDays

It is an optional parameter, and it specifies the duration of the report in days.
The possible values of ReportPeriodInDays are: 1,7, 14, 28.

 ```yaml
Type: Int
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## CommonParameters

## Related Links
