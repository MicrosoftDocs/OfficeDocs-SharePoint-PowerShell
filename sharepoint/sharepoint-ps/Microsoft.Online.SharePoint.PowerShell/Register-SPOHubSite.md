---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/register-spohubsite
applicable: SharePoint Online
title: Register-SPOHubSite
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Register-SPOHubSite

## SYNOPSIS

Enables the hub site feature on a site to make it a hub site. For more information visit [SharePoint hub sites overview](/sharepoint/dev/features/hub-site/hub-site-overview).

## SYNTAX

```
Register-SPOHubSite [-Site] <SpoSitePipeBind> -Principals <String[]> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to register an existing site collection as a hub site.

> [!IMPORTANT]
> A maximum of 2000 hub sites may be created per tenant, with 'unlimited' number of site collections associated to a hub site.
> [!NOTE]
> It can take up to 2-4 hours for the changes to appear.

## EXAMPLES

### Example 1

```powershell
Register-SPOHubSite https://contoso.sharepoint.com/sites/Marketing  -Principals $null
```

This example registers the marketing site on Contoso as hub site without setting any principals for it.

## PARAMETERS

### -Principals

> Applicable: SharePoint Online

Specifies one or more principals (user or group) to be granted rights to the specified HubSite. Can be used to filter who can associate sites to this hub site.

```yaml
Type: System.String[]
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

Specifies the URL of the site collection to which to enable the hub site features.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

If the site doesn't exist, this cmdlet returns a "File not found" error.

If the site is already a hub site, this cmdlet returns a "This site is already a HubSite" error.

If the site is already associated with another hub site, this cmdlet returns a "This site is currently associated with a HubSite" error. You'll need to run the [Remove-SPOHubSiteAssociation](Remove-SPOHubSiteAssociation.md) cmdlet first before you can make the site a hub site.

## RELATED LINKS
