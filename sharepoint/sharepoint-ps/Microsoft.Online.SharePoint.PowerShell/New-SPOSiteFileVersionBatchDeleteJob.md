---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
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

### AutomaticTrim
```
New-SPOSiteFileVersionBatchDeleteJob [-Identity] <SpoSitePipeBind> [-Automatic] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DeleteOlderThanDays
```
New-SPOSiteFileVersionBatchDeleteJob [-Identity] <SpoSitePipeBind> [-DeleteBeforeDays <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### CountLimits
```
New-SPOSiteFileVersionBatchDeleteJob [-Identity] <SpoSitePipeBind> -MajorVersionLimit <Int32>
 -MajorWithMinorVersionsLimit <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
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

### -Automatic
Trim file versions using automatic version history limit algorithm.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutomaticTrim
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteBeforeDays
The minimum age of file versions to trim. In other words, all file versions that are older than this number of days will be deleted.

```yaml
Type: System.Int32
Parameter Sets: DeleteOlderThanDays
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Online

Specifies the URL of the site collection.

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

### -MajorVersionLimit
Trim file version using version count limits. Need to specify `MajorWithMinorVersionsLimit` as well.

```yaml
Type: System.Int32
Parameter Sets: CountLimits
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorWithMinorVersionsLimit
Trim file version using version count limits. Need to specify `MajorVersionLimit` as well.

```yaml
Type: System.Int32
Parameter Sets: CountLimits
Aliases:

Required: True
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

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOSiteFileVersionBatchDeleteJobProgress](Get-SPOSiteFileVersionBatchDeleteJobProgress.md)

[Remove-SPOSiteFileVersionBatchDeleteJob](Remove-SPOSiteFileVersionBatchDeleteJob.md)
