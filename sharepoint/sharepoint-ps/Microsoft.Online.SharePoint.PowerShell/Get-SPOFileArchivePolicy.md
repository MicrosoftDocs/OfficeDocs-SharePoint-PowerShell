---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spofilearchivepolicy
applicable: SharePoint Online
title: Get-SPOFileArchivePolicy
schema: 2.0.0
author: HectorRMota
ms.author: hemota
ms.reviewer:
---

# Get-SPOFileArchivePolicy

## SYNOPSIS

Gets one or all file archive policies for the tenant.

## SYNTAX

```
Get-SPOFileArchivePolicy [-PolicyId <Guid>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet retrieves the properties of file archive policies for the connected SharePoint Online tenant. If the `-PolicyId` parameter is specified, returns only the matching policy. If omitted, returns all file archive policies under the tenant.

> [!NOTE]
> This cmdlet is part of the file archive policies feature which is currently in preview.

## EXAMPLES

### Example 1

```powershell
Get-SPOFileArchivePolicy
```

Returns all file archive policies configured for the tenant.

### Example 2

```powershell
Get-SPOFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890"
```

Returns the file archive policy with the specified ID.

## PARAMETERS

### -PolicyId

Specifies the unique identifier (GUID) of the policy to retrieve. If not specified, all policies under the tenant are returned.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

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

[Get-SPOFileArchivePolicyReport](Get-SPOFileArchivePolicyReport.md)

[Get-SPOFileArchivePolicySites](Get-SPOFileArchivePolicySites.md)

[New-SPOFileArchivePolicy](New-SPOFileArchivePolicy.md)

[Remove-SPOFileArchivePolicy](Remove-SPOFileArchivePolicy.md)

[Remove-SPOSiteToFileArchivePolicy](Remove-SPOSiteToFileArchivePolicy.md)

[Set-SPOFileArchivePolicy](Set-SPOFileArchivePolicy.md)
