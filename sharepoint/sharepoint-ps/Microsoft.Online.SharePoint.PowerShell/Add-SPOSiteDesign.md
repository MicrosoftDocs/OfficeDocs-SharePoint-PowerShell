---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spositedesign
applicable: SharePoint Online
title: Add-SPOSiteDesign
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Add-SPOSiteDesign

## SYNOPSIS

Creates a new site design available to users when they create a new site from the SharePoint home page.

## SYNTAX

```
Add-SPOSiteDesign -Title <String> -WebTemplate <String> -SiteScripts <SPOSiteScriptPipeBind[]>
 [-Description <String>] [-ThumbnailUrl <String>] [-PreviewImageUrl <String>] [-PreviewImageAltText <String>]
 [-IsDefault] [-DesignPackageId <Guid>] [<CommonParameters>]
```

## DESCRIPTION

Creates a new site design available to users when they create a new site from the SharePoint home page.

## EXAMPLES

### Example 1

This example creates a new site design.

```powershell
Add-SPOSiteDesign `
  -Title "Contoso customer tracking" `
  -WebTemplate "64" `
  -SiteScripts "<ID>" `
  -Description "Tracks key customer data in a list" `
  -ThumbnailUrl "https://contoso.sharepoint.com/SiteAssets/site-thumbnail.png" `
  -PreviewImageUrl "https://contoso.sharepoint.com/SiteAssets/site-preview.png" `
  -PreviewImageAltText "site preview"
```

## PARAMETERS

### -Description

> Applicable: SharePoint Online

The display description of the site design.

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

### -DesignPackageId

> Applicable: SharePoint Online

The ID of the design package associated with the site design.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsDefault

> Applicable: SharePoint Online

A switch that if provided, applies the site design to the default site template. For more information, see [Customize a default site design](/sharepoint/dev/declarative-customization/customize-default-site-design).

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

### -PreviewImageAltText

> Applicable: SharePoint Online

The alt text description of the image for accessibility.

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

### -PreviewImageUrl

> Applicable: SharePoint Online

The URL of a preview image. If none is specified, SharePoint uses a generic image.

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

### -SiteScripts

> Applicable: SharePoint Online

An array of one or more site scripts. Each is identified by an ID. The scripts run in the order listed.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteScriptPipeBind[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThumbnailUrl

> Applicable: SharePoint Online

The URL of a thumbnail image. If none is specified, SharePoint uses a generic image. Recommended size is 400 x 300 pixels.

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

### -Title

> Applicable: SharePoint Online

The display name of the site design.

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

### -WebTemplate

> Applicable: SharePoint Online

Identifies which base template to add the design to. Use the value **64** for the Team site template, and the value **68** for the Communication site template.
For more information, visit [SharePoint site design and site script overview](/sharepoint/dev/declarative-customization/site-design-overview).

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
