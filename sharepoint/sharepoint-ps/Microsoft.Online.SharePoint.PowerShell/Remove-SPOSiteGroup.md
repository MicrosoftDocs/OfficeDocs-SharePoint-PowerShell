---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spositegroup
applicable: SharePoint Online
title: Remove-SPOSiteGroup
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Remove-SPOSiteGroup

## SYNOPSIS

Removes a SharePoint Online group from a site collection.

## SYNTAX

```
Remove-SPOSiteGroup -Site <SpoSitePipeBind> -Identity <String> [<CommonParameters>]
```

## DESCRIPTION

Use the `Remove-SPOSiteGroup` cmdlet to remove a group from a site collection by specifying the name of the group in the Identity parameter.

You must be at least a SharePoint Online administrator and be a site collection administrator to run the `Remove-SPOSiteGroup` cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### -----------------------EXAMPLE-----------------------------

```powershell
Remove-SPOSiteGroup -Site https://contoso.sharepoint.com/sites/marketing -Identity GroupToRemove
```

This example removes a group named GroupToRemove from the site collection <https://contoso.sharepoint.com/sites/marketing.>

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the name of the group to remove.

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

Specifies the site collection to remove the group from.

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

[New-SPOSiteGroup](New-SPOSiteGroup.md)
