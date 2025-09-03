---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spoorgassetslibrary
applicable: SharePoint Online
title: Set-SPOOrgAssetsLibrary
author: Maralesfahanpoor
ms.author: maesfaha
ms.reviewer:
manager: paulac
schema: 2.0.0
ms.date: 07/30/2025
---

# Set-SPOOrgAssetsLibrary

## SYNOPSIS

Updates information for a library that is designated as a location for organization assets.

## SYNTAX

```
Set-SPOOrgAssetsLibrary -LibraryUrl <String> [-ThumbnailUrl <String>] [-OrgAssetType <OrganizationAssetType>]
 [-CopilotSearchable <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The Set-SPOOrgAssetsLibrary cmdlet updates information for a library that is designated as a location for organization assets. Updating the thumbnail URL and OrgAssetType are currently supported.

## EXAMPLES

### Example 1

This example updates the thumbnail URL publicly displayed for the library to contosologo2.jpg.

```powershell
Set-SPOOrgAssetsLibrary -LibraryURL sites/branding/Assets -ThumbnailURL https://contoso.sharepoint.com/sites/branding/Assets/contosologo2.jpg
```

### Example 2

This example removes the thumbnail URL that was previously set for the library.

```powershell
Set-SPOOrgAssetsLibrary -LibraryURL sites/branding/Assets -ThumbnailURL ""
```

### Example 3

This example changes the OrgAssetType to OfficeTemplateLibrary.

```powershell
Set-SPOOrgAssetsLibrary -LibraryURL sites/branding/Templates -OrgAssetType OfficeTemplateLibrary
```

### Example 4

This example changes the OrgAssetType to "ImageDocumentLibrary,OfficeTemplateLibrary".

```powershell
Set-SPOOrgAssetsLibrary -LibraryURL sites/branding/Templates -OrgAssetType ImageDocumentLibrary,OfficeTemplateLibrary
```

## PARAMETERS

### -CopilotSearchable

> Applicable: SharePoint Online

Specifies whether the library is made available to Microsoft 365 Copilot Search.

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

Indicates the server relative URL of the library to be modified.

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

### -OrgAssetType

> Applicable: SharePoint Online

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
Default value: None
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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/add-spoorgassetslibrary)

[Get-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/get-spoorgassetslibrary)

[Remove-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/remove-spoorgassetslibrary)
