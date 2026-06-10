---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/set-spocustomfontcatalog
applicable: SharePoint Online
title: Set-SPOCustomFontCatalog
schema: 2.0.0
---

# Set-SPOCustomFontCatalog

## SYNOPSIS

Generates an organization fonts catalog and uploads the font files and catalog files to a SharePoint Organization Asset Library.

## SYNTAX

```
Set-SPOCustomFontCatalog -LibraryUrl <SpoSitePipeBind> -FontFolder <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The `Set-SPOCustomFontCatalog` cmdlet generates the catalog files that make organization fonts available in supported Microsoft 365 apps, including PowerPoint and Word, and uploads the catalog files and font files to a SharePoint Organization Asset Library.

Before you run this cmdlet, designate the target document library as an Organization Asset Library for organization fonts by running `Add-SPOOrgAssetsLibrary` with `-OrgAssetType OfficeFontLibrary` and `-CdnType Public`.

The local font folder must contain the complete set of font files that you want published. The folder must be local, must not contain subfolders, and must only contain font files. To add, update, or remove fonts later, update the local folder so it contains the complete desired set of fonts, including unchanged fonts, and then run this cmdlet again.

Updates to Organization Asset Libraries for organization fonts can take up to 24 hours to propagate.

> [!WARNING]
> By using this feature and publishing font files, a font catalog file will be created. The newly created font catalog files will be publicly stored, along with the fonts, in the cloud and will not respect the site classification guidelines if the Organization Asset Library is hosted on a Restricted SharePoint Site. The font catalog files will contain font names and other font-related metadata. Please note that the files will be accessible to anyone, including persons external to your organization, who are able to extract the URLs that point to them.
>
> These newly created files can be deleted by you. If deleted, the feature will not work as expected.
>
> Do not use this feature if your fonts contain proprietary information, or if they have license usage restrictions, such as restrictions on cloud hosting, or if your organization isn't comfortable making the fonts publicly available.

## EXAMPLES

### Example 1

```powershell
Add-SPOOrgAssetsLibrary -LibraryUrl https://contoso.sharepoint.com/sites/branding/FontLibrary -OrgAssetType OfficeFontLibrary -CdnType Public
Set-SPOCustomFontCatalog -FontFolder "C:\ContosoFonts" -LibraryUrl https://contoso.sharepoint.com/sites/branding/FontLibrary
```

This example designates the FontLibrary document library as an Organization Asset Library for organization fonts and uploads the fonts from `C:\ContosoFonts` with the generated font catalog files.

### Example 2

```powershell
Set-SPOCustomFontCatalog -FontFolder "C:\ContosoFonts" -LibraryUrl https://contoso.sharepoint.com/sites/branding/FontLibrary
```

This example replaces the published organization font set with the complete set of fonts in `C:\ContosoFonts`.

### Example 3

```powershell
Set-SPOCustomFontCatalog -FontFolder "C:\ContosoFonts" -LibraryUrl https://contoso.sharepoint.com/sites/branding/FontLibrary -Verbose
```

This example uploads the fonts and displays additional font validation details and font menu previews.

## PARAMETERS

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FontFolder

> Applicable: SharePoint Online

Specifies the local folder that contains the font files to upload. The folder must be a local path, must contain at least one supported font file, must not contain subfolders, and must only contain font files.

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

### -LibraryUrl

> Applicable: SharePoint Online

Specifies the absolute URL of the SharePoint document library that is designated as an Organization Asset Library for organization fonts. The library must be added by using `Add-SPOOrgAssetsLibrary -OrgAssetType OfficeFontLibrary -CdnType Public`.

Only include the direct path to the document library. Don't include a view page, such as `/AllItems.aspx`.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Online

Shows what would happen if the cmdlet runs. Note that the cmdlet is not actually run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

You may be prompted to enter your credentials again during upload.

Use the `-Verbose` common parameter to show additional non-blocking font validation information and font menu previews. Verbose output can include validation warnings, informational messages about font characteristics, and previews of how font families and faces will appear in Office font menus.

## RELATED LINKS

[Add-SPOOrgAssetsLibrary](Add-SPOOrgAssetsLibrary.md)

[Get-SPOOrgAssetsLibrary](Get-SPOOrgAssetsLibrary.md)

[Remove-SPOOrgAssetsLibrary](Remove-SPOOrgAssetsLibrary.md)

[Support for organization fonts in PowerPoint and Word](/sharepoint/support-for-organization-fonts-in-powerpoint-for-the-web)
