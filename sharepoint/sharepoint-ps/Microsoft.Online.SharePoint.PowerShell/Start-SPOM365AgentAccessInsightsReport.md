---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/start-spom365agentaccessinsightsreport
applicable: SharePoint Online
title: Start-SPOM365AgentAccessInsightsReport
schema: 2.0.0
author: starringGTM
ms.author: gchaudhary
ms.reviewer:
---

 # Start-SPOM365AgentAccessInsightsReport

## SYNOPSIS

Using this cmdlet, administrators may trigger the build of a new Microsoft 365 agent insight report for the specified number of days.

> [!NOTE]
> The feature associated with this cmdlet will be rolling out soon.

## SYNTAX

```
Start-SPOM365AgentAccessInsightsReport [-Force] [-ReportPeriodInDays <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

After executing this cmdlet, the Microsoft 365 agent insight report generation request for the specified number of days is added to the pipeline queue.

## EXAMPLES

### EXAMPLE 1

```powershell
Start-SPOM365AgentAccessInsightsReport
```

Example 1 generates the Microsoft 365 agent insight report for a default duration of 1 day since the parameter `–ReportPeriodInDays` is not provided.

### EXAMPLE 2

```powershell
Start-SPOM365AgentAccessInsightsReport –ReportPeriodInDays 14
```

Example 2 generates the Copilot agent insight report for a specified duration of 14 days.

## PARAMETERS

### -Force

> Applicable: SharePoint Online

It is an optional parameter which is used to bypass confirmation prompts and execute the command without interruptions.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportPeriodInDays

> Applicable: SharePoint Online

It specifies the duration of the M365 agent insight report in days. The possible values of ReportPeriodInDays are: 1, 7, 14, 28. If this parameter is not provided, it generates the report for a default duration of 1 day.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)


[Get-SPOM365AgentAccessInsightsReport](./Get-SPOM365AgentAccessInsightsReport.md)

