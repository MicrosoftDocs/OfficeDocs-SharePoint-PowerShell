---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spofilerequestbrandingprofiles
applicable: SharePoint Online
title: Get-SPOFileRequestBrandingProfiles
author: nabeelnaiyer
ms.author: nabeelnaiyer
ms.reviewer:
manager: ahackett
schema: 2.0.0
---

# Get-SPOFileRequestBrandingProfiles

## SYNOPSIS

Retrieves branding profiles configured for the file request feature, including details about logo and background assets.

## SYNTAX

```
Get-SPOFileRequestBrandingProfiles [<CommonParameters>]
```

## DESCRIPTION

The Get-SPOFileRequestBrandingProfiles cmdlet returns the branding profiles currently configured for the file request feature in the tenant. Each profile contains metadata about the logo and background image assets, such as file name and file URL. The cmdlet will output the asset library URL being used, along with information for both the primary and secondary branding profiles (if present). Each tenant can have at most one primary and one secondary branding profile.

## EXAMPLES

### Example 1

This example sets https://contoso.sharepoint.com/sites/branding/Assets/ as the organization asset library containing branding images for file request pages. It adds a branding profile using LogoA.jpg and BackgroundA.jpg, whose server-relative paths are provided via the LogoFileUrl and BackgroundFileUrl parameters. The IsPrimary flag indicates whether this profile should be treated as the primary branding profile for the tenant. In this example, the profile is being set as the primary profile.

```powershell
Get-SPOFileRequestBrandingProfiles
```

## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-SPOFileRequestBrandingProfile](/powershell/module/sharepoint-online/add-spofilerequestbrandingprofile)

[Remove-SPOFileRequestBrandingProfile](/powershell/module/sharepoint-online/remove-spofilerequestbrandingprofile)

[Switch-SPOFileRequestBrandingProfiles](/powershell/module/sharepoint-online/switch-spofilerequestbrandingprofiles)
