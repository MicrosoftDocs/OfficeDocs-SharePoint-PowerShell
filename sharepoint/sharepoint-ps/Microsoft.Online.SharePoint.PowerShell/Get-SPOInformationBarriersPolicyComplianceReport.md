---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spoinformationbarrierspolicycompliancereport
applicable: SharePoint Online
title: Get-SPOInformationBarriersPolicyComplianceReport
schema: 2.0.0
author: srmuppana
ms.author: srmuppana
manager: dbolick
ms.reviewer: nibandyo
---

# Get-SPOInformationBarriersPolicyComplianceReport

## SYNOPSIS

Gets the status and results of Information Barriers policy compliance reports.

## SYNTAX

```
Get-SPOInformationBarriersPolicyComplianceReport [-ReportID <Guid>] [<CommonParameters>]
```

## DESCRIPTION

When you run this cmdlet without parameters, it returns the status and metadata of all Information Barriers policy compliance reports.

When you specify `-ReportID`, the cmdlet returns the metadata and content of that report. The content identifies SharePoint sites, OneDrive accounts, and user-owned SharePoint Embedded containers that are noncompliant with current Information Barriers policies.

The cmdlet can return the following properties:

| Property | Description |
|----------|-------------|
| Content | The noncompliant SharePoint sites, OneDrive accounts, and user-owned SharePoint Embedded containers in the specified completed report. |
| HasNonCompliantSites | Indicates whether the specified report contains noncompliant sites, accounts, or containers. |
| State | The status of the report. |
| Id | The unique ID of the report. |
| StartTimeInUtc | The date and time in UTC when report generation started. |
| CompleteTimeInUtc | The date and time in UTC when report generation completed. |
| QueuedTimeInUtc | The date and time in UTC when report generation was queued. |
| UpdateOneDriveSegments | Indicates whether the report was configured to update noncompliant OneDrive segments automatically. |
| UpdateUserOwnedContainerSegments | Indicates whether the report was configured to update noncompliant user-owned SharePoint Embedded container segments automatically. |

## EXAMPLES

### Example 1

```powershell
Get-SPOInformationBarriersPolicyComplianceReport
```

This example gets the status and metadata of all Information Barriers policy compliance reports.

### Example 2

```powershell
Get-SPOInformationBarriersPolicyComplianceReport -ReportID beedfc3e-850c-4ca2-9ae0-7eacbe529d77
```

This example gets the metadata and noncompliant content of the specified report.

### Example 3

```powershell
$report = Get-SPOInformationBarriersPolicyComplianceReport -ReportID beedfc3e-850c-4ca2-9ae0-7eacbe529d77
$report.Content
```

This example gets a specific report and displays the compliance details for each noncompliant SharePoint site, OneDrive account, or user-owned SharePoint Embedded container.

## PARAMETERS

### -ReportID

Specifies the unique identifier of a report. If you don't specify this parameter, the cmdlet returns the status and metadata of all reports.

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## RELATED LINKS

[Start-SPOInformationBarriersPolicyComplianceReport](./Start-SPOInformationBarriersPolicyComplianceReport.md)

[Create an Information Barriers policy compliance report](/purview/information-barriers-sharepoint-report)
