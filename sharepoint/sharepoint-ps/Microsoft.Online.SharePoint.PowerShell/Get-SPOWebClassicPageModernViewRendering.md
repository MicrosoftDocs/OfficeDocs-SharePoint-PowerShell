---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spowebclassicpagemodernviewrendering
schema: 2.0.0
applicable: SharePoint Online
title: Get-SPOWebClassicPageModernViewRendering
author: yifengmao
ms.author: yifengmao
manager:
ms.reviewer:
---

# Get-SPOWebClassicPageModernViewRendering

## SYNOPSIS
This cmdlet gets the stored modern view rendering setting for classic pages on a web.

## SYNTAX

```
Get-SPOWebClassicPageModernViewRendering -WebUrl <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet returns the modern view rendering setting that's stored on a single web. The web can be the root web of a site collection or any subsite.

The setting applies only to the web that you specify. Parent webs, sibling webs, and subsites aren't affected, and they aren't included in the result.

This cmdlet reports the stored configuration only. A result of `Enabled` doesn't guarantee that every page renders with the modern view, because page type, page eligibility, request-level opt-out, and service safeguards also affect rendering.

Use `Set-SPOWebClassicPageModernViewRendering -Operation Enable` or `-Operation Disable` to store an explicit override. Use `-Operation UseTenantDefault` to remove the override; the next read then reports `NotSet`, not `Disabled`.

## EXAMPLES

### Example 1
```powershell
Get-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing"
```

This example gets the stored setting for the root web of the Marketing site.

### Example 2
```powershell
Get-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing/europe"
```

This example gets the stored setting for the Europe subsite. The result describes only that subsite.

## PARAMETERS

### -WebUrl

> Applicable: SharePoint Online

Specifies the absolute URL of the web to inspect. The URL must point to an existing web. A URL that points to a page, a document library, or a web that doesn't exist returns an error.

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
This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### System.Object

## RELATED LINKS
[Set-SPOWebClassicPageModernViewRendering](Set-SPOWebClassicPageModernViewRendering.md)
