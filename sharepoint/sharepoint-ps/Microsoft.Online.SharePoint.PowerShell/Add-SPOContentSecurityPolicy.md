---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spocontentsecuritypolicy
applicable: SharePoint Online
title: Add-SPOContentSecurityPolicy
schema: 2.0.0
author: jaobrie
ms.author: jaobrie
manager: ryannak
ms.reviewer:
---

# Add-SPOContentSecurityPolicy

## SYNOPSIS

Adds a source to the **Content Security Policy** configuration.

## SYNTAX

```
Add-SPOContentSecurityPolicy [-Source] <String> [<CommonParameters>]
```

## DESCRIPTION

Adds a source to the **Content Security Policy** configuration.
The source will be added to the `script-src` directive during construction of the `Content-Security-Policy` header.
In multi-geo environments, **Content Security Policy** configuration is unique to each geo.

## EXAMPLES

## PARAMETERS

### -Source

> Applicable: SharePoint Online

Source to be added to the **Content Security Policy** configuration.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:


Required: True
Position: 0
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

[Get-SPOContentSecurityPolicy](Get-SPOContentSecurityPolicy.md)

[Remove-SPOContentSecurityPolicy](Remove-SPOContentSecurityPolicy.md)

[Content Security Policy source values](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/Sources#sources)
