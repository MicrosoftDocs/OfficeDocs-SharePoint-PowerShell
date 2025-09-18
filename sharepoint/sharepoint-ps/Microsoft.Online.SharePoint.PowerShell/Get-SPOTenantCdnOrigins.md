---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/get-spotenantcdnorigins
applicable: SharePoint Online
title: Get-SPOTenantCdnOrigins
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Get-SPOTenantCdnOrigins

## SYNOPSIS

Lists all the configured origins under the tenancy or under a given site. You must be a SharePoint Online administrator to run this cmdlet.

## SYNTAX

```
Get-SPOTenantCdnOrigins -CdnType <SPOTenantCdnType> [<CommonParameters>]
```

## DESCRIPTION

Lists all the configured origins under the tenancy or under a given site.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantCdnOrigins -CdnType Public
```

The example returns a list of origins from the Tenant.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
