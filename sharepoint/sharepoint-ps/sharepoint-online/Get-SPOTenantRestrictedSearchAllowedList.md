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

The Get-SPOTenantRestrictedSearchAllowedList cmdlet returns all the sites that are in the restricted search allowed list.

## SYNTAX

```powershell
Get-SPOTenantRestrictedSearchAllowedList
```

## DESCRIPTION

Restricted SharePoint search allows Global and SharePoint Administrators to enable or disable organization wide search. This control, when enabled offers up to 100 sites to be allowed in organization wide search, includes user's previously accessed files and includes content from user's frequent sites. Allow list is a set of curated sites where the administrator has reviewed the permissions and has applied data governance on them. Allow list will support sites, hub sites and communication sites.

This Get-SPOTenantRestrictedSearchAllowedList cmdlet returns all the sites that are in the restricted search allowed list.

You must be a SharePoint or Global Administrator to run this cmdlet.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantRestrictedSearchAllowedList
```

This gets the existing restricted search allowed list.

## RELATED LINKS

[Get-SPOTenantRestrictedSearchMode](Get-SPOTenantRestrictedSearchMode.md)
[Set-SPOTenantRestrictedSearchMode](Set-SPOTenantRestrictedSearchMode.md)
[Add-SPOTenantRestrictedSearchAllowedList](Add-SPOTenantRestrictedSearchAllowedList.md)
[Remove-SPOTenantRestrictedSearchAllowedList](Remove-SPOTenantRestrictedSearchAllowedList.md)