---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spolistdesign
schema: 2.0.0
author: reedpa-microsoft
ms.author: reedpa
ms.reviewer:
ms.topic: List Templates
title: Add-SPOListDesign
---

# Add-SPOListDesign

## SYNOPSIS
Creates a new list or document library design available to users when they create a new list or document library from site contents, certain site home pages, the SharePoint home page, the Microsoft Lists app, Microsoft Teams, or Office.com.

## SYNTAX

```
Add-SPOListDesign -Title <String> -SiteScripts <SPOSiteScriptPipeBind[]> [-Description <String>]
 [-ThumbnailUrl <String>] [-TemplateFeatures <String[]>] [-ListColor <SPOListDesignColor>]
 [-ListIcon <SPOListDesignIcon>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new list or document library design available to users when they create a new list or document library from the SharePoint home page, the Microsoft Lists app, Microsoft Teams, or Office.com.

List designs will be available in UI where lists are created, and document library designs will be available in UI where document libraries are created. The difference is based on the "templateType" of the site design used. "templateType" 100 is for Lists, "templateType" 101 is for document libraries.

## EXAMPLES

### Example 1

```powershell
PS > Add-SPOListDesign
    -Title "Contoso customer tracking"  
    -Description "Tracks key customer data in a list"  
    -SiteScripts "<ID>"  
    -ListColor Orange  
    -ListIcon BullseyeTarget  
    -Thumbnail "https://contoso.sharepoint.com/SiteAssets/site-thumbnail.png"
```

This example creates a new list or document library design.

## PARAMETERS

### -Description
The display description of the list or document library design.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListColor
Default color associated with the list when creating the list.

```yaml
Type: SPOListDesignColor
Parameter Sets: (All)
Aliases:
Accepted values: DarkRed, Red, Orange, Green, DarkGreen, Teal, Blue, NavyBlue, BluePurple, DarkBlue, Lavendar, Pink

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListIcon
Default icon associated with the list when creating the list.

```yaml
Type: SPOListDesignIcon
Parameter Sets: (All)
Aliases:
Accepted values: Bug, Calendar, BullseyeTarget, ClipboardList, Airplane, Rocket, Color, Insights, CubeShape, TestBeakerSolid, Robot, Savings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteScripts
An array of one or more site scripts. Each is identified by an ID. The scripts run in the order listed. 

```yaml
Type: SPOSiteScriptPipeBind[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemplateFeatures
Set of features that the template comes with. It is displayed as a bulleted list when the user is looking at the template preview in the list or document library creation dialog.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThumbnailUrl
The URL of a thumbnail image. If none is specified, SharePoint uses a generic image. Recommended size is 400 x 300 pixels.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title
The display name of the list or document library design.

```yaml
Type: String
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
