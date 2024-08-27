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

Removes entries from the Content Security Policy configuration.

## SYNTAX

### Default

```powershell
Remove-SPOContentSecurityPolicy [-Url] <String>
```

## DESCRIPTION

Removes all entries associated with the given url from the Content Security Policy configuration. 
In multi-geo environments Content Security Policy entries are unique to each geo.

## PARAMETERS

### -Url

Url of the Content Security Policy entries to be removed.

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
