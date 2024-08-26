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

Adds an entry to the Content Security Policy configuration.

## SYNTAX

### Default

```powershell
Remove-SPOContentSecurityPolicy [-Url] <String> [-Directive] <String> 
```

## DESCRIPTION

Removes an entry to the Content Security Policy configuration. 
The url in each entry will be added to the corresponding directive during construction of the Content-Security-Policy header.
Entries with a "*" directive will be applied to all directives.

## PARAMETERS

### -Url

Url of the Content Security Policy entry to be removed.

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

Directive of the Content Security Policy entry to be removed.

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

[Add-SPOContentSecurityPolicy](Add-SPOContentSecurityPolicy.md)
