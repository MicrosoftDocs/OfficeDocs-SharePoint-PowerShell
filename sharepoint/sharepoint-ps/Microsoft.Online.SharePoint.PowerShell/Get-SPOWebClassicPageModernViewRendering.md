---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
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
Gets the stored modern view rendering setting for classic pages on a web.

## SYNTAX

```
Get-SPOWebClassicPageModernViewRendering -WebUrl <String> [<CommonParameters>]
```

## DESCRIPTION
The `Get-SPOWebClassicPageModernViewRendering` cmdlet returns the modern view rendering setting that's stored on a single web. The web can be the root web of a site collection or any subsite.

The setting applies only to the web that you specify. Parent webs, sibling webs, and subsites aren't affected, and they aren't included in the result.

The cmdlet returns an object with the following properties:

- **WebUrl**: The web that was inspected.
- **StoredOverride**: One of the following values.

  | Value | Description |
  |-------|-------------|
  | `Enabled` | Classic pages on this web render with the modern view. |
  | `Disabled` | Classic pages on this web render with the classic view. |
  | `NotSet` | No setting is stored on this web, so the tenant-level rollout decides how classic pages render. `NotSet` isn't the same as `Disabled`. |
  | `Invalid` | A stored value can't be interpreted. The tenant-level rollout decides how classic pages render until you set a valid value or clear the setting. |

This cmdlet reports the stored configuration only. A result of `Enabled` doesn't guarantee that every page renders with the modern view, because page type and page eligibility also affect rendering.

You must be a SharePoint Administrator to run this cmdlet.

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing"
```

This example gets the stored setting for the root web of the Marketing site.

### Example 2
```powershell
PS C:\> Get-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing/europe"
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

To see the examples, type: "get-help Get-SPOWebClassicPageModernViewRendering -examples".

For more information, type: "get-help Get-SPOWebClassicPageModernViewRendering -detailed".

For technical information, type: "get-help Get-SPOWebClassicPageModernViewRendering -full".

For online help, type: "get-help Get-SPOWebClassicPageModernViewRendering -online"

## RELATED LINKS
[Set-SPOWebClassicPageModernViewRendering](Set-SPOWebClassicPageModernViewRendering.md)
