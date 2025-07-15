---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/new-spolistfileversionbatchdeletejob
applicable: SharePoint Online
title: New-SPOListFileVersionBatchDeleteJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# New-SPOListFileVersionBatchDeleteJob

## SYNOPSIS

Queues a job to trim versions from a document library.

## SYNTAX

### AutomaticTrim
```
New-SPOListFileVersionBatchDeleteJob [-Site] <SpoSitePipeBind> -List <SPOListPipeBind> [-Automatic] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeleteOlderThanDays
```
New-SPOListFileVersionBatchDeleteJob [-Site] <SpoSitePipeBind> -List <SPOListPipeBind>
 [-DeleteBeforeDays <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CountLimits
```
New-SPOListFileVersionBatchDeleteJob [-Site] <SpoSitePipeBind> -List <SPOListPipeBind>
 -MajorVersionLimit <Int32> -MajorWithMinorVersionsLimit <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Queues a job to trim versions from a document library.

Caution: Versions trimmed using this command will be permanently deleted and cannot be recovered from the recycle bin.

## EXAMPLES

### EXAMPLE 1

```powershell
New-SPOListFileVersionBatchDeleteJob -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -DeleteBeforeDays 360
```

Example 1 starts a trim job that will delete all file versions that are over 360 days old in the document library called "Documents".

### EXAMPLE 2

```powershell
New-SPOListFileVersionBatchDeleteJob -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -Automatic
```

Example 2 starts a trim job that will delete file versions that expired and set version expiration time for the ones not expired in the document library called "Documents" based on the automatic backend algorithm.

### EXAMPLE 3

```powershell
New-SPOListFileVersionBatchDeleteJob -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -MajorVersionLimit 30 -MajorWithMinorVersionsLimit 10
```

Example 3 starts a trim job that will delete file versions in the document library called "Documents" based on the version count limits.

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

### -Site

Specifies the URL of the site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
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

[Get-SPOListFileVersionBatchDeleteJobProgress](Get-SPOListFileVersionBatchDeleteJobProgress.md)

[Remove-SPOListFileVersionBatchDeleteJob](Remove-SPOListFileVersionBatchDeleteJob.md)
