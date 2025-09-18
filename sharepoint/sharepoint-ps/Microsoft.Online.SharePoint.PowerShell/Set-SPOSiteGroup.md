---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/set-spositegroup
applicable: SharePoint Online
title: Set-SPOSiteGroup
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Set-SPOSiteGroup

## SYNOPSIS

Updates the SharePoint Online owner and permission levels on a group inside a site collection.

## SYNTAX

```
Set-SPOSiteGroup -Site <SpoSitePipeBind> -Identity <String> [-Name <String>]
 [-PermissionLevelsToAdd <String[]>] [-PermissionLevelsToRemove <String[]>] [-Owner <String>]
 [<CommonParameters>]
```

## DESCRIPTION

You must be at least a SharePoint Online administrator and be a site collection administrator to run the `Set-SPOSiteGroup` cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
Set-SPOSiteGroup -Site https://contoso.sharepoint.com/sites/siteA -Identity "ProjectViewers" -PermissionLevelsToRemove "Full Control" -PermissionLevelsToAdd "View Only"
```

Example 1 changes permission level of the ProjectViewers group inside site collection <https://contoso.sharepoint.com/sites/siteA> from Full Control to View Only.

### EXAMPLE 2

```powershell
Set-SPOSiteGroup -Site https://contoso.sharepoint.com -Identity "ProjectViewers" -Owner Melissa.kerr@contoso.com
```

Example 2 sets Melissa.kerr@contoso.com as the owner of the ProjectViewers group.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the name of the group.

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

### -Name

> Applicable: SharePoint Online

Specifies the new name of the group.

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

### -Owner

> Applicable: SharePoint Online

Specifies the owner (individual or a security group) of the group to be created.

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

### -PermissionLevelsToAdd

> Applicable: SharePoint Online

Specifies the permission levels to grant to the group.

> [!NOTE]
> Permission levels are defined by SharePoint Online administrators from SharePoint Online Administration Center.

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

### -PermissionLevelsToRemove

> Applicable: SharePoint Online

Specifies the permission levels to remove from the group.

> [!NOTE]
> Permission levels are defined by SharePoint Online administrators from SharePoint Online Administration Center.

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

### -Site

> Applicable: SharePoint Online

Specifies the site collection the group belongs to.

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

[Get-SPOSiteGroup](Get-SPOSiteGroup.md)
