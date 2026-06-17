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
Add-SPOSiteToFileArchivePolicy -PolicyId <Guid> -Site <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet adds a site to an existing file archive policy that has a PolicyType of `SelectedSites`. The site must exist and be eligible for archiving. At least one site must be added before a `SelectedSites` policy can be activated.

> [!NOTE]
> This cmdlet is part of the file archive policies feature which is currently in preview.

## EXAMPLES

### Example 1

```powershell
Add-SPOSiteToFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890" -Site "https://contoso.sharepoint.com/sites/marketing"
```

Adds the marketing site to the specified file archive policy.

## PARAMETERS

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
