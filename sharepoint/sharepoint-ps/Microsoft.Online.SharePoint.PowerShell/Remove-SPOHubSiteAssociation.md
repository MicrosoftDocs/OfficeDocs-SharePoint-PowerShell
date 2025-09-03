---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spohubsiteassociation
applicable: SharePoint Online
title: Remove-SPOHubSiteAssociation
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
ms.date: 07/16/2025
---

# Remove-SPOHubSiteAssociation

## SYNOPSIS

Removes a site from its associated hub site.

## SYNTAX

```
Remove-SPOHubSiteAssociation [-Site] <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove an association between a site and a hub site.

> [!IMPORTANT]
> This cmdlet is currently in preview and is subject to change. It is not currently supported for use in production environments.

If the site or hub site doesn't exist, this cmdlet returns a "File not found" error.

## EXAMPLES

### Example 1

```powershell
Remove-SPOHubSiteAssociation https://contoso.sharepoint.com/sites/Research
```

This example removes the research site from the marketing hub site.

## PARAMETERS

### -Site

> Applicable: SharePoint Online

URL of the site to remove from the hub site.

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

## RELATED LINKS
