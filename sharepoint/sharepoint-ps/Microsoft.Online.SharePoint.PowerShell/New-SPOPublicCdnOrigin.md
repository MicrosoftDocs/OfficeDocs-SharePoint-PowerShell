---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/new-spopubliccdnorigin
applicable: SharePoint Online
title: New-SPOPublicCdnOrigin
schema: 2.0.0
author: trent-green
ms.author: speedta
ms.reviewer:
---

# New-SPOPublicCdnOrigin

## SYNOPSIS

Creates a new public CDN on a document library in your SharePoint Online Tenant

## SYNTAX

```
New-SPOPublicCdnOrigin [-Url] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new Public CDN Origin in your SPO Tenant

## EXAMPLES

### EXAMPLE 1

```powershell
New-SPOPublicCdnOrigin -URL https://contoso.sharepoint.com/sites/CDN/CDNFilesLibrary/
```

This example shows how to you can setup a new Public CDN on a document library in your SharePoint online tenant.

## PARAMETERS

### -Url

> Applicable: SharePoint Online

Specify the URL that will be enabled for Public CDN in your tenant

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Introduction to the SharePoint Online management shell](https://support.office.com/en-us/article/introduction-to-the-sharepoint-online-management-shell-c16941c3-19b4-4710-8056-34c034493429)

[SharePoint Online Management Shell Download](https://www.microsoft.com/en-US/download/details.aspx?id=35588)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Get-SPOPublicCdnOrigins](Get-SPOPublicCdnOrigins.md)

[Remove-SPOPublicCdnOrigin](Remove-SPOPublicCdnOrigin.md)
