---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositescriptfromweb
applicable: SharePoint Online
title: Get-SPOSiteScriptFromWeb
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Get-SPOSiteScriptFromWeb

## SYNOPSIS

Creates site script syntax from an existing SharePoint site.

## SYNTAX

```
Get-SPOSiteScriptFromWeb [-WebUrl] <String> [-IncludedLists <String[]>] [-IncludeBranding] [-IncludeTheme]
 [-IncludeRegionalSettings] [-IncludeSiteExternalSharingCapability] [-IncludeLinksToExportedItems]
 [<CommonParameters>]
```

## DESCRIPTION

Uses an existing SharePoint site to output a JSON blob that can be used to create a site script for use in a site design.

## EXAMPLES

### Example 1

This example creates the site script output from an existing site - and writes it to a variable. This variable is then referenced to create a site script.

```powershell
C:\> $extracted = Get-SPOSiteScriptFromWeb `
    -WebUrl https://contoso.sharepoint.com/sites/template `
    -IncludeBranding `
    -IncludeTheme `
    -IncludeRegionalSettings `
    -IncludeSiteExternalSharingCapability `
    -IncludeLinksToExportedItems `
    -IncludedLists ("Shared%20Documents", "Lists/Project%20Activities")
C:\> Add-SPOSiteScript `
    -Title "Contoso template site" `
    -Description "This is a copy of a site collection." `
    -Content $extracted
```

## PARAMETERS

### -IncludeBranding

> Applicable: SharePoint Online

A switch that if provided, extracts the configuration of the site's branding.

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

### -IncludedLists

> Applicable: SharePoint Online

An array of one or more lists. Each is identified by the list url.

Note: Currently, navigation nodes are not exported.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeLinksToExportedItems

> Applicable: SharePoint Online

A switch that if provided, extracts navigation links. In order to export navigation links pointing to lists, the list needs to be included in the request as well.

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

### -IncludeRegionalSettings

> Applicable: SharePoint Online

A switch that if provided, extracts the site's regional settings.

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

### -IncludeSiteExternalSharingCapability

> Applicable: SharePoint Online

A switch that if provided, extracts the site's external sharing capability.

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

### -IncludeTheme

> Applicable: SharePoint Online

A switch that if provided, extracts the site's custom theme by using the themeJson property.

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

### -WebUrl

> Applicable: SharePoint Online

The url that starts with HTTPS of the site to retrieve the site script.

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
