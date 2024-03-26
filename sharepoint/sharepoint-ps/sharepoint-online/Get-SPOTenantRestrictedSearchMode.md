---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenantrestrictedsearchmode
applicable: SharePoint Online
title: Get-SPOTenantRestrictedSearchMode
schema: 2.0.0
author: praporwal
ms.author: praporwal
ms.reviewer:
---

# Get-SPOTenantRestrictedSearchMode

## SYNOPSIS

Gets the current mode of the restricted search setting.

## SYNTAX

```powershell
Get-SPOTenantRestrictedSearchMode
```

## DESCRIPTION

This cmdlet returns the current restricted search mode that is set in the tenant.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantRestrictedSearchMode
```

This example gets the existing restricted search mode in the tenant. Result can be 'Enabled' or 'Disabled' based on the current setting.

## RELATED LINKS

[Set-SPOTenantRestrictedSearchMode](Set-SPOTenantRestrictedSearchMode.md)

[Get-SPOTenantRestrictedSearchAllowedList](Get-SPOTenantRestrictedSearchAllowedList.md)

[Add-SPOTenantRestrictedSearchAllowedList](Add-SPOTenantRestrictedSearchAllowedList.md)

[Remove-SPOTenantRestrictedSearchAllowedList](Remove-SPOTenantRestrictedSearchAllowedList.md)
