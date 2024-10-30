---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spotenantrenamesiteprioritization
applicable: SharePoint Online
title: Remove-SPOTenantRenameSitePrioritization
author: AnfraMsft
ms.author: anfra
ms.reviewer: anushmag
manager: anushmag
schema: 2.0.0

---

# Remove-SPOTenantRenameSitePrioritization
## SYNOPSIS
Allows removal of the prioritization previously assigned to a site for early execution, as part of [Advanced Tenant Rename](/sharepoint/change-your-sharepoint-domain-name#advanced-tenant-rename-preview).
## SYNTAX
```
Remove-SPOTenantRenameSitePrioritization -SiteUrl <String> [<CommonParameters>]
```
## DESCRIPTION
This cmdlet can be used to remove priority previously assigned to a site as part of [Advanced Tenant Rename](/sharepoint/change-your-sharepoint-domain-name#advanced-tenant-rename-preview).

Removing prioritization from a site means that it will be not be queued for initial execution as part of the overall rename operation. The site will still be queued for processing subsequently like any other unprioritized site, and does not get skipped from the rename.

You must be at least a SharePoint administrator to run the cmdlet.

## EXAMPLES

### Example 1

```powershell
Remove-SPOTenantRenameSitePrioritization -SiteUrl https://contoso.sharepoint.com/sites/projectx
```

This example removes the 'projectx' site from the prioritized list of sites within the Advanced Tenant Rename.

## PARAMETERS

### -SiteUrl

Specifies the full site URL of the site you wish to prioritize. This can be either a OneDrive for Business or SharePoint Online site. Only a site that is currently prioritized can be removed.

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
