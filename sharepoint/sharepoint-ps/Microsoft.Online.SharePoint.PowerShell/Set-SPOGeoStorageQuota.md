---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/set-spogeostoragequota
applicable: SharePoint Online
title: Set-SPOGeoStorageQuota
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Set-SPOGeoStorageQuota

## SYNOPSIS

This cmdlet sets the storage quota on a multi-geo tenant.

## SYNTAX

```
Set-SPOGeoStorageQuota -GeoLocation <String> -StorageQuotaMB <Int64> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet sets the storage quota, in megabytes, on a particular geo-location. Additionally, it requires a connection to a multi-geo tenant to run correctly. You must be at least a SharePoint Online Administrator to run the cmdlet.

## EXAMPLES

### EXAMPLE 1

```powershell
Set-SPOGeoStorageQuota -GeoLocation EASTUS -StorageQuotaMB 512
```

Sets the SharePoint Online Storage Quota on the EAST US location to 512 MB.

### EXAMPLE 2

```powershell
Set-SPOGeoStorageQuota -GeoLocation NORTHCENTRALUS -StorageQuotaMB 1024
```

Sets the SharePoint Online Storage Quota on the **NORTH CENTRAL US** location to 1024 MB (1GB).

## PARAMETERS

### -GeoLocation

> Applicable: SharePoint Online

The desired Geo Location to set.

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

### -StorageQuotaMB

> Applicable: SharePoint Online

SharePoint Online Storage Quota in MegaBytes.

```yaml
Type: System.Int64
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

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Get-SPOGeoStorageQuota](Get-SPOGeoStorageQuota.md)
