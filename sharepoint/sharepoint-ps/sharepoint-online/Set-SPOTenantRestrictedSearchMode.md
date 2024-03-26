---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spotenantrestrictedsearchmode
applicable: SharePoint Online
title: Set-SPOTenantRestrictedSearchMode
schema: 2.0.0
author: praporwal-microsoft
ms.author: praporwal
ms.reviewer:
---

# Set-SPOTenantRestrictedSearchMode

## SYNOPSIS

Set the mode for the restricted search setting.

## SYNTAX

```powershell
Set-SPOTenantRestrictedSearchMode -Mode {Disabled | Enabled} [<CommonParameters>]
```

## DESCRIPTION

Enable or disable the restricted search setting for the tenant. When the cmdlet is run for the first time, the allow list will be empty.

## EXAMPLES

### EXAMPLE 1

```powershell
Set-SPOTenantRestrictedSearchMode -Mode Enabled
```

This example enables the restricted search mode for the tenant.

### EXAMPLE 2

```powershell
Set-SPOTenantRestrictedSearchMode -Mode Disabled
```

This example disables the restricted search mode for the tenant.

## PARAMETERS

### -Mode

The restricted search mode to set for the tenant.

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

[Get-SPOTenantRestrictedSearchAllowedList](Get-SPOTenantRestrictedSearchAllowedList.md)

[Add-SPOTenantRestrictedSearchAllowedList](Add-SPOTenantRestrictedSearchAllowedList.md)

[Remove-SPOTenantRestrictedSearchAllowedList](Remove-SPOTenantRestrictedSearchAllowedList.md)
