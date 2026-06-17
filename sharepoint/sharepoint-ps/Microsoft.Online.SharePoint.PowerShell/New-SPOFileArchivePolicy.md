---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/new-spofilearchivepolicy
applicable: SharePoint Online
title: New-SPOFileArchivePolicy
schema: 2.0.0
author: HectorRMota
ms.author: hemota
ms.reviewer:
---

# New-SPOFileArchivePolicy

## SYNOPSIS

Creates a new file archive policy for the tenant.

## SYNTAX

```
New-SPOFileArchivePolicy [-Name <String>] -PolicyType <String> [-LastAccessDateCriteria <Int32>]
 [-FileTypeCriteria <String[]>] [-IsWhatIfMode <Boolean>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new file archive policy for the connected SharePoint Online tenant. A file archive policy defines the criteria under which files are automatically archived based on their last access date. The policy is created in an Inactive state and must be activated using `Set-SPOFileArchivePolicy` with `-State Active` before it takes effect.

> [!NOTE]
> This cmdlet is part of the file archive policies feature which is currently in preview.

## EXAMPLES

### Example 1

```powershell
New-SPOFileArchivePolicy -PolicyType "AllSites" -Name "ArchiveAll"
```

Creates a new file archive policy named "ArchiveAll" that targets all sites in the tenant, using the default last access date criteria of 24 months.

### Example 2

```powershell
New-SPOFileArchivePolicy -PolicyType "SelectedSites" -Name "ArchiveMarketing" -LastAccessDateCriteria 12 -FileTypeCriteria ".docx", ".pptx", ".xlsx"
```

Creates a new file archive policy named "ArchiveMarketing" that targets selected sites, archives files not accessed in the last 12 months, and only applies to .docx, .pptx, and .xlsx file types.

### Example 3

```powershell
New-SPOFileArchivePolicy -PolicyType "AllSites" -IsWhatIfMode $true
```

Creates a new file archive policy in `WhatIf` mode. When the policy runs, it will report which files would be archived without actually archiving them.

## PARAMETERS

### -FileTypeCriteria

Specifies an array of file extensions to include in the policy. Only files matching the specified extensions will be considered for archiving. Use the dot-prefixed format. If not specified, all file types are included.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsWhatIfMode

Specifies whether the policy runs in `WhatIf` mode. When set to `$true`, the policy will evaluate which files meet the archiving criteria and report the results, but will not actually archive any files. When set to `$false` or not specified, the policy archives files normally when active.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LastAccessDateCriteria

Specifies the number of months since a file was last accessed before it becomes eligible for archiving. Valid values range from 6 to 48. The default value is 24 months.

> [!IMPORTANT]
> The last access date is accurate starting July 2025. Dates before that may be missing access signals from some clients. For critical data, ensure your criteria doesn't archive based on last access dates before July 2025.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies a display name for the policy. If not specified, defaults to "MyPolicy".

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyType

Specifies whether the policy targets all sites in the tenant or only selected sites. Accepted values are `AllSites` and `SelectedSites`. If `SelectedSites` is chosen, you must add at least one site using `Add-SPOSiteToFileArchivePolicy` before the policy can be activated.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AllSites, SelectedSites

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
