---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/remove-spositecollectionappcatalog
applicable: SharePoint Online
title: Remove-SPOSiteCollectionAppCatalog
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Remove-SPOSiteCollectionAppCatalog

## SYNOPSIS

Removes the site collection app catalog.

## SYNTAX

```
Remove-SPOSiteCollectionAppCatalog [-Site] <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove the site collection app catalog.

## EXAMPLES

### Example 1

```powershell
Remove-SPOSiteCollectionAppCatalog -Site https://contoso.sharepoint.com/sites/Research
```

This example removes the site collection app catalog from the site <https://contoso.sharepoint.com/sites/Research.>

## PARAMETERS

### -Site

> Applicable: SharePoint Online

Url of the site collection.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
