---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spotenantrestrictedsearchallowedlist
applicable: SharePoint Online
title: Remove-SPOTenantRestrictedSearchAllowedList
schema: 2.0.0
author: praporwal
ms.author: praporwal
ms.reviewer:
---

# Remove-SPOTenantRestrictedSearchAllowedList

## SYNOPSIS

Remove a list of sites from the allowed list.

## SYNTAX

```powershell
Remove-SPOTenantRestrictedSearchAllowedList -SitesList <List[string]> [<CommonParameters>]
```

```powershell
Remove-SPOTenantRestrictedSearchAllowedList -SitesListFileUrl <string> [-ContainsHeader <bool>] [<CommonParameters>]
```

## DESCRIPTION

Restricted SharePoint Search gives an ability to Global and SharePoint Administrators to enable or disable organization wide search. This control, when enabled offers up to 100 sites to be allowed in organization wide search, includes user's previously accessed files and includes content from user's frequent sites. Allow list is a set of curated sites where the administrator has reviewed the permissions and has applied data governance on them. Allow list will support sites, hub sites and communication sites. This command gives the ability to remove sites from existing allowed list so they can be removed from organization wider search.  

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOTenantRestrictedSearchAllowedList-SitesList @("https://contoso.sharepoint.com/sites/Marketing", "https://contoso.sharepoint.com/sites/Benefits")
```

This example lets the administrator remove the sites to the allowed list.

### EXAMPLE 2

```powershell
Remove-SPOTenantRestrictedSearchAllowedList -SitesListFileUrl .\AllowList.csv
```

This example lets the administrator remove the sites from the allowed list by giving a CSV file containing the list of site URLs.

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

File that has list of site URLs that can be added to an allowed list when the tenant is set to restricted tenant search mode.

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

Below is a sample input file containing site URLs without header.

```console
https://contosomarketing.sharepoint.com/sites/CommunicationSite
https://contosomarketing.sharepoint.com/sites/Finance
https://contosomarketing.sharepoint.com/sites/Marketing
https://contosomarketing.sharepoint.com/sites/TestSite
```

### -ContainsHeader

Indicate whether CSV file contains header. If set to True, the first row in file will be treated as header and will be skipped.

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

[Add-SPOTenantRestrictedSearchAllowedList](Add-SPOTenantRestrictedSearchAllowedList.md)
[Get-SPOTenantRestrictedSearchAllowedList](Get-SPOTenantRestrictedSearchAllowedList.md)
