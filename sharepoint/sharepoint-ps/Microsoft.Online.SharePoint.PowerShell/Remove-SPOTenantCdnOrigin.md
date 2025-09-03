---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spotenantcdnorigin
applicable: SharePoint Online
title: Remove-SPOTenantCdnOrigin
schema: 2.0.0
author: trent-green
ms.author: speedta
ms.reviewer:
---

# Remove-SPOTenantCdnOrigin

## SYNOPSIS

Removes a new origin from the Public or Private content delivery network (CDN). Requires Tenant administrator permissions.

## SYNTAX

```
Remove-SPOTenantCdnOrigin -OriginUrl <String> -CdnType <SPOTenantCdnType> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Removes a new origin from the Public or Private content delivery network (CDN).

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOTenantCdnOrigin -CdnType Public -OriginUrl sites/pubsite/siteassets/subfolder
```

The example removes a CDN from a tenant level.

### EXAMPLE 2

```powershell
Remove-SPOTenantCdnOrigin -CdnType Public -OriginScope Site  -Site https://contoso.sharepoint.com/sites/pubsite -OriginUrl siteassets/subfolder
```

The example removes a CDN from a site level.

### EXAMPLE 3

```powershell
Remove-SPOTenantCdnOrigin -CdnType Private -OriginUrl /sites/branding/Assets
```

This example removes a recently-removed organizational assets library from a CDN.

## PARAMETERS

### -CdnType

> Applicable: SharePoint Online

Specifies the CDN type. The valid values are: Public or Private.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SPOTenantCdnType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OriginUrl

> Applicable: SharePoint Online

Specifies a path to the doc library to be configured. It can be provided in two ways: relative path, or a mask.

Relative-Relative path depends on the OriginScope. If the originScope is Tenant, a path must be a relative path under the tenant root. If the originScope is Site, a path must be a relative path under the given Site. The path must point to the valid Document Library or a folder with a document library.

Any asset stored under the path provided (in the container itself or any of its subfolders) will be exposed via CDN

Mask - Mask allows to configure a partial URL match. It must start with */, and must not include * anywhere else. I.e. an origin "*/masterpages" will expose all the assets under all the masterpages libraries, either under the tenant root (means, anywhere in the tenancy) or in the given site collection, depends on the OriginScope parameter. Equally, */masterpages/subfolder will enable items in "subfolder" and below.

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

### -WhatIf

> Applicable: SharePoint Online

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

## RELATED LINKS
