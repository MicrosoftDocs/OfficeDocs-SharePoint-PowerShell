---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: microsoft.online.sharepoint.powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spoversionpolicywithchanges
applicable: SharePoint Online
title: Get-SPOVersionPolicyWithChanges
schema: 2.0.0
author: blarrywangmsft
ms.author: blarrywang
ms.reviewer:
---

# Get-SPOVersionPolicyWithChanges

## SYNOPSIS

Returns a locally modified copy of a version policy.

## SYNTAX

### Default (Default)
```
Get-SPOVersionPolicyWithChanges -VersionPolicy <SPOFileVersionPolicySettings> [-MajorVersionLimit <Int32>]
 [-ExpireVersionsAfterDays <Int32>] [-EnableAutoExpirationVersionTrim <Boolean>] [<CommonParameters>]
```

### FileType
```
Get-SPOVersionPolicyWithChanges -VersionPolicy <SPOFileVersionPolicySettings> -FileType <String>
 [-MajorVersionLimit <Int32>] [-ExpireVersionsAfterDays <Int32>]
 [-EnableAutoExpirationVersionTrim <Boolean>] [<CommonParameters>]
```

### FileTypeRemove
```
Get-SPOVersionPolicyWithChanges -VersionPolicy <SPOFileVersionPolicySettings> -FileType <String> [-Remove]
 [<CommonParameters>]
```

## DESCRIPTION

Returns a modified copy of the given version policy. This cmdlet is intended to be used in a pipeline with `Get-SPOTenantVersionPolicy` to build a modified policy that can then be passed to `New-SPOTenantApplyFileVersionPolicyJob` or `Get-SPOTenantApplyFileVersionPolicyJobImpact`.

When `-FileType` is omitted, the default policy settings are modified. When `-FileType` is specified, the per-file-type override for that type is created or updated. For supported file type names, see [File type version limits in SharePoint](/sharepoint/file-type-version-limits).

Use `-Remove` with `-FileType` to delete a per-file-type override.

## EXAMPLES

### Example 1
```powershell
Get-SPOTenantVersionPolicy | Get-SPOVersionPolicyWithChanges -MajorVersionLimit 100
```

Retrieves the current tenant version policy and returns a copy with the default major version limit changed to 100.

### Example 2
```powershell
Get-SPOTenantVersionPolicy | Get-SPOVersionPolicyWithChanges -FileType "video" -MajorVersionLimit 50 -ExpireVersionsAfterDays 180
```

Retrieves the current tenant version policy and returns a copy with a per-file-type override for `video` files that limits to 50 major versions and expires versions after 180 days.

### Example 3
```powershell
Get-SPOTenantVersionPolicy | Get-SPOVersionPolicyWithChanges -FileType "video" -Remove
```

Retrieves the current tenant version policy and returns a copy with the `video` file type override removed, so `video` files will fall back to the default policy.

## PARAMETERS

### -EnableAutoExpirationVersionTrim
When `$true`, uses automatic expiration, where Microsoft manages the expiration schedule. When `$false`, uses the manual expiration schedule defined by `-MajorVersionLimit` and `-ExpireVersionsAfterDays`.

When `EnableAutoExpirationVersionTrim` is `$true`, `MajorVersionLimit` is always 500 and `ExpireVersionsAfterDays` is always 30. As a result, switching `-EnableAutoExpirationVersionTrim` from `$false` to `$true` sets `MajorVersionLimit` to 500 and `ExpireVersionsAfterDays` to 30.

Applies to the default policy or the file type specified by `-FileType`.

```yaml
Type: Boolean
Parameter Sets: Default, FileType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpireVersionsAfterDays
The number of days after which versions expire. Set to `0` to disable time-based expiration.

Specifying `-ExpireVersionsAfterDays` when the policy has `EnableAutoExpirationVersionTrim` set to `$true` throws an error.

Applies to the default policy or the file type specified by `-FileType`.

```yaml
Type: Int32
Parameter Sets: Default, FileType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileType
The file type name whose per-file-type override should be created, updated, or removed. Supported values are `"audio"`, `"video"`, and `"outlookspst"`. Omit this parameter to modify the default policy. For more information, see [File type version limits in SharePoint](/sharepoint/file-type-version-limits).

```yaml
Type: String
Parameter Sets: FileType, FileTypeRemove
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorVersionLimit
The maximum number of major versions to retain.

Specifying `-ExpireVersionsAfterDays` when the policy has `EnableAutoExpirationVersionTrim` set to `$true` throws an error.

Applies to the default policy or the file type specified by `-FileType`.

```yaml
Type: Int32
Parameter Sets: Default, FileType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Remove
Removes the per-file-type override identified by `-FileType`. `-FileType` is required when this switch is specified.

```yaml
Type: SwitchParameter
Parameter Sets: FileTypeRemove
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VersionPolicy
The version policy object to modify, typically piped from `Get-SPOTenantVersionPolicy`. The original object is not modified; a new object with the requested changes is returned.

```yaml
Type: SPOFileVersionPolicySettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### Microsoft.Online.SharePoint.TenantAdministration.SPOFileVersionPolicySettings

## OUTPUTS

### Microsoft.Online.SharePoint.TenantAdministration.SPOFileVersionPolicySettings

## NOTES

Always review the returned policy object before passing it to `New-SPOTenantApplyFileVersionPolicyJob` or `Get-SPOTenantApplyFileVersionPolicyJobImpact` to confirm it reflects the intended configuration.

## RELATED LINKS

[Get-SPOTenantVersionPolicy](Get-SPOTenantVersionPolicy.md)

[New-SPOTenantApplyFileVersionPolicyJob](New-SPOTenantApplyFileVersionPolicyJob.md)

[Get-SPOTenantApplyFileVersionPolicyJobImpact](Get-SPOTenantApplyFileVersionPolicyJobImpact.md)
