---
external help file:
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontentsecuritypolicy
applicable: SharePoint Online
title: Get-SPOContentSecurityPolicy
schema: 2.0.0
author: jaobrie
ms.author: jaobrie
manager: ryannak
ms.reviewer:
---

# Get-SPOContentSecurityPolicy

## SYNOPSIS

Returns all entries in the current **Content Security Policy** configuration.

## SYNTAX

### Default

```powershell
Get-SPOContentSecurityPolicy
```

## DESCRIPTION

Returns all entries in the current **Content Security Policy** configuration.
The url in each entry will be added to the corresponding directive during construction of the `Content-Security-Policy` header.

## RELATED LINKS

[Add-SPOContentSecurityPolicy](Add-SPOContentSecurityPolicy.md)

[Remove-SPOContentSecurityPolicy](Remove-SPOContentSecurityPolicy.md)
