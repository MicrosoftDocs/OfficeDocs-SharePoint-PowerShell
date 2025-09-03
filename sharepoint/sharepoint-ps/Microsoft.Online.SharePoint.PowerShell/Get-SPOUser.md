---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spouser
applicable: SharePoint Online
title: Get-SPOUser
schema: 2.0.0
author: trent-green
ms.author: speedta
ms.reviewer:
---

# Get-SPOUser

## SYNOPSIS

Returns the SharePoint Online user or security group accounts that match a given search criteria.

## SYNTAX

### All (Default)
```
Get-SPOUser -Site <SpoSitePipeBind> [-Limit <String>] [<CommonParameters>]
```

### ByGroup
```
Get-SPOUser -Site <SpoSitePipeBind> [-Group <String>] [-Limit <String>] [<CommonParameters>]
```

### ByLogin
```
Get-SPOUser -Site <SpoSitePipeBind> [-LoginName <String>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet Parameter Sets](/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The `Get-SPOUser` cmdlet matches one and only one user or security group.

Be sure to run the `Get-SPOUser` cmdlet as at least a SharePoint Online administrator and be a site collection administrator of the queried site.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at <https://go.microsoft.com/fwlink/p/?LinkId=251832>.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOUser -Site https://contoso.sharepoint.com/sites/finance
```

Example 1 returns all user or security group accounts from the site collection <https://contoso.sharepoint.com/sites/finance>.

### EXAMPLE 2

```powershell
Get-SPOUser -Site https://contoso.sharepoint.com/sites/finance -LoginName melissa.kerr@contoso.com
```

Example 2 returns one user or security group account whose user name is "melissa.kerr@contoso.com" from the site collection <https://contoso.sharepoint.com/sites/finance>.

### EXAMPLE 3

```powershell
Get-SPOUser -Site https://contoso.sharepoint.com/sites/finance -Group "Team Site Members"
```

Example 3 returns one user or security group account inside group Team Site Members from the site collection <https://contoso.sharepoint.com/sites/finance>.

## PARAMETERS

### -Group

> Applicable: SharePoint Online

Specifies the group to get the users from.

```yaml
Type: System.String
Parameter Sets: ByGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit

> Applicable: SharePoint Online

Specifies the maximum number of users returned. The default value is to return 500 users. To return all users specify the value "All".

```yaml
Type: System.String
Parameter Sets: All, ByGroup
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
Parameter Sets: ByLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site

> Applicable: SharePoint Online

Specifies the URL of the site collection to get the user from.

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [About_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Remove-SPOUser](Remove-SPOUser.md)

[Set-SPOUser](Set-SPOUser.md)
