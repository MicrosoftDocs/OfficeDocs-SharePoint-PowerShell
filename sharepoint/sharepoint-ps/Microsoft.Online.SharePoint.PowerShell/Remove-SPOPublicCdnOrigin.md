---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/remove-spopubliccdnorigin
applicable: SharePoint Online
title: Remove-SPOPublicCdnOrigin
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Remove-SPOPublicCdnOrigin

## SYNOPSIS

Removes a given public CDN origin based on its identity (id) in your SharePoint Online Tenant

## SYNTAX

```
Remove-SPOPublicCdnOrigin [-Identity] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet will remove a Public CDN Origin based on its identity.

## EXAMPLES

### EXAMPLE 1

```powershell
#Get a list of CDN origins

Get-SPOPublicCdnOrigins
Id                                                                       Url
--                                                                       ---
11270051ee79e73829f6e7a3ee5d900d49c4fc5901645c642b799ecb62787a5069ca80fb HTTPS://CONTOSO.SHAREPOINT.COM/SITES/CDN...
#then remove the CDN by Identity id GUID.
Remove-SPOPublicCdnOrigin -Identity 11270051ee79e73829f6e7a3ee5d900d49c4fc5901645c642b799ecb62787a5069ca80fb
```

This example returns a list of CDN origins and then removes an origin based on the identity.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

It's the unique identifier of the Public CDN path, it can be queried using the Cmdlet Get-SpoPublicCdnOrigins

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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Add-SPOGeoAdministrator](Add-SPOGeoAdministrator.md)

[New-SPOPublicCdnOrigin](New-SPOPublicCdnOrigin.md)
