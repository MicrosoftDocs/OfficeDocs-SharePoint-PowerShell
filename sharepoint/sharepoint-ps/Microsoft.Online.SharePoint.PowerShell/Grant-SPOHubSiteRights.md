---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/grant-spohubsiterights
applicable: SharePoint Online
title: Grant-SPOHubSiteRights
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Grant-SPOHubSiteRights

## SYNOPSIS

Grants rights to users or mail-enabled security groups to associate their site with a hub site.

## SYNTAX

```
Grant-SPOHubSiteRights [-Identity] <SpoHubSitePipeBind> -Principals <String[]>
 -Rights <SPOHubSiteUserRightsClient> [<CommonParameters>]
```

## DESCRIPTION

Applies permissions to a set of users or mail-enabled security groups. Use this cmdlet to scope visibility of who can associate their site with the hub site when using the SharePoint user interface. Hub sites are public by default. Once you set permissions, only those groups or users you specified can associate their site with the hub site.

To view which users or groups have permissions to a site, use the [Get-SPOHubSite](Get-SPOHubSite.md) cmdlet.

## EXAMPLES

### Example 1

```powershell
Grant-SPOHubSiteRights https://contoso.sharepoint.com/sites/Marketing
-Principals nestorw@contoso.onmicrosoft.com
-Rights Join
```

This example shows how to grant rights to Nestor (a user at the fictional Contoso site) to associate his sites with the marketing hub site.

## PARAMETERS

### -Identity

URL of the hub site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoHubSitePipeBind
Parameter Sets: (All)
Aliases: HubSite
Applicable: SharePoint Online

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Principals

One or more principals to add permissions for.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rights

Always set to the value **Join**. Any user or group with **Join** permissions can view and join the hub site.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Join
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
