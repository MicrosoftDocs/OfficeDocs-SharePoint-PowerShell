---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/add-spofilerequestbrandingprofile
applicable: SharePoint Online
title: Add-SPOFileRequestBrandingProfile
author: nabeelnaiyer
ms.author: nabeelnaiyer
ms.reviewer:
manager: ahackett
schema: 2.0.0
---

# Add-SPOFileRequestBrandingProfile

## SYNOPSIS

Adds a branding profile for the file request feature by specifying logo and background assets from an existing organization asset library.

## SYNTAX

```
Add-SPOFileRequestBrandingProfile -AssetLibraryUrl <String> -IsPrimary <Boolean> [-LogoFileUrl <String>] [-BackgroundFileUrl <String>]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet registers a branding profile to be used for the file request feature across the tenant. You must specify an existing organization asset library URL where the branding assets are stored and indicate whether the profile should be designated as primary. Each tenant can have one primary and one secondary profile. The organization asset library being used must be configured with the CdnType being "Public" (see [Add-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/add-spoorgassetslibrary) for more info).

## EXAMPLES

### Example 1

```powershell
Add-SPOFileRequestBrandingProfile -AssetLibraryUrl "https://contoso.sharepoint.com/sites/branding/Assets" -LogoFileUrl "/sites/branding/Assets/LogoA.jpg" -BackgroundFileUrl "/sites/branding/Assets/BackgroundA.jpg" -IsPrimary $true
```

This example sets https://contoso.sharepoint.com/sites/branding/Assets/ as the organization asset library containing branding images for file request pages. It adds a branding profile using LogoA.jpg and BackgroundA.jpg, whose server-relative paths are provided via the LogoFileUrl and BackgroundFileUrl parameters. The `-IsPrimary` flag indicates whether this profile should be treated as the primary branding profile for the tenant. In this example, the profile is being set as the primary profile.

### Example 2

```powershell
Add-SPOFileRequestBrandingProfile -AssetLibraryUrl "https://contoso.sharepoint.com/sites/branding/Assets" -LogoFileUrl "/sites/branding/Assets/LogoB.jpg" -BackgroundFileUrl "/sites/branding/Assets/BackgroundB.jpg" -IsPrimary $false
```

This example sets https://contoso.sharepoint.com/sites/branding/Assets/ as the organization asset library containing branding images for file request pages. It adds a branding profile using LogoB.jpg and BackgroundB.jpg, whose server-relative paths are provided via the LogoFileUrl and BackgroundFileUrl parameters. The `-IsPrimary` flag indicates whether this profile should be treated as the primary branding profile for the tenant. In this example, the profile is NOT being set as the primary profile.

## PARAMETERS

### -AssetLibraryUrl

> Applicable: SharePoint Online

Specifies the absolute URL of the asset library containing the branding assets.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogoFileUrl

Specifies the relative URL of the logo image file.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackgroundFileUrl

Specifies the relative URL of the background image file.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsPrimary
Specifies if this branding profile configuration is the primary profile.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOFileRequestBrandingProfiles](/powershell/module/sharepoint-online/get-spofilerequestbrandingprofiles)

[Remove-SPOFileRequestBrandingProfile](/powershell/module/sharepoint-online/remove-spofilerequestbrandingprofile)

[Switch-SPOFileRequestBrandingProfiles](/powershell/module/sharepoint-online/switch-spofilerequestbrandingprofiles)
