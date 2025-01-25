---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-sporestrictedsitecreation
applicable: SharePoint Online
title: Get-SPORestrictedSiteCreation
schema: 2.0.0
author: vgaddam-pm
ms.author: vgaddam
ms.reviewer:
---

# Get-SPORestrictedSiteCreation

## SYNOPSIS

This cmdlet allows SharePoint administrators to check the current configuration of the restricted site creation feature.

## SYNTAX

```powershell
Get-SPORestrictedSiteCreation [-SiteType <RestrictedSiteCreationSiteType>]
```

## DESCRIPTION

This cmdlet obtains the current configuration information for the restricted site creation feature, including whether it is enabled, the current mode, and the current policies.

> [!Important]
>You must use version 16.0.25513.12000 (published November 2024) or later of the [SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) for these commands to function properly. Earlier versions do not have the current list of site types and will not operate correctly.

## EXAMPLES

### Example 1

```powershell
Get-SPORestrictedSiteCreation
```

Example 1 returns all configuration information for the restricted site creation feature. This includes whether the feature is enabled, the current mode (deny or allow), and the Microsoft Entra security groups configured for each site type.

### Example 2

```powershell
Get-SPORestrictedSiteCreation –SiteType Communication
```

Example 2 returns a comma-separated list of the IDs of the Microsoft Entra security groups configured for the `Communication` site type. Depending on whether restricted site creation is in allow or deny mode, members of these groups are either allowed or denied from creating SharePoint communication sites.

## PARAMETERS

### -SiteType
When provided, only return the Microsoft Entra security groups configured for the specified site type.

PARAMVALUE: All | SharePoint | OneDrive | Team | Communication
-	All - OneDrive and all SharePoint sites 
-	SharePoint - All SharePoint sites (but not OneDrive) 
-	OneDrive - Only OneDrive 
-	Team - Only SharePoint team sites (group-connected and classic) 
-	Communication - Only SharePoint communication sites

```yaml
Type: RestrictedSiteCreationSiteType
Parameter Sets: (All)
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).
