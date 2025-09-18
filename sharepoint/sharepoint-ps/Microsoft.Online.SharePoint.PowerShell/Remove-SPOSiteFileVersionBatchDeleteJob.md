---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/remove-spositefileversionbatchdeletejob
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

Stops further processing of site level trim job that is in-progress.

## SYNTAX

```
Remove-SPOSiteFileVersionBatchDeleteJob [-Identity] <SpoSitePipeBind> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Stops further processing of site level trim job that is in-progress.

Once the cmdlet executes successfully, all new asynchronous version deletion will be stopped. Stopping a trim job will not impact versions that have already been permanently deleted when the job was in progress.

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOSiteFileVersionBatchDeleteJob -Identity https://contoso.sharepoint.com/sites/site1
```

Example 1 cancels further processing of the trim job for the site collection.

## PARAMETERS

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

[New-SPOSiteFileVersionBatchDeleteJob](New-SPOSiteFileVersionBatchDeleteJob.md)
