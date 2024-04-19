---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spositefileversionbatchdeletejob
applicable: SharePoint Online
title: Remove-SPOSiteFileVersionBatchDeleteJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Remove-SPOSiteFileVersionBatchDeleteJob

## SYNOPSIS

> [!NOTE]
> This feature is part of the version history controls preview. If your tenant is not part of the preview or the feature has not rolled out to your tenant, you will get an error when trying to run this cmdlet.

Cancels further processing of a file version batch trim job for a site collection.

## SYNTAX

```powershell
Remove-SPOSiteFileVersionBatchDeleteJob [-Identity] <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

Cancels further processing of a file version batch trim job for a site collection. This will stop the ongoing version deletion trim job and no further deletions will happen. Stopping a trim job will not impact versions that have already been permanently deleted when the job was in progress.

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOSiteFileVersionBatchDeleteJob -Identity https://contoso.sharepoint.com/sites/site1
```

Example 1 cancels further processing of the file version batch trim job for the site collection.

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

[Get-SPOSiteFileVersionBatchDeleteJobProgress](Get-SPOSiteFileVersionBatchDeleteJobProgress.md)

[New-SPOSiteFileVersionBatchDeleteJob](New-SPOSiteFileVersionBatchDeleteJob.md)