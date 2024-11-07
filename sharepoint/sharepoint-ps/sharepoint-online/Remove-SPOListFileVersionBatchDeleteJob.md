---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spolistfileversionbatchdeletejob
applicable: SharePoint Online
title: Remove-SPOListFileVersionBatchDeleteJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Remove-SPOListFileVersionBatchDeleteJob

## SYNOPSIS

Cancels further processing of a trim job for a document library.

## SYNTAX

```powershell
Remove-SPOListFileVersionBatchDeleteJob [-Site] <SpoSitePipeBind> [-List] <SpoListPipeBind> [<CommonParameters>]
```

## DESCRIPTION

Cancels further processing of a trim job for a document library. This will stop the ongoing version deletion trim job and no further deletions will happen. Stopping a trim job will not impact versions that have already been permanently deleted when the job was in progress.

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOListFileVersionBatchDeleteJob -Site https://contoso.sharepoint.com/sites/site1 -List "Documents"
```

Example 1 cancels further processing of the trim job for a document library called "Documents".

## PARAMETERS

### -Site

Specifies the URL of the site.

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

### -List

The document library name or Id.

```yaml
Type: SPOListPipeBind
Parameter Sets: (All)

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Get-SPOListFileVersionBatchDeleteJobProgress](Get-SPOListFileVersionBatchDeleteJobProgress.md)

[New-SPOListFileVersionBatchDeleteJob](New-SPOListFileVersionBatchDeleteJob.md)
