---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
applicable: SharePoint Online
title: Set-SPOWebClassicPageModernViewRendering
author: yifengmao
ms.author: yifengmao
manager:
ms.reviewer:
---

# Set-SPOWebClassicPageModernViewRendering

## SYNOPSIS
Sets or clears the modern view rendering setting for classic pages on a web.

## SYNTAX

```
Set-SPOWebClassicPageModernViewRendering -WebUrl <String> -Operation <WebClassicPageModernViewRenderingOperation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPOWebClassicPageModernViewRendering` cmdlet controls whether classic pages on a single web render with the modern view. The web can be the root web of a site collection or any subsite.

The setting applies only to the web that you specify. Parent webs, sibling webs, and subsites keep their own settings. To change more than one web, run the cmdlet once for each web.

Specify one of the following operations:

- **-Operation Enable**: Stores an explicit opt-in to modern view rendering, even if the tenant-level rollout hasn't reached the web.
- **-Operation Disable**: Stores an explicit opt-out of modern view rendering, even if the tenant-level rollout has reached the web.
- **-Operation UseTenantDefault**: Removes the stored setting, so the tenant-level rollout decides how classic pages render. This operation can result in either modern or classic rendering; it isn't the same as `Disable`.

The setting takes precedence over the tenant-level rollout. `Enable` doesn't bypass page eligibility, request-level opt-out, or service safeguards, and doesn't guarantee that every page renders with the modern view.

The operation is required and has no default. To read the stored setting without changing it, use `Get-SPOWebClassicPageModernViewRendering`.

You must be a SharePoint Administrator to run this cmdlet.

## EXAMPLES

### Example 1
```powershell
PS C:\> Set-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing" -Operation Enable
```

This example opts the root web of the Marketing site into modern view rendering for eligible classic pages.

### Example 2
```powershell
PS C:\> Set-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing/europe" -Operation Disable
```

This example turns off modern view rendering for classic pages on the Europe subsite. Other webs in the site collection aren't affected.

### Example 3
```powershell
PS C:\> Set-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing/europe" -Operation UseTenantDefault
```

This example removes the stored setting from the Europe subsite, so the tenant-level rollout decides how classic pages render. `Get-SPOWebClassicPageModernViewRendering` then reports `StoredOverride` as `NotSet`.

### Example 4
```powershell
PS C:\> Set-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing" -Operation UseTenantDefault -WhatIf
```

This example previews removing the web override and using tenant defaults on the root web of the Marketing site. The setting isn't changed.

## PARAMETERS

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Operation

> Applicable: SharePoint Online

Specifies the change to make to this web. `Enable` stores an explicit opt-in, `Disable` stores an explicit opt-out, and `UseTenantDefault` removes the override so the tenant-level rollout applies again. Using tenant defaults doesn't necessarily disable modern view rendering.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOWebClassicPageModernViewRendering+WebClassicPageModernViewRenderingOperation
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable, UseTenantDefault

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebUrl

> Applicable: SharePoint Online

Specifies the absolute URL of the web to update. The URL must point to an existing web. A URL that points to a page, a document library, or a web that doesn't exist returns an error.

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

### -WhatIf

> Applicable: SharePoint Online

Shows what would happen if the cmdlet runs. The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
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

To see the examples, type: "get-help Set-SPOWebClassicPageModernViewRendering -examples".

For more information, type: "get-help Set-SPOWebClassicPageModernViewRendering -detailed".

For technical information, type: "get-help Set-SPOWebClassicPageModernViewRendering -full".

For online help, type: "get-help Set-SPOWebClassicPageModernViewRendering -online"

## RELATED LINKS
[Get-SPOWebClassicPageModernViewRendering](Get-SPOWebClassicPageModernViewRendering.md)
