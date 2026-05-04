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
manager: seanmc
---

# Get-SPOVersionPolicyWithChanges

## SYNOPSIS

Returns a locally modified copy of a version policy without sending any changes to the server. SharePoint Advanced Management license or Copilot license is required to run this cmdlet.

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

## SYNTAX

```
Get-SPOVersionPolicyWithChanges -VersionPolicy <SPOFileVersionPolicySettings> [-FileType <String>]
 [-MajorVersionLimit <Int32>] [-ExpireVersionsAfterDays <Int32>]
 [-EnableAutoExpirationVersionTrim <Boolean>] [-Remove] [<CommonParameters>]
```

## DESCRIPTION

Returns a modified copy of the given version policy. All changes are local — nothing is sent to the server. This cmdlet is intended to be used in a pipeline with `Get-SPOTenantVersionPolicy` to build a modified policy that can then be passed to `New-SPOTenantApplyFileVersionPolicyJob` or `Get-SPOTenantApplyFileVersionPolicyJobImpact`.

When `-FileType` is omitted or set to `"default"`, the default policy settings are modified. When `-FileType` specifies a file type name (for example, `"docx"`), the per-file-type override for that type is created or updated.

Use `-Remove` with `-FileType` to delete a per-file-type override. The default policy cannot be removed.

## EXAMPLES

### Example 1
```powershell
$policy = Get-SPOTenantVersionPolicy | Get-SPOVersionPolicyWithChanges -MajorVersionLimit 100
```

Retrieves the current tenant version policy and returns a copy with the default major version limit changed to 100.

### Example 2
```powershell
$policy = Get-SPOTenantVersionPolicy | Get-SPOVersionPolicyWithChanges -FileType "docx" -MajorVersionLimit 50 -ExpireVersionsAfterDays 180
```

Retrieves the current tenant version policy and returns a copy with a per-file-type override for `docx` files that limits to 50 major versions and expires versions after 180 days.

### Example 3
```powershell
$policy = Get-SPOTenantVersionPolicy | Get-SPOVersionPolicyWithChanges -FileType "docx" -Remove
```

Retrieves the current tenant version policy and returns a copy with the `docx` file type override removed, so `docx` files will fall back to the default policy.

### Example 4
```powershell
$policy = Get-SPOTenantVersionPolicy |
    Get-SPOVersionPolicyWithChanges -MajorVersionLimit 100 |
    Get-SPOVersionPolicyWithChanges -FileType "docx" -MajorVersionLimit 50
Get-SPOTenantApplyFileVersionPolicyJobImpact -VersionPolicy $policy
```

Builds a modified policy with a 100-version default and a 50-version docx override, then estimates how many versions would be trimmed using the collected dataset.

## PARAMETERS

### -EnableAutoExpirationVersionTrim
When `$true`, uses automatic expiration, where Microsoft manages the expiration schedule. When `$false`, uses the manual expiration schedule defined by `-MajorVersionLimit` and `-ExpireVersionsAfterDays`.

Applies to the default policy or the file type specified by `-FileType`.

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

### -ExpireVersionsAfterDays
The number of days after which versions expire. Set to `0` to disable time-based expiration.

Applies to the default policy or the file type specified by `-FileType`.

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

### -FileType
The file type name whose per-file-type override should be created, updated, or removed (for example, `"docx"`, `"xlsx"`). Omit this parameter or pass `"default"` to modify the default policy.

Required when using `-Remove`.

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

### -MajorVersionLimit
The maximum number of major versions to retain.

Applies to the default policy or the file type specified by `-FileType`.

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

### -Remove
Removes the per-file-type override identified by `-FileType`. The default policy cannot be removed. `-FileType` is required when this switch is specified.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
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

## RELATED LINKS

[Get-SPOTenantVersionPolicy](Get-SPOTenantVersionPolicy.md)

[New-SPOTenantApplyFileVersionPolicyJob](New-SPOTenantApplyFileVersionPolicyJob.md)

[Get-SPOTenantApplyFileVersionPolicyJobImpact](Get-SPOTenantApplyFileVersionPolicyJobImpact.md)

[SharePoint Advanced Management](/sharepoint/sharepoint-advanced-management-licensing)

[Microsoft 365 Copilot](/microsoft-365/copilot/microsoft-365-copilot-licensing)
