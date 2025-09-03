---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spohubsite
applicable: SharePoint Online
title: Get-SPOHubSite
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
ms.date: 07/16/2025
---

# Get-SPOHubSite

## SYNOPSIS

Lists hub sites or hub site information.

## SYNTAX

```
Get-SPOHubSite [[-Identity] <SpoHubSitePipeBind>] [<CommonParameters>]
```

## DESCRIPTION

Lists all hub sites found on the SharePoint tenant. If you provide **-Identity** the cmdlet returns detailed information about the specific hub. You can find which hub a site is associated with by providing the site's identity with this cmdlet.

If the hub site doesn't exist, this cmdlet returns a "File not found" error.

> [!NOTE]
> If a deleted hub site appears in the output of this cmdlet you may not have run [Unregister-SPOHubSite](/powershell/module/sharepoint-online/unregister-spohubsite) on the deleted hub site.

## EXAMPLES

### Example 1

```powershell
Get-SPOHubSite
```

This example lists all hub sites in the tenant.

### Example 2

```powershell
Get-SPOHubSite -Identity https://contoso.sharepoint.com/sites/online-marketing

ID                   : 44252d09-62c4-4913-9eb0-a2a8b8d7f863
Title                : Marketing Hub
SiteId               : 44252d09-62c4-4913-9eb0-a2a8b8d7f863
SiteUrl              : https://contoso.sharepoint.com/sites/Marketing
LogoUrl              : https://contoso.sharepoint.com/sites/Marketing/SiteAssets/hublogo.png
Description          : Hub for the Marketing division
Permissions          : {Wilke, Nestor}
SiteDesignId         : 00000000-0000-0000-0000-000000000000
RequiresJoinApproval : False
HideNameInNavigation : False
```

This example begins with the online-marketing site. The cmdlet finds the associated hub site, which is marketing. Then it lists all the details about the marketing hub site.

## PARAMETERS

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

URL of the hub site. If not specified, the cmdlet lists all hub sites in the tenant.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoHubSitePipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoHubSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
