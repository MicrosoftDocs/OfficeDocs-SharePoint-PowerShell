---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spositearchivestate
applicable: SharePoint Online
title: Set-SPOSiteArchiveState
schema: 2.0.0
author: AdiGanMSFT
ms.author: adigan
ms.reviewer:
---

# Set-SPOSiteArchiveState

## SYNOPSIS

Sets the archived state of the site. Can be used to archive and reactivate sites.

## SYNTAX

```powershell
Set-SPOSiteArchiveState [-Identity] <SpoHubSitePipeBind> -ArchiveState <String> [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to change the archive status of the site. You must be at least a SharePoint Online administrator and be a site collection administrator to run the cmdlet.
Microsoft 365 Archive needs to be enabled for the organization to be able to use the feature.

## EXAMPLES

### Example 1

```powershell
Set-SPOSiteArchiveState https://contoso.sharepoint.com/sites/Marketing -ArchiveState Archived
```

This example marks the site as Archived. For seven days after the operation, the site will remain in a "RecentlyArchived" state, where any reactivations will be free and instantaneous. If a site is reactivated after seven days, any reactivations will be charged and will take time.

### Example 2

```powershell
Set-SPOSiteArchiveState https://contoso.sharepoint.com/sites/Marketing -ArchiveState Active
```

This example triggers the reactivation of a site. If the site is reactivated from the "RecentlyArchived" state, it will become available instantaneously. If the site is reactivated from the "FullyArchived" state, it may take time for it to be reactivated.

## PARAMETERS

### -ArchiveState

Sets the archived state of the site. Valid values are Archived, Active.

```yaml
Type: String
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).
