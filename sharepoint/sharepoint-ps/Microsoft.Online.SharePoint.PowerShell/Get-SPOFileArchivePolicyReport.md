---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spofilearchivepolicyreport
applicable: SharePoint Online
title: Get-SPOFileArchivePolicyReport
schema: 2.0.0
author: HectorRMota
ms.author: hemota
ms.reviewer:
---

# Get-SPOFileArchivePolicyReport

## SYNOPSIS

Gets run reports for a file archive policy.

## SYNTAX

```
Get-SPOFileArchivePolicyReport -PolicyId <Guid> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet retrieves the run reports for a file archive policy. Reports are kept for the past 12 months and include details about each policy run such as how many sites were processed, how many files were archived, and the total storage archived.

For policies running in `WhatIf` mode, reports show how many files and how much storage would have been archived instead.

> [!NOTE]
> This cmdlet is part of the file archive policies feature which is currently in preview.

## EXAMPLES

### Example 1

```powershell
Get-SPOFileArchivePolicyReport -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890"
```

Returns all run reports for the specified file archive policy from the past 12 months.

## PARAMETERS

### -PolicyId

Specifies the unique identifier (GUID) of the policy to retrieve run reports for.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-SPOSiteToFileArchivePolicy](Add-SPOSiteToFileArchivePolicy.md)

[Get-SPOFileArchivePolicy](Get-SPOFileArchivePolicy.md)

[Get-SPOFileArchivePolicySites](Get-SPOFileArchivePolicySites.md)

[New-SPOFileArchivePolicy](New-SPOFileArchivePolicy.md)

[Remove-SPOFileArchivePolicy](Remove-SPOFileArchivePolicy.md)

[Remove-SPOSiteToFileArchivePolicy](Remove-SPOSiteToFileArchivePolicy.md)

[Set-SPOFileArchivePolicy](Set-SPOFileArchivePolicy.md)
