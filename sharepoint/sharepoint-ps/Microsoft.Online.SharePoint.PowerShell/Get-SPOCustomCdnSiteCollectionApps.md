---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spocustomcdnsitecollectionapps
applicable: SharePoint Online
title: Get-SPOCustomCdnSiteCollectionApps
schema: 2.0.0
author: Yadong1106
ms.author: yadongzhai
---

# Get-SPOCustomCdnSiteCollectionApps

## SYNOPSIS

Retrieves all app installations that use a custom content delivery network (CDN) for a specific site collection.

## SYNTAX

```
Get-SPOCustomCdnSiteCollectionApps -SiteUrl <String> [<CommonParameters>]
```

## DESCRIPTION

Retrieves all app installations that are configured to use a custom CDN for the specified site collection. The output includes the product ID, title, app installation ID, site ID, and site URL of each app installation.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOCustomCdnSiteCollectionApps -SiteUrl "https://contoso.sharepoint.com/sites/marketing"
```

This example returns a list of all app installations that use a custom CDN for the specified site collection.

## PARAMETERS

### -SiteUrl

> Applicable: SharePoint Online

Specifies the URL of the site collection for which to retrieve custom CDN app installations.

```yaml
Type: System.String
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

[Get-SPOCustomCdnTenantApps](Get-SPOCustomCdnTenantApps.md)
