---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://docs.microsoft.com/powershell/module/sharepoint-online/Get-SPOBuiltInSiteTemplateSettings
applicable: SharePoint Online
title: Get-SPOBuiltInSiteTemplateSettings
schema: 2.0.0
author: Holland-ODSP
ms.author: hokavian
ms.reviewer:
---

# Get-SPOBuiltInSiteTemplateSettings

## SYNOPSIS

Get the current state of Microsoft-provided SharePoint site templates displayed or hidden in the site template gallery in your tenant.

## SYNTAX

```powershell
Get-SPOBuiltInSiteTemplateSettings -Identity <object>
```

## DESCRIPTION

The `Get-SPOBuiltInSiteTemplateSettings` cmdlet displays the current state of Microsoft-provided SharePoint site templates displayed or hidden in the site template gallery in your tenant. 

>[!NOTE]
> - All site templates are displayed by default. [Learn more](support.microsoft.com/office/apply-and-customize-sharepoint-site-templates-39382463-0e45-4d1b-be27-0e96aeec8398) about SharePoint site templates
> - You must have SharePoint admin credentials (or higher) to use SharePoint PowerShell.
> - The minimum SharePoint PowerShell version required is 16.0.21610.12000.
> - For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).


## EXAMPLE 

### ------------ Example 1 --------------------
This example checks what Microsoft-provided SharePoint site templates are currently hidden from the site template gallery. 

```powershell
Get-SPOBuiltInSiteTemplateSettings 
```

>[!NOTE]
> If a site template has never been hidden, it will not show up in the list. If a site template has been hidden, then changed back to displayed (i.e. currently set to True), then it will show up in the list. 


## PARAMETERS

#### -Identity
 
Specifies the ID for the site template if you'd like to filter results. 

```yaml
Type: String
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
Applies to: SharePoint Online
```

## RELATED LINKS

[Apply and customize SharePoint sites](support.microsoft.com/office/apply-and-customize-sharepoint-site-templates-39382463-0e45-4d1b-be27-0e96aeec8398)