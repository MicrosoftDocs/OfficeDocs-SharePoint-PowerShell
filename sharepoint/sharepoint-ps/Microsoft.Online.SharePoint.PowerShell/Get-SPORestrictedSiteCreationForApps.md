---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-sporestrictedsitecreationforapps
applicable: SharePoint Online
title: Get-SPORestrictedSiteCreationForApps
schema: 2.0.0
author: vgaddam-pm
ms.author: vgaddam
ms.reviewer:
---

# Get-SPORestrictedSiteCreationForApps

## SYNOPSIS

This cmdlet allows SharePoint Administrators to check the current configuration of the restricted site creation for apps feature.

## SYNTAX

```
Get-SPORestrictedSiteCreationForApps [-SiteType <RestrictedSiteCreationSiteType>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet obtains the current configuration information for the restricted site creation for apps feature, including whether it is enabled, the current mode, and the current policies.

> [!Note]
> This feature is currently in preview and may not be available in your tenant.

## EXAMPLES

### Example 1

```powershell
Get-SPORestrictedSiteCreationForApps
```

Example 1 returns all configuration information for the restricted site creation for apps feature. This includes whether the feature is enabled, the current mode (deny or allow), and the app IDs configured for each site type.

### Example 2

```powershell
Get-SPORestrictedSiteCreation –SiteType Communication
```

Example 2 returns a comma-separated list of the app IDs for the `Communication` site type. Depending on whether restricted site creation is in allow or deny mode, these apps are either allowed or denied from creating SharePoint communication sites.

## PARAMETERS

### -SiteType

> Applicable: SharePoint Online
When provided, only return the Microsoft Entra security groups configured for the specified site type.

PARAMVALUE: All | SharePoint | OneDrive | Team | Communication
-	All - OneDrive and all SharePoint sites
-	SharePoint - All SharePoint sites (but not OneDrive)
-	OneDrive - Only OneDrive
-	Team - Only SharePoint team sites (group-connected and classic)
-	Communication - Only SharePoint communication sites

```yaml
Type: Microsoft.SharePoint.Administration.SPOnlineProvisioning.RestrictedSiteCreationSiteType
Parameter Sets: (All)
Aliases:
Accepted values: All, SharePoint, OneDrive, Team, Communication

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).
