---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/start-spoinformationbarriersinsightsreport
applicable: SharePoint Online
title: Start-SPOInformationBarriersInsightsReport
schema: 2.0.0
author: pvrk
ms.author: pullabhk
manager: 
ms.reviewer:
---

# Start-SPOInformationBarriersInsightsReport

## SYNOPSIS

This cmdlet generates reports in information barriers (IB) meant to identify and discover usage patterns across SharePoint sites and OneDrive accounts in the organization.

## SYNTAX

```powershell
Start-SPOInformationBarriersInsightsReport [-Yes <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet would create reports in Information Barriers (IB) to identify top sites and their modes to help apply suitable controls for the sites as applicable.

## EXAMPLES

### Example 1

```powershell
PS C:\> Start-SPOInformationBarriersInsightsReport
```

This PS command would create Information Barriers reports to identify top sites and their modes to help apply suitable controls for the sites as applicable.

## PARAMETERS

### -Yes

This boolean parameter will start generating the IB report.

```yaml
Type: Boolean
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

[Get-SPOInformationBarriersInsightsReport](./Get-SPOInformationBarriersInsightsReport.md)
