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

Restricted SharePoint Search gives Global/Tenant and SharePoint admins the ability to enable/disable organization-wide search. The Get-SPOTenantRestrictedSearchMode cmdlet will return the current mode that is set in the tenant.


## SYNTAX

```powershell
Get-SPOTenantRestrictedSearchMode
```

## DESCRIPTION

Restricted SharePoint Search gives Global/Tenant and SharePoint admins the ability to enable/disable organization-wide search. The Get-SPOTenantRestrictedSearchMode cmdlet will return the current mode that is set in the tenant.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantRestrictedSearchMode
```

This example lets the admin get the existing allowed list in the tenant. Result can be ‘Enabled’ or ‘Disabled’ based on the current setting.

## RELATED LINKS

[Set-SPOTenantRestrictedSearchMode](Set-SPOTenantRestrictedSearchMode.md)
