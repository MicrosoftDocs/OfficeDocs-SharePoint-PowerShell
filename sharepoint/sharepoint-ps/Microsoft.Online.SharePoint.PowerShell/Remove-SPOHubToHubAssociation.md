---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spohubtohubassociation
applicable: SharePoint Online
title: Remove-SPOHubToHubAssociation
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Remove-SPOHubToHubAssociation

## SYNOPSIS

Removes the selected hub site from its parent hub.

## SYNTAX

```
Remove-SPOHubToHubAssociation [-HubSiteId] <Guid> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove the selected hub site from its parent hub.

## EXAMPLES

### Example 1

```powershell
Remove-SPOHubToHubAssociation -HubSiteId 6638bd4c-d88d-447c-9eb2-c84f28ba8b15
```

This example removes the site with the given id from its parent Hub.

## PARAMETERS

### -HubsiteId

> Applicable: SharePoint Online

Id of the Hub site to be removed from its parent Hub.

```yaml
Type: System.Guid
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

### System.Guid

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
