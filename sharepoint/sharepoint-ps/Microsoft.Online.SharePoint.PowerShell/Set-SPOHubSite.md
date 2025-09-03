---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spohubsite
applicable: SharePoint Online
title: Set-SPOHubSite
schema: 2.0.0
author: trent-green
ms.author: speedta
ms.reviewer:
---

# Set-SPOHubSite

## SYNOPSIS

Sets the hub site information such as name, logo, and description.

## SYNTAX

```
Set-SPOHubSite [-Identity] <SpoHubSitePipeBind> [-Title <String>] [-LogoUrl <String>] [-Description <String>]
 [-SiteDesignId <Guid>] [-RequiresJoinApproval <Boolean>] [-HideNameInNavigation <Boolean>]
 [-EnablePermissionsSync <Boolean>] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to set properties such as name, logo, and description. These properties appear for the hub in the SharePoint user interface.

If the hub site doesn't exist, this cmdlet returns a "File not found" error.

## EXAMPLES

### Example 1

```powershell
Set-SPOHubSite https://contoso.sharepoint.com/sites/Marketing `
-Title "Marketing Hub" `
-LogoUrl https://contoso.sharepoint.com/sites/Marketing/SiteAssets/hublogo.png `
-Description "Hub for the Marketing division"
```

This example updates the name of the hub displayed in the SharePoint user interface. It also updates the logo used in the hub navigation, and specifies an optional description for the hub.

## PARAMETERS

### -Description

> Applicable: SharePoint Online

A description of the hub site.

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

### -EnablePermissionsSync

> Applicable: SharePoint Online

Whether to enable permission sync to the associated sites.

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

### -HideNameInNavigation

> Applicable: SharePoint Online

Whether to include the hub site name and logo in the hub site navigation.

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

### -Identity

> Applicable: SharePoint Online

URL of the hub site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoHubSitePipeBind
Parameter Sets: (All)
Aliases: HubSite

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LogoUrl

> Applicable: SharePoint Online

The URL of a logo to use in the hub navigation.

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

### -RequiresJoinApproval

> Applicable: SharePoint Online

Determines if joining a Hub site requires approval.

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

### -SiteDesignId

> Applicable: SharePoint Online

Site Design ID, for example db752673-18fd-44db-865a-aa3e0b28698e

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

### -Title

> Applicable: SharePoint Online

The display name of the hub.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoHubSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
