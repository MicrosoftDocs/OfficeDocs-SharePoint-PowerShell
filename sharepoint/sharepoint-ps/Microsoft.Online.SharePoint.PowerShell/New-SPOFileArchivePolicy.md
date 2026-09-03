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
New-SPOFileArchivePolicy [-Name <String>] -PolicyType <SPOFileArchivePolicyType> [-LastAccessDateCriteria <Int32>]
 [-FileTypeCriteria <String[]>] [-FileTypeExclusionCriteria <String[]>] [-IsWhatIfMode <Boolean>]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new file archive policy for the connected SharePoint Online tenant. A file archive policy defines the criteria under which files are automatically archived based on their last access date. The policy is created in an Inactive state and must be activated using `Set-SPOFileArchivePolicy` with `-State Active` before it takes effect.

Use `-PolicyType` to choose the scope of the policy: all SharePoint sites in the tenant (`AllSites`), all OneDrive for Business sites in the tenant (`AllODBSites`), or only the sites you explicitly add (`SelectedSites`).

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
New-SPOFileArchivePolicy -PolicyType "SelectedSites" -Name "ArchiveMarketing" -LastAccessDateCriteria 12
```

Creates a new file archive policy named "ArchiveMarketing" that targets only the sites you add with `Add-SPOSiteToFileArchivePolicy`, and archives files not accessed in the last 12 months.

### Example 3

```powershell
New-SPOFileArchivePolicy -PolicyType "AllODBSites" -Name "ArchiveOneDrive"
```

Creates a new file archive policy named "ArchiveOneDrive" that targets all OneDrive for Business sites in the tenant. To exempt individual OneDrive sites, add them as exclusions with `Add-SPOSiteToFileArchivePolicy` and the `-Exclude` parameter.

### Example 4

```powershell
New-SPOFileArchivePolicy -PolicyType "AllSites" -IsWhatIfMode $true
```

Creates a new file archive policy in `WhatIf` mode. When the policy runs, it will report which files would be archived without actually archiving them.

## PARAMETERS

### -FileTypeCriteria

Specifies an array of file extensions to include in the policy, in dot-prefixed format (for example, `.docx`). When omitted, all file types are included.

> [!NOTE]
> File type filtering isn't implemented in the current preview. Supplying this parameter returns the error "Updating file type criteria is not supported. Please remove and recreate the policy." Omit the parameter to create the policy with all file types included.

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

### -FileTypeExclusionCriteria

Specifies an array of file extensions to exclude from the policy, in dot-prefixed format (for example, `.docx`). When omitted, no file types are excluded.

> [!NOTE]
> File type filtering isn't implemented in the current preview. Supplying this parameter returns the error "Updating file type exclusion criteria is not supported. Please remove and recreate the policy." Omit the parameter to create the policy with no file type exclusions.

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

Specifies the scope of the policy. Accepted values are:

- `AllSites`: The policy applies to all SharePoint sites in the tenant.
- `AllODBSites`: The policy applies to all OneDrive for Business sites in the tenant.
- `SelectedSites`: The policy applies only to the sites you explicitly add to it.

If you choose `SelectedSites`, you must add at least one site using `Add-SPOSiteToFileArchivePolicy` before the policy can be activated. If you choose `AllSites` or `AllODBSites`, you can optionally exempt individual sites by adding them with `Add-SPOSiteToFileArchivePolicy` and the `-Exclude` parameter.

```yaml
Type: SPOFileArchivePolicyType
Parameter Sets: (All)
Aliases:
Accepted values: AllSites, SelectedSites, AllODBSites

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

[Get-SPOFileArchivePolicyReport](Get-SPOFileArchivePolicyReport.md)

[Get-SPOFileArchivePolicySites](Get-SPOFileArchivePolicySites.md)

[Remove-SPOFileArchivePolicy](Remove-SPOFileArchivePolicy.md)

[Remove-SPOSiteToFileArchivePolicy](Remove-SPOSiteToFileArchivePolicy.md)

[Set-SPOFileArchivePolicy](Set-SPOFileArchivePolicy.md)
