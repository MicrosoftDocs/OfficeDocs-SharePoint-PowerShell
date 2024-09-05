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

Returns all sources in the current **Content Security Policy** configuration.

## SYNTAX

### Default

```powershell
Get-SPOContentSecurityPolicy
```

## DESCRIPTION

Returns all sources in the current **Content Security Policy** configuration.
Each source will be added to the `script-src` directive during construction of the `Content-Security-Policy` header.

## RELATED LINKS

[Add-SPOContentSecurityPolicy](Add-SPOContentSecurityPolicy.md)

[Remove-SPOContentSecurityPolicy](Remove-SPOContentSecurityPolicy.md)
