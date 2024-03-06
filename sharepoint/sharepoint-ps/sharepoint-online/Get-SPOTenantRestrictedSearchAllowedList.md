---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenantrestrictedsearchallowedlist
applicable: SharePoint Online
title: Get-SPOTenantRestrictedSearchAllowedList
schema: 2.0.0
author: praporwal
ms.author: praporwal
ms.reviewer:
---

# Get-SPOTenantRestrictedSearchAllowedList

## SYNOPSIS

The Get-SPOTenantRestrictedSearchAllowedList cmdlet will return all the sites that are in the allowed list in the tenant.

## SYNTAX

```powershell
Get-SPOTenantRestrictedSearchAllowedList
```

## DESCRIPTION

Restricted SharePoint Search gives an ability to Global and SharePoint Administrators to enable or disable organization wide search. This control, when enabled offers up to 100 sites to be allowed in organization wide search, includes user's previously accessed files and includes content from user's frequent sites. Allow list is a set of curated sites where the administrator has reviewed the permissions and has applied data governance on them. Allow list will support sites, hub sites and communication sites.

The Get-SPOTenantRestrictedSearchAllowedList cmdlet will return all the sites that are in the allowed list in the tenant.  

You must be a SharePoint Online or global administrator to run the Get-SPOTenantRestrictedSearchAllowedList cmdlet.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantRestrictedSearchAllowedList
```

This example lets the administrator get the existing allowed list in the tenant.

## RELATED LINKS

[Add-SPOTenantRestrictedSearchAllowedList](Add-SPOTenantRestrictedSearchAllowedList.md)
[Remove-SPOTenantRestrictedSearchAllowedList](Remove-SPOTenantRestrictedSearchAllowedList.md)
