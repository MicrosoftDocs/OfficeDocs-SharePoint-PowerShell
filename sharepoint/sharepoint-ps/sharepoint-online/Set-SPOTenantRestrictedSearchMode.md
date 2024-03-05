---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spotenantrestrictedsearchmode
applicable: SharePoint Online
title: Set-SPOTenantRestrictedSearchMode
schema: 2.0.0
author: praporwal
ms.author: praporwal
ms.reviewer:
---

# Set-SPOTenantRestrictedSearchMode

## SYNOPSIS

Enable or disabled the Restricted Search setting with the default being disabled. The first time when the setting is enabled the allow list is empty.


## SYNTAX

```powershell
Set-SPOTenantRestrictedSearchMode -Mode {Disabled | Enabled} [<CommonParameters>]
```

## DESCRIPTION

Enable or disabled the Restricted Search setting with the default being disabled. The first time when the setting is enabled the allow list is empty.

## EXAMPLES

### EXAMPLE 1

```powershell
Set-SPOTenantRestrictedSearchMode -Mode Enabled
```

This example sets or enables the Restricted Tenant Search mode for the tenant.

### EXAMPLE 2

```powershell
Set-SPOTenantRestrictedSearchMode -Mode Disabled
```

This example disables the Restricted Tenant Search mode for the tenant.

## PARAMETERS

### -Mode

Sets the mode for the Restricted Tenant Search.

```yaml
Type: String
Parameter Sets: (All)
Applicable: SharePoint Online

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## RELATED LINKS

[Get-SPOTenantRestrictedSearchMode](Get-SPOTenantRestrictedSearchMode.md)
