---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spotenantrenamesiteprioritization
applicable: SharePoint Online
title: Set-SPOTenantRenameSitePrioritization
author: AnfraMsft
ms.author: anfra
ms.reviewer: anushmag
manager: anushmag
schema: 2.0.0

---

# Set-SPOTenantRenameSitePrioritization
## SYNOPSIS
Allows prioritization of a site for early execution, as part of [Advanced Tenant Rename](/sharepoint/change-your-sharepoint-domain-name#advanced-tenant-rename-preview).
## SYNTAX
```
Set-SPOTenantRenameSitePrioritization -SiteUrl <String> [<CommonParameters>]
```
## DESCRIPTION
Allows for the specified site to be prioritized. 

As part of [Advanced Tenant Rename](/sharepoint/change-your-sharepoint-domain-name#advanced-tenant-rename-preview), organizations can prioritize up to 4,000 sites for initial execution among all other sites in your organization as part of the overall rename operation.

It is possible to start prioritizing sites only once the rename operation has been scheduled using the [Start-SPOTenantRename](Start-SPOTenantRename.md) cmdlet.

Please note that prioritizing a site is not a guarantee that it will complete first. There are several factors that can affect processing times, and multiple site renames are processed in parallel. Prioritized sites have a much higher chance of completing first.

You must be at least a SharePoint administrator to run the cmdlet.

## EXAMPLES

### Example 1

```powershell
Set-SPOTenantRenameSitePrioritization -SiteUrl https://contoso.sharepoint.com/sites/projectx
```

This example prioritizes the 'projectx' site within the Advanced Tenant Rename.

## PARAMETERS

### -SiteUrl

Specifies the full site URL of the site you wish to prioritize. This can be either a OneDrive for Business or SharePoint Online site. Root URLs (e.g., contoso.sharepoint.com, contoso-admin.sharepoint.com or contoso-my.sharepoint.com) can't be prioritized.
```yaml

Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Advanced Tenant Rename](https://aka.ms/advancedtenantrename)
