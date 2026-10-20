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

### Enabled
```
Set-SPOWebClassicPageModernViewRendering -WebUrl <String> -Enabled <Boolean> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Clear
```
Set-SPOWebClassicPageModernViewRendering -WebUrl <String> [-Clear] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPOWebClassicPageModernViewRendering` cmdlet controls whether classic pages on a single web render with the modern view. The web can be the root web of a site collection or any subsite.

The setting applies only to the web that you specify. Parent webs, sibling webs, and subsites keep their own settings. To change more than one web, run the cmdlet once for each web.

Use one of the following options:

- **-Enabled $true**: Classic pages on this web render with the modern view, even if the tenant-level rollout hasn't reached the web.
- **-Enabled $false**: Classic pages on this web render with the classic view, even if the tenant-level rollout has reached the web. This is an explicit opt out, not the same as clearing the setting.
- **-Clear**: Removes the stored setting, so the tenant-level rollout decides how classic pages render.

The setting takes precedence over the tenant-level rollout. Clearing it restores the tenant-level behavior.

You must be a SharePoint Administrator to run this cmdlet.

## EXAMPLES

### Example 1
```powershell
PS C:\> Set-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing" -Enabled $true
```

This example turns on modern view rendering for classic pages on the root web of the Marketing site.

### Example 2
```powershell
PS C:\> Set-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing/europe" -Enabled $false
```

This example turns off modern view rendering for classic pages on the Europe subsite. Other webs in the site collection aren't affected.

### Example 3
```powershell
PS C:\> Set-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing/europe" -Clear
```

This example removes the stored setting from the Europe subsite, so the tenant-level rollout decides how classic pages render.

### Example 4
```powershell
PS C:\> Set-SPOWebClassicPageModernViewRendering -WebUrl "https://contoso.sharepoint.com/sites/marketing" -Clear -WhatIf
```

This example shows what would happen if you cleared the setting on the root web of the Marketing site. The setting isn't changed.

## PARAMETERS

### -Clear

> Applicable: SharePoint Online

Removes the stored setting from the web, so the tenant-level rollout decides how classic pages render. You can't use this parameter together with the **Enabled** parameter, and you can't specify it as `$false`.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Clear
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Enabled

> Applicable: SharePoint Online

Specifies how classic pages render on the web. Use `$true` to render them with the modern view, or `$false` to render them with the classic view. A value of `$false` is an explicit opt out. To remove the setting instead, use the **Clear** parameter.

```yaml
Type: System.Boolean
Parameter Sets: Enabled
Aliases:

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
