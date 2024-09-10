---
external help file:
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spocontentsecuritypolicy
applicable: SharePoint Online
title: Remove-SPOContentSecurityPolicy
schema: 2.0.0
author: jaobrie
ms.author: jaobrie
manager: ryannak
ms.reviewer:
---

# Remove-SPOContentSecurityPolicy

## SYNOPSIS

Removes a source from the **Content Security Policy** configuration.

## SYNTAX

### Default

```powershell
Remove-SPOContentSecurityPolicy [-Source] <String>
```

## DESCRIPTION

Removes the given source from the **Content Security Policy** configuration. 
In multi-geo environments, **Content Security Policy** configuration is unique to each geo.

## PARAMETERS

### -Source

Source to be removed from the **Content Security Policy** configuration.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## RELATED LINKS

[Get-SPOContentSecurityPolicy](Get-SPOContentSecurityPolicy.md)

[Add-SPOContentSecurityPolicy](Add-SPOContentSecurityPolicy.md)

[Content Security Policy source values](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/Sources#sources)