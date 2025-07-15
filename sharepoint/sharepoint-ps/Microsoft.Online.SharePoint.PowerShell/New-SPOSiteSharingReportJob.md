---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://docs.microsoft.com/powershell/module/sharepoint-online/New-SPOSiteSharingReportJob
applicable: SharePoint Online
title: New-SPOSiteSharingReportJob
schema: 2.0.0
author: salarson
ms.author: salarson
ms.reviewer:
---

# New-SPOSiteSharingReportJob

## SYNOPSIS

Creates a new sharing report job.

## SYNTAX

```
New-SPOSiteSharingReportJob [-Site] <SpoSitePipeBind> [-ReportStorageWebUrl] <String>
 [-ReportStorageFolderUrl] <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is not currently active in Production and may be removed in the future. You will receive the error, "Site collection sharing report feature has not been enabled", if you run this cmdlet which is currently by design.

## EXAMPLES

### EXAMPLE 1

```powershell
$site = Get-SPOSite -Identity https://contoso.sharepoint.com/sites/site1

New-SPOSiteSharingReportJob -Site $site -ReportStorageWebUrl 'https://contoso.sharepoint.com/sites/site2/web1' -ReportStorageFolderUrl '/Documents/folder'
```

## PARAMETERS

### -ReportStorageFolderUrl

Location to where the report will be exported.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportStorageWebUrl

Report web storage URL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site

Specifies the site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 0
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
