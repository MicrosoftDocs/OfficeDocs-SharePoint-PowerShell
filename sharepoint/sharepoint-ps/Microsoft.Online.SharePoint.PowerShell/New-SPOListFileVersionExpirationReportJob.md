---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/new-spolistfileversionexpirationreportjob
applicable: SharePoint Online
title: New-SPOListFileVersionExpirationReportJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# New-SPOListFileVersionExpirationReportJob

## SYNOPSIS

Starts generating file version expiration report for a document library.

## SYNTAX

```
New-SPOListFileVersionExpirationReportJob [-Site] <SpoSitePipeBind> -List <SPOListPipeBind> -ReportUrl <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starts generating file version expiration report for a document library.

## EXAMPLES

### EXAMPLE 1

```powershell
New-SPOListFileVersionExpirationReportJob -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -ReportUrl "https://contoso.sharepoint.com/sites/sites1/reports/MyReports/VersionReport.csv"
```

Example 1 starts generating file version expiration report on for the document library called "Documents", saving the result to a csv file within the site.

## PARAMETERS

### -List

The document library name or Id.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOListPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReportUrl

The URL of the report to save to.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site

> Applicable: SharePoint Online

Specifies the URL of the site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

### Microsoft.Online.SharePoint.PowerShell.SPOListPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOListFileVersionExpirationReportJobProgress](Get-SPOListFileVersionExpirationReportJobProgress.md)
