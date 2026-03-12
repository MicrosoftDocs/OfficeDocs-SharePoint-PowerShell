---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spocustomcdntenantapps
applicable: SharePoint Online
title: Get-SPOCustomCdnTenantApps
schema: 2.0.0
author: yadongzhai
ms.author: yadongzhai
ms.reviewer:
---

# Get-SPOCustomCdnTenantApps

## SYNOPSIS

Retrieves all apps that use a custom CDN from the Tenant App Catalog. You must be a SharePoint Online administrator to run this cmdlet.

## SYNTAX

```
Get-SPOCustomCdnTenantApps [<CommonParameters>]
```

## DESCRIPTION

Retrieves all apps from the Tenant App Catalog that are configured to use a custom content delivery network (CDN). The output includes the product ID and title of each app.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOCustomCdnTenantApps
```

This example returns a list of all apps in the Tenant App Catalog that use a custom CDN.

## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOCustomCdnSiteCollectionApps](Get-SPOCustomCdnSiteCollectionApps.md)
