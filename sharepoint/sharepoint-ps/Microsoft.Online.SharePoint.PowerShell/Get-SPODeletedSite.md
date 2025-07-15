---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spodeletedsite
applicable: SharePoint Online
title: Get-SPODeletedSite
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPODeletedSite

## SYNOPSIS

Returns all deleted site collections from the Recycle Bin.

## SYNTAX

### ParameterSetAllSites (Default)
```
Get-SPODeletedSite [[-Identity] <SpoSitePipeBind>] [-Limit <String>] [-IncludePersonalSite]
 [<CommonParameters>]
```

### ParameterSetPersonalSitesOnly
```
Get-SPODeletedSite [[-Identity] <SpoSitePipeBind>] [-Limit <String>] [-IncludeOnlyPersonalSite]
 [<CommonParameters>]
```

## DESCRIPTION

The `Get-SPODeletedSite` cmdlet returns all deleted site collections that match the given criteria from the Recycle Bin.

By default the cmdlet only returns site and site collections that are not Personal Sites (My Sites).
To include personal sites, use the IncludePersonalSite parameter.
To return only Personal Sites, use the IncludeOnlyPersonalSite parameter.

These two Switch Parameters are in different parameter sets, so you can only use either one of them but not both.

This action does not restore these returned sites or site collection.
It only returns their properties so that you can see what sites or site collections have been deleted.
To restore the site or site collections, forward the results to the `Restore-SPODeletedSite` cmdlet in the pipeline.

You must be a SharePoint Online administrator and be a site collection administrator for the deleted site collections to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Get-SPODeletedSite -IncludePersonalSite
```

The command in this example returns all deleted site collections from the Recycle Bin including Personal Sites.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the URL of the deleted site collection to be returned.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:


Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IncludeOnlyPersonalSite

> Applicable: SharePoint Online

Use this switch parameter to only include Personal Sites in the returned results.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetPersonalSitesOnly
Aliases:


Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludePersonalSite

> Applicable: SharePoint Online

Use this switch parameter to include Personal Sites with the returned results.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetAllSites
Aliases:


Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit

> Applicable: SharePoint Online

Specifies the maximum number of site collections to return.
It can be any number.
To retrieve all site collections, use ALL.
The default value is 200.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Restore-SPODeletedSite](Restore-SPODeletedSite.md)

[Remove-SPODeletedSite](Remove-SPODeletedSite.md)
