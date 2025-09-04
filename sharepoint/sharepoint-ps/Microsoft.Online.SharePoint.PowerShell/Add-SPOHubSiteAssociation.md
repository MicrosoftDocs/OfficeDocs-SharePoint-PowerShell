---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spohubsiteassociation
applicable: SharePoint Online
title: Add-SPOHubSiteAssociation
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Add-SPOHubSiteAssociation

## SYNOPSIS

Associates a site with a hub site.

## SYNTAX

```
Add-SPOHubSiteAssociation [-Site] <SpoSitePipeBind> -HubSite <SpoHubSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to associate a site with a hub site.

## EXAMPLES

### Example 1

```powershell
Add-SPOHubSiteAssociation https://contoso.sharepoint.com/sites/Research -HubSite https://contoso.sharepoint.com/sites/Marketing
```

This example associates the research site with the marketing hub site.

## PARAMETERS

### -HubSite

> Applicable: SharePoint Online

URL or Site ID of the hub site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoHubSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site

> Applicable: SharePoint Online

URL of the site to join to the hub site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

If the site or hub site doesn't exist, this cmdlet returns a "File not found" error.

If the site is already a hub site, this cmdlet returns a "This site is already a HubSite" error.

In multi-geo situations, when assigning a hub that is across geo locations, you must pass the site ID of the hub site to the HubSite parameter as a URL will fail.

## RELATED LINKS
