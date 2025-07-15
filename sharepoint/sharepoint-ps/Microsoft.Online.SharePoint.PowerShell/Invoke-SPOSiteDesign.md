---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/invoke-spositedesign
applicable: SharePoint Online
title: Invoke-SPOSiteDesign
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Invoke-SPOSiteDesign

## SYNOPSIS

Applies a published site design to a specified site collection target. This allows a site design to be applied to an existing site collection. The supported site templates you can apply a site design to include: "modern" team site (with O365 group), "modern" team site (without an O365 group); communication site; classic team site; and classic publishing site.

## SYNTAX

```
Invoke-SPOSiteDesign -Identity <SPOSiteDesignPipeBind> -WebUrl <String> [<CommonParameters>]
```

## DESCRIPTION

Applies a published site design to a specified site collection target. This allows a site design to be applied to an existing site collection.

## EXAMPLES

### Example 1

This example applies a site design whose script creates two lists, formats several of the columns, adds the lists to the site navigation, and then joins the site to an existing hub site.

```powershell
Invoke-SPOSiteDesign -Identity 501z8c32-4147-44d4-8607-26c2f67cae82 -WebUrl "https://contoso.sharepoint.com/sites/projectgo"

Title                                             Outcome
----------------------------------------------    -------
Create or update list Project Activities          Success
Update list description                           Success
Create column Project Status                      Success
Create column Effort (days)                       Success
Set custom formatter for field Project Status     Success
Set custom formatter for field Effort (days)      Success
Create or update list Project Collateral          Success
Create column Due Date                            Success
Set custom formatter for field Due Date           Success
Add Project Activities to left nav                Success
Add Project Collateral to left nav                Success
Add to Hub Site                                   Success
```

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

The ID of the site design to apply.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebUrl

> Applicable: SharePoint Online
The URL of the site collection where the site design will be applied.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
