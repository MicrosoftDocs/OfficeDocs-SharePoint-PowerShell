---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/remove-spositetofilearchivepolicy
applicable: SharePoint Online
title: Remove-SPOSiteToFileArchivePolicy
schema: 2.0.0
author: HectorRMota
ms.author: hemota
ms.reviewer:
---

# Remove-SPOSiteToFileArchivePolicy

## SYNOPSIS

Removes a site from a file archive policy.

## SYNTAX

```
Remove-SPOSiteToFileArchivePolicy -PolicyId <Guid> -Site <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet removes a site from an existing file archive policy. It removes either an included site from a `SelectedSites` policy or an excluded site from an `AllSites` or `AllODBSites` policy.

Removing an included site means the policy no longer applies to that site. Removing an excluded site means the site is no longer exempt, so the policy applies to it again on future runs.

You can't remove the last remaining site from an active `SelectedSites` policy, because that would leave the policy active with no sites in scope. Set the policy to `Inactive` first, or add another site before removing this one.

> [!NOTE]
> This cmdlet is part of the file archive policies feature which is currently in preview.

## EXAMPLES

### Example 1

```powershell
Remove-SPOSiteToFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890" -Site "https://contoso.sharepoint.com/sites/marketing"
```

Removes the marketing site from the specified file archive policy.

## PARAMETERS

### -PolicyId

Specifies the unique identifier (GUID) of the policy to remove the site from.

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

### -Site

Specifies the URL of the site to remove from the policy.

```yaml
Type: SpoSitePipeBind
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

[Get-SPOFileArchivePolicyReport](Get-SPOFileArchivePolicyReport.md)

[Get-SPOFileArchivePolicySites](Get-SPOFileArchivePolicySites.md)

[New-SPOFileArchivePolicy](New-SPOFileArchivePolicy.md)

[Remove-SPOFileArchivePolicy](Remove-SPOFileArchivePolicy.md)

[Set-SPOFileArchivePolicy](Set-SPOFileArchivePolicy.md)
