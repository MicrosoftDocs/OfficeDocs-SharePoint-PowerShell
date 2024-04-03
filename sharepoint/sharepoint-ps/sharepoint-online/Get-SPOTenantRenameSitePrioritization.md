---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenantrenamesiteprioritization
applicable: SharePoint Online
title: Get-SPOTenantRenameSitePrioritization
author: AnfraMsft
ms.author: anfra
ms.reviewer: anushmag
manager: anushmag
schema: 2.0.0
ms.topic: reference
---

# Get-SPOTenantRenameSitePrioritization
## SYNOPSIS
Returns the list of sites that are prioritized for early execution, as part of Advanced Tenant Rename.
## SYNTAX
```
Get-SPOTenantRenameSitePrioritization [<CommonParameters>]
```
## DESCRIPTION
This cmdlet can be used to view the currently prioritized sites, as part of Advanced Tenant Rename. 

The output is a list of all site URLs, one per row. If desired, the output can be downloaded using the standard PowerShell Out-File option. If you want just the count of prioritized sites, you can use the standard Measure option.

You must be a SharePoint or Global Administrator to run this cmdlet.
## EXAMPLES
### Example 1
```powershell
Get-SPOTenantRenameSitePrioritization
```
This example will return the list of sites prioritized for the Advanced Tenant Rename scheduled in the tenant, if one exists. 
### Example 2
```powershell
Get-SPOTenantRenameSitePrioritization | measure
```
This example will return the count of prioritized sites.
### Example 3
```powershell
Get-SPOTenantRenameSitePrioritization | Out-File -FilePath <path>
```
This example will download the list of prioritized sites to the specified path. 
## PARAMETERS
### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).
## INPUTS
### None
## OUTPUTS
### System.Object
## NOTES
## RELATED LINKS
[Advanced Tenant Rename](https://aka.ms/advancedtenantrename)
