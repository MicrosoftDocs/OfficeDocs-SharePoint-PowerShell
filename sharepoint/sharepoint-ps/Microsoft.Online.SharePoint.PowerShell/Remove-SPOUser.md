---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/remove-spouser
applicable: SharePoint Online
title: Remove-SPOUser
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Remove-SPOUser

## SYNOPSIS

Removes a user or a security group from a site collection or a group.

## SYNTAX

```
Remove-SPOUser -Site <SpoSitePipeBind> -LoginName <String> [-Group <String>] [<CommonParameters>]
```

## DESCRIPTION

You must be at least a SharePoint Online administrator and be a site collection administrator to run the `Remove-SPOUser` cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE

```powershell
Remove-SPOUser -Site https://contoso.sharepoint.com/sites/sc1 -LoginName joe.healy@contoso.com -Group "SC1 Owners"
```

This example removes a user who has the email address joe.healy@contoso.com from the group SC1 Owners in the site collection <https://contoso.sharepoint.com/sites/sc1.>

## PARAMETERS

### -Group

> Applicable: SharePoint Online

Specifies the group to remove the user from. If not specified, the cmdlet removes the user from all groups.

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

### -LoginName

> Applicable: SharePoint Online

Specifies the user name.

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

### -Site

> Applicable: SharePoint Online

Specifies the site collection to remove the user from.

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

[Get-SPOUser](Get-SPOUser.md)
