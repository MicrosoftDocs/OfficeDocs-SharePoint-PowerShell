---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/add-spositetofilearchivepolicy
applicable: SharePoint Online
title: Add-SPOSiteToFileArchivePolicy
schema: 2.0.0
author: HectorRMota
ms.author: hemota
ms.reviewer:
---

# Add-SPOSiteToFileArchivePolicy

## SYNOPSIS

Adds a site to a file archive policy.

## SYNTAX

```
Add-SPOSiteToFileArchivePolicy -PolicyId <Guid> -Site <SpoSitePipeBind> [-Exclude] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet adds a site to an existing file archive policy, either as an inclusion or as an exclusion.

By default, the site is added as an inclusion. Inclusions are only valid for a policy whose PolicyType is `SelectedSites`, and at least one site must be added before such a policy can be activated. Adding an inclusion to an `AllSites` or `AllODBSites` policy returns an error.

When you use the `-Exclude` parameter, the site is added as an exclusion and is exempted from the policy when it runs. Exclusions are only valid for a policy whose PolicyType is `AllSites` or `AllODBSites`. Adding an exclusion to a `SelectedSites` policy returns an error.

The site must exist and be eligible for archiving. A single policy can contain a maximum of 1,000 sites, counting inclusions and exclusions together.

> [!NOTE]
> This cmdlet is part of the file archive policies feature which is currently in preview.

## EXAMPLES

### Example 1

```powershell
Add-SPOSiteToFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890" -Site "https://contoso.sharepoint.com/sites/marketing"
```

Adds the marketing site to the specified `SelectedSites` file archive policy, so that the policy applies to it.

### Example 2

```powershell
Add-SPOSiteToFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890" -Site "https://contoso-my.sharepoint.com/personal/user_contoso_com" -Exclude
```

Adds a OneDrive for Business site to the specified `AllODBSites` policy as an exclusion, exempting it from archiving while the policy continues to apply to every other OneDrive site in the tenant.

## PARAMETERS

### -Exclude

Adds the site as an exclusion instead of an inclusion, exempting it from the policy when the policy runs.

Use this parameter only with a policy whose PolicyType is `AllSites` or `AllODBSites`. Omit it when adding sites to a `SelectedSites` policy.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyId

Specifies the unique identifier (GUID) of the policy to add the site to.

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

Specifies the URL of the site to add to the policy. The site must exist and be eligible for archiving.

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

[Get-SPOFileArchivePolicy](Get-SPOFileArchivePolicy.md)

[Get-SPOFileArchivePolicyReport](Get-SPOFileArchivePolicyReport.md)

[Get-SPOFileArchivePolicySites](Get-SPOFileArchivePolicySites.md)

[New-SPOFileArchivePolicy](New-SPOFileArchivePolicy.md)

[Remove-SPOFileArchivePolicy](Remove-SPOFileArchivePolicy.md)

[Remove-SPOSiteToFileArchivePolicy](Remove-SPOSiteToFileArchivePolicy.md)

[Set-SPOFileArchivePolicy](Set-SPOFileArchivePolicy.md)
