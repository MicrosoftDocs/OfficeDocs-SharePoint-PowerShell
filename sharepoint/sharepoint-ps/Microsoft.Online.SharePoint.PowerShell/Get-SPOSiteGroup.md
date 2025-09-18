---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spositegroup
applicable: SharePoint Online
title: Get-SPOSiteGroup
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Get-SPOSiteGroup

## SYNOPSIS

Gets all the groups on the specified site collection.

## SYNTAX

```
Get-SPOSiteGroup -Site <SpoSitePipeBind> [-Group <String>] [-Limit <Int32>] [<CommonParameters>]
```

## DESCRIPTION

Use the `Get-SPOSiteGroup` cmdlet to get all the groups on the specified site collection by using the Site parameter.

You must be a SharePoint Online administrator and a site collection administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [SharePoint Online PowerShell](/powershell/module/microsoft.online.sharepoint.powershell/index).

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOSiteGroup -Site https://contoso.sharepoint.com/sites/siteA
```

This example returns all the groups on the specified site collection <https://contoso.sharepoint.com/sites/siteA.>

## PARAMETERS

### -Group

> Applicable: SharePoint Online

Specifies the group name.

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

### -Limit

> Applicable: SharePoint Online

Specifies the maximum number of groups to return. The default value is 200.

```yaml
Type: System.Int32
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

Specifies the site collection scope.

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

[Set-SPOSiteGroup](Set-SPOSiteGroup.md)

[Remove-SPOSiteGroup](Remove-SPOSiteGroup.md)
