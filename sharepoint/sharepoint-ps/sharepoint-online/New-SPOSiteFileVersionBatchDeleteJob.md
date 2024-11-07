---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/new-spositefileversionbatchdeletejob
applicable: SharePoint Online
title: New-SPOSiteFileVersionBatchDeleteJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# New-SPOSiteFileVersionBatchDeleteJob

## SYNOPSIS

Queues a job to trim versions for all document libraries in a site collection.

## SYNTAX

```powershell
New-SPOSiteFileVersionBatchDeleteJob [-Identity] <SpoSitePipeBind> [-Automatic] [-DeleteBeforeDays <Int32>] [-MajorVersionLimit <Int32>] [-MajorWithMinorVersionsLimit <Int32>] [<CommonParameters>]
```

## DESCRIPTION

Queues a job to trim versions for all document libraries in a site collection.

Caution: Versions deleted using this cmdlet will be permanently deleted and cannot be recovered from the recycle bin.

## EXAMPLES

### EXAMPLE 1

```powershell
New-SPOSiteFileVersionBatchDeleteJob -Identity https://contoso.sharepoint.com/sites/site1 -DeleteBeforeDays 360
```

Example 1 starts a trim job that will delete all file versions that are over 360 days old in all document libraries in the site collection.

### EXAMPLE 2

```powershell
New-SPOSiteFileVersionBatchDeleteJob -Identity https://contoso.sharepoint.com/sites/site1 -Automatic
```

Example 2 starts a trim job that will delete file versions that expired and set version expiration time for the ones not expired in the site collection based on the backend algorithm.

### EXAMPLE 3

```powershell
New-SPOSiteFileVersionBatchDeleteJob -Identity https://contoso.sharepoint.com/sites/site1 -MajorVersionLimit 30 -MajorWithMinorVersionsLimit 10
```

Example 3 starts a trim job that will delete file versions in the site collection based on the version count limits.

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

### -Automatic
Trim file versions using automatic version history limit algorithm.

```yaml
Type: SwitchParameter
Parameter Sets: AutomaticTrim

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteBeforeDays
The minimum age of file versions to trim. In other words, all file versions that are older than this number of days will be deleted.

```yaml
Type: int
Parameter Sets: DeleteOlderThanDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorVersionLimit
Trim file version using version count limits. Need to specify `MajorWithMinorVersionsLimit` as well.

```yaml
Type: int
Parameter Sets: CountLimits

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorWithMinorVersionsLimit
Trim file version using version count limits. Need to specify `MajorVersionLimit` as well.

```yaml
Type: int
Parameter Sets: CountLimits

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Get-SPOSiteFileVersionBatchDeleteJobProgress](Get-SPOSiteFileVersionBatchDeleteJobProgress.md)

[Remove-SPOSiteFileVersionBatchDeleteJob](Remove-SPOSiteFileVersionBatchDeleteJob.md)
