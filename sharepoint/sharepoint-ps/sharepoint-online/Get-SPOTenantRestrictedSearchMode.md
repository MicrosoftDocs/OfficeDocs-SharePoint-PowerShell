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

Get the current mode of Restricted Search setting.

## SYNTAX

```powershell
Get-SPOTenantRestrictedSearchMode
```

## DESCRIPTION

Restricted SharePoint Search gives Global and SharePoint Administrators the ability to enable or disable organization-wide search. The Get-SPOTenantRestrictedSearchMode cmdlet will return the current mode that is set in the tenant.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantRestrictedSearchMode
```

This example lets the administrator get the existing allowed list in the tenant. Result can be 'Enabled' or 'Disabled' based on the current setting.

## RELATED LINKS

[Set-SPOTenantRestrictedSearchMode](Set-SPOTenantRestrictedSearchMode.md)
