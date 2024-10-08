---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositepages
applicable: SharePoint Online
title: Get-SPOSitePages
schema: 2.0.0
author: xuyangzo
ms.author: xuyangzou
ms.reviewer:
---

# Get-SPOSitePages

## SYNOPSIS

This cmdlet allows you to retrieve all SharePoint pages under a specific SharePoint site.

## SYNTAX

```powershell
Get-SPOSitePages -Site <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

After this cmdlet is executed, the information for each SharePoint page will be displayed with the following properties:

| Property             | Description                              |
| :------------------- | :--------------------------------------- |
| Name                 | The name of the SharePoint page.                    |
| Title                | The title of the SharePoint page.                   |
| UniqueId             | The unique ID of the SharePoint page.               |
| CreatedDateTime      | The creation date and time of the SharePoint page.       |
| LastModifiedDateTime | The last modified date and time of the SharePoint page. |
| CreatedBy            | The creator of the SharePoint page.                 |

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPOSitePages -Site 'https://contoso.sharepoint.com/sites/testsite'
```

Example 1 demonstrates how a SharePoint Administrator can retrieve all the SharePoint pages under the `testsite`.


## PARAMETERS

### -Site

Specifies the URL of the SharePoint site from which to fetch the SharePoint pages.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).


## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Copy-SPOPersonalSitePage.md](./Copy-SPOPersonalSitePage.md)

[Get-SPOPersonalSitePageCopyProgress.md](./Get-SPOPersonalSitePageCopyProgress.md)
