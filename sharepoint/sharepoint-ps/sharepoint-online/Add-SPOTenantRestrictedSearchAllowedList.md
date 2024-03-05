---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spotenantrestrictedsearchallowedlist
applicable: SharePoint Online
title: Add-SPOTenantRestrictedSearchAllowedList
schema: 2.0.0
author: praporwal
ms.author: praporwal
ms.reviewer:
---

# Add-SPOTenantRestrictedSearchAllowedList

## SYNOPSIS

This command lets the admin add the sites to the allowed list.

## SYNTAX

```powershell
Add-SPOTenantRestrictedSearchAllowedList -SitesList <List[string]> [<CommonParameters>]
```

```powershell
Add-SPOTenantRestrictedSearchAllowedList -SitesListFileUrl <string> [-ContainsHeader <bool>] [<CommonParameters>]
```

## DESCRIPTION

Restricted SharePoint Search gives Global/Tenant and SharePoint admins the ability to enable/disable organization-wide search. When enabled, this control offers up to 100 sites to be included in organization-wide search, including user's previously accessed files and content from user's frequent sites. The allow list is a set of curated sites where the customer has reviewed the permissions and applied data governance to them. The allow list supports Site Collections, Hub, and Communication sites.

## EXAMPLES

### EXAMPLE 1

```powershell
Add-SPOTenantRestrictedSearchAllowedList-SitesList @(“https://contoso.sharepoint.com/sites/Marketing”, “https://contoso.sharepoint.com/sites/Benefits”)
```

This example lets the admin add the sites to the allowed list.

### EXAMPLE 2

```powershell
Add-SPOTenantRestrictedSearchAllowedList -SitesListFileUrl .\AllowList.csv
```

This example lets the admin add the sites to the allowed list by giving a CSV file. Add the list of site URL’s in URL column.

## PARAMETERS

### -SitesList

Site list for allowed list.

```yaml
Type: String[]
Parameter Sets: SitesList
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SitesListFileUrl

File that has list of sites URLs that can be added to an allowed list when the tenant is set to Restricted Tenant Search Mode.

```yaml
Type: String
Parameter Sets: SitesListFileUrl
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainsHeader

Indicate whether CSV file contains header. If set to True, first row in file will be treated as header and will be skipped.

```yaml
Type: Boolean
Parameter Sets: SitesListFileUrl
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## RELATED LINKS

[Remove-SPOTenantRestrictedSearchAllowedList](Remove-SPOTenantRestrictedSearchAllowedList.md)
[Get-SPOTenantRestrictedSearchAllowedList](Get-SPOTenantRestrictedSearchAllowedList.md)
