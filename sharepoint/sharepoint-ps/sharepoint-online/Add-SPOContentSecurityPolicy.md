---
external help file:
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

Adds an entry to the Content Security Policy configuration.

## SYNTAX

### Default

```powershell
Add-SPOContentSecurityPolicy [-Url] <String> [-Directive] <String> 
```

## DESCRIPTION

Adds an entry to the Content Security Policy configuration. 
The url in each entry will be added to the corresponding directive during construction of the Content-Security-Policy header.
Entries with a "*" directive will be applied to all directives.

## PARAMETERS

### -Url

Url to allow as part of this Content Security Policy entry.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Directive

Directive to allow as part of this Content Security Policy entry.
Currently allowed values are "*", "script-src" and "worker-src".

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## RELATED LINKS

[Get-SPOContentSecurityPolicy](Get-SPOContentSecurityPolicy.md)

[Remove-SPOContentSecurityPolicy](Remove-SPOContentSecurityPolicy.md)
