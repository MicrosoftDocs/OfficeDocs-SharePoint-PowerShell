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

Removes a list of sites from the allowed list.

## SYNTAX

```powershell
Remove-SPOTenantRestrictedSearchAllowedList -SitesList <List[string]> [<CommonParameters>]
```

```powershell
Remove-SPOTenantRestrictedSearchAllowedList -SitesListFileUrl <string> [-ContainsHeader <bool>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet removes the given sites from existing allowed list so they can be removed from organization wider search.

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOTenantRestrictedSearchAllowedList -SitesList @("https://contoso.sharepoint.com/sites/Marketing", "https://contoso.sharepoint.com/sites/Benefits")
```

This example removes the given sites from restricted search allowed list.

### EXAMPLE 2

```powershell
Remove-SPOTenantRestrictedSearchAllowedList -SitesListFileUrl .\AllowList.csv
```

This example removes the given sites from the restricted search allowed list by giving a CSV file containing the list of site URLs.

## PARAMETERS

### -SitesList

List of sites to be removed from the allowed list.

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

File that has the list of site URLs to be removed from restricted search allowed list when the tenant is set to restricted tenant search mode. Below is a sample input file containing site URLs without header.

```console
https://contosomarketing.sharepoint.com/sites/CommunicationSite
https://contosomarketing.sharepoint.com/sites/Finance
https://contosomarketing.sharepoint.com/sites/Marketing
https://contosomarketing.sharepoint.com/sites/TestSite
```

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

Indicates whether the given CSV file contains header. If set to True, the first row in the file will be treated as the header and will be skipped.

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

[Get-SPOTenantRestrictedSearchMode](Get-SPOTenantRestrictedSearchMode.md)

[Set-SPOTenantRestrictedSearchMode](Set-SPOTenantRestrictedSearchMode.md)

[Get-SPOTenantRestrictedSearchAllowedList](Get-SPOTenantRestrictedSearchAllowedList.md)

[Add-SPOTenantRestrictedSearchAllowedList](Add-SPOTenantRestrictedSearchAllowedList.md)
