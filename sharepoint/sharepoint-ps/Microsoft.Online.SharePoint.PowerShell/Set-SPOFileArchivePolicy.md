---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/set-spofilearchivepolicy
applicable: SharePoint Online
title: Set-SPOFileArchivePolicy
schema: 2.0.0
author: HectorRMota
ms.author: hemota
ms.reviewer:
---

# Set-SPOFileArchivePolicy

## SYNOPSIS

Updates an existing file archive policy.

## SYNTAX

```
Set-SPOFileArchivePolicy -PolicyId <Guid> [-Name <String>] [-PolicyType <SPOFileArchivePolicyType>]
 [-LastAccessDateCriteria <Int32>] [-FileTypeCriteria <String[]>] [-IsWhatIfMode <Boolean>] [-State <SPOFileArchivePolicyState>]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet updates the properties of an existing file archive policy. Only the parameters that are specified will be updated; all other properties remain unchanged. You cannot set the State to `Active` unless the PolicyType is `AllSites` or at least one site has been added to the policy using `Add-SPOSiteToFileArchivePolicy`.

> [!NOTE]
> This cmdlet is part of the file archive policies feature which is currently in preview.

## EXAMPLES

### Example 1

```powershell
Set-SPOFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890" -State "Active"
```

Activates the specified file archive policy.

### Example 2

```powershell
Set-SPOFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890" -Name "Updated Policy Name" -LastAccessDateCriteria 12
```

Updates the display name and changes the last access date criteria to 12 months for the specified policy.

### Example 3

```powershell
Set-SPOFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890" -IsWhatIfMode $true
```

Enables `WhatIf` mode on the specified policy. Future policy runs will report eligible files without archiving them.

## PARAMETERS

### -FileTypeCriteria

Specifies an updated array of file extensions to include in the policy. Only files matching the specified extensions will be considered for archiving. Use the dot-prefixed format. Set to `$null` to include all file types.

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

Specifies whether the policy runs in `WhatIf` mode. When set to `$true`, the policy will evaluate which files meet the archiving criteria and report the results, but will not actually archive any files. When set to `$false`, the policy archives files normally when active.

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

Specifies the updated number of months since a file was last accessed before it becomes eligible for archiving. Valid values range from 6 to 48.

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

Specifies an updated display name for the policy.

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

### -PolicyId

Specifies the unique identifier (GUID) of the policy to update.

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

### -PolicyType

Specifies the updated policy type. Accepted values are `AllSites` (targets all sites in the tenant) and `SelectedSites` (targets only sites explicitly added to the policy).

```yaml
Type: SPOFileArchivePolicyType
Parameter Sets: (All)
Aliases:
Accepted values: AllSites, SelectedSites

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State

Specifies the updated state of the policy. Accepted values are `Active` and `Inactive`. A policy cannot be set to `Active` unless its PolicyType is `AllSites` or at least one site has been added to it.

```yaml
Type: SPOFileArchivePolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Inactive

Required: False
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

[New-SPOFileArchivePolicy](New-SPOFileArchivePolicy.md)

[Remove-SPOFileArchivePolicy](Remove-SPOFileArchivePolicy.md)

[Remove-SPOSiteToFileArchivePolicy](Remove-SPOSiteToFileArchivePolicy.md)
