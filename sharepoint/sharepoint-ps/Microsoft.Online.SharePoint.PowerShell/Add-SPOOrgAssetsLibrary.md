---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spoorgassetslibrary
applicable: SharePoint Online
title: Add-SPOOrgAssetsLibrary
author: Maralesfahanpoor
ms.author: maesfaha
ms.reviewer:
manager: paulac
schema: 2.0.0
---

# Add-SPOOrgAssetsLibrary

## SYNOPSIS

Designates a library to be used as a central location for organization assets across the tenant.

## SYNTAX

```
Add-SPOOrgAssetsLibrary -LibraryUrl <String> [-ThumbnailUrl <String>] [-OrgAssetType <OrganizationAssetType>]
 [-CdnType <SPOTenantCdnType>] [-NoDefaultOrigins] [-CopilotSearchable <Boolean>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The Add-SPOOrgAssetsLibrary cmdlet designates a library to be a central location for organization assets across the tenant. Once this cmdlet is run, assets stored within this library are available to sites across the tenant.  The name publicly displayed for the library will be the organization's name. Note that it may take from a couple of hours to a day for changes to be reflected.

## EXAMPLES

### Example 1

This example adds https://contoso.sharepoint.com/sites/branding/Assets as a designated library for organization assets. Assets is the name of the SharePoint library added. The thumbnail publicly displayed for the library is contosologo.jpg, from that same library.

```powershell
Add-SPOOrgAssetsLibrary -LibraryURL https://contoso.sharepoint.com/sites/branding/Assets -ThumbnailURL https://contoso.sharepoint.com/sites/branding/Assets/contosologo.jpg
```
### Example 2

This example adds https://contoso.sharepoint.com/sites/branding/Templates as a designated library for organization assets. Templates is the name of the SharePoint library added and will be the name publicly displayed for the library. The thumbnail publicly displayed for the library is contosologo.jpg, from that same library. OrgAssetType is the type of SharePoint library.

```powershell
Add-SPOOrgAssetsLibrary -LibraryURL https://contoso.sharepoint.com/sites/branding/Templates -ThumbnailURL https://contoso.sharepoint.com/sites/branding/Templates/contosologo.jpg -OrgAssetType OfficeTemplateLibrary
```

## PARAMETERS

### -CdnType

> Applicable: SharePoint Online

Specifies the CDN type. The valid values are public or private.

Note: The manually configured Private CDN is in the process of being deprecated. For more information, see [Use the Office 365 Content Delivery Network (CDN) with SharePoint Online](/microsoft-365/enterprise/use-microsoft-365-cdn-with-spo).

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SPOTenantCdnType
Parameter Sets: (All)
Aliases:

Accepted values: Public, Private

Required: False
Position: Named
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### -CopilotSearchable
{{ Fill CopilotSearchable Description }}

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

### -LibraryUrl

> Applicable: SharePoint Online

Indicates the absolute URL of the library to be designated as a central location for organization assets.

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

### -NoDefaultOrigins
{{ Fill NoDefaultOrigins Description }}

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrgAssetType

Indicates the type of content in this library. Currently supported values are "ImageDocumentLibrary" and "OfficeTemplateLibrary".

ImageDocumentLibrary is the default OrgAssetType and is best used for images. You can access the contents of this library from any site or page in the SharePoint filepicker.
OfficeTemplateLibrary is the suggested type for Office files and will show up in the UI of all Office desktop apps and Office online in the templates section.

In order to benefit from both UIs you can choose "ImageDocumentLibrary,OfficeTemplateLibrary" as OrgAssetType.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.OrganizationAssetType
Parameter Sets: (All)
Aliases:
Accepted values: ImageDocumentLibrary, OfficeTemplateLibrary, OfficeFontLibrary, BrandKitLibrary

Required: False
Position: Named
Default value: ImageDocumentLibrary
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThumbnailUrl

> Applicable: SharePoint Online

Indicates the URL of the background image used when the library is publicly displayed. If no thumbnail URL is indicated, the card will have a gray background.

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

### -Confirm
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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/get-spoorgassetslibrary)

[Set-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/set-spoorgassetslibrary)

[Remove-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/remove-spoorgassetslibrary)
