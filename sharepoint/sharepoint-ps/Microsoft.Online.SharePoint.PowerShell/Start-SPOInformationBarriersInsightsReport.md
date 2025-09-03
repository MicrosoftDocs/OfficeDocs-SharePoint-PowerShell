---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/start-spoinformationbarriersinsightsreport
applicable: SharePoint Online
title: Start-SPOInformationBarriersInsightsReport
schema: 2.0.0
author: pvrk
ms.author: pullabhk
manager:
ms.reviewer:
ms.date: 07/15/2025
---

# Start-SPOInformationBarriersInsightsReport

## SYNOPSIS

Generates a new report to identify and discover the usage patterns of Information Barriers (IB) across SharePoint sites and OneDrive accounts in the organization.

## SYNTAX

```
Start-SPOInformationBarriersInsightsReport [-Yes <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates reports to identify [top sites and their IB modes](/purview/information-barriers-insights-report) to help apply suitable controls for the sites as applicable.

## EXAMPLES

### Example 1

```powershell
Start-SPOInformationBarriersInsightsReport -Yes
```

This example generates IB reports without asking for further confirmation.

## PARAMETERS

### -Yes

This parameter provides confirmation to generate the IB report.

```yaml
Type: System.Boolean
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

[Get-SPOInformationBarriersInsightsReport](./Get-SPOInformationBarriersInsightsReport.md)
