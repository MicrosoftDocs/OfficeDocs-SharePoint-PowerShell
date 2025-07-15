---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/revoke-spohubsiterights
applicable: SharePoint Online
title: Revoke-SPOHubSiteRights
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Revoke-SPOHubSiteRights

## SYNOPSIS

Revokes rights for specified principals to a hub.

## SYNTAX

```
Revoke-SPOHubSiteRights [-Identity] <SpoHubSitePipeBind> -Principals <String[]> [<CommonParameters>]
```

## DESCRIPTION

Revokes rights for specified principals to the given hub site. The specified principals will no longer be able to associate sites with the hub. To find which principals have access to a hub site, use the [Get-SPOHubSite](Get-SPOHubSite.md) cmdlet.

> [!NOTE]
> If the hub site doesn't exist, this cmdlet returns a "File not found" error.

## EXAMPLES

### Example 1

```powershell
Revoke-SPOHubSiteRights https://contoso.sharepoint.com/sites/Marketing `
-Principals "nestorw@contoso.onmicrosoft.com"
```

This example shows how to revoke rights so that Nestor can no longer join sites to the Marketing hub site.

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

One or more principals to revoke the permissions for.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoHubSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
