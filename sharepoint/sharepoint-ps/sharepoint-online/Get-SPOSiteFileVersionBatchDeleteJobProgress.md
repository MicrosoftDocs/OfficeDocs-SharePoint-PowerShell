---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositefileversionbatchdeletejobprogress
applicable: SharePoint Online
title: Get-SPOSiteFileVersionBatchDeleteJobProgress
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Get-SPOSiteFileVersionBatchDeleteJobProgress

## SYNOPSIS

Gets the progress of a trim job for a site collection.

## SYNTAX

```powershell
Get-SPOSiteFileVersionBatchDeleteJobProgress [-Identity] <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

Gets the progress of a trim job for a site collection.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOSiteFileVersionBatchDeleteJobProgress -Identity https://contoso.sharepoint.com/sites/site1
```

Example 1 gets the progress of a trim job for a site collection.

## PARAMETERS

### -Identity

Specifies the URL of the site collection.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Remove-SPOSiteFileVersionBatchDeleteJob](Remove-SPOSiteFileVersionBatchDeleteJob.md)

[New-SPOSiteFileVersionBatchDeleteJob](New-SPOSiteFileVersionBatchDeleteJob.md)
