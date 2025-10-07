---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/new-spositegroup
applicable: SharePoint Online
title: New-SPOSiteGroup
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# New-SPOSiteGroup

## SYNOPSIS

Creates a new group in a SharePoint Online site collection.

## SYNTAX

```
New-SPOSiteGroup -Site <SpoSitePipeBind> -Group <String> -PermissionLevels <String[]> [<CommonParameters>]
```

## DESCRIPTION

A SharePoint group is a set of individual users.
SharePoint groups enable you to manage sets of users instead of individual users.

You must be at least a SharePoint Online administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
New-SPOSiteGroup -Site https://contoso.sharepoint.com/sites/siteA -Group "Project Leads" -PermissionLevels "Full Control"
```

This example creates a group named Project Leads with the Full Control permission level on the site collection <https://contoso.sharepoint.com/sites/siteA.>

### EXAMPLE 2

```powershell
New-SPOSiteGroup -Site https://contoso.sharepoint.com/sites/marketing -Group "NewGroupName" -PermissionLevels "Design"
```

This example creates a group named NewGroupName with the Design permission level on the site collection <https://contoso.sharepoint.com/sites/marketing.>

## PARAMETERS

### -Group

> Applicable: SharePoint Online

Specifies the name of the group to add.

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

### -PermissionLevels

> Applicable: SharePoint Online

Specifies the permission levels to grant to the newly created group. It can be any permission level that exists on the site collection on which the group is being created.

> [!NOTE]
> Permission Levels, are defined on the top-level site of the site collection, please see [How to create and edit permission levels](/sharepoint/how-to-create-and-edit-permission-levels) for more information.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site

> Applicable: SharePoint Online

Specifies the site collection to add the group to.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[New-SPOSite](New-SPOSite.md)
