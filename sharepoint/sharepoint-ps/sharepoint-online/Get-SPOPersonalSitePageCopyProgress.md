---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spopersonalsitepagecopyprogress
applicable: SharePoint Online
title: Get-SPOPersonalSitePageCopyProgress
schema: 2.0.0
author: xuyangzo
ms.author: xuyangzou
ms.reviewer:
---

# Get-SPOPersonalSitePageCopyProgress

## SYNOPSIS

This cmdlet enables you to track the progress of a SharePoint page's copy operation.

## SYNTAX

```powershell
Get-SPOPersonalSitePageCopyProgress -DestinationSite <SpoSitePipeBind> -WorkItemId <Guid> [<CommonParameters>]
```

## DESCRIPTION

After this cmdlet is executed, you'll receive the following information:

| Property | Description |
| :------- | :---------- |
| ErrorMessage | The error message if there is an error. |
| JobState | The state of the job. |
| NewPageUrl | The URL of the new page if the copy is already finished. |
| SourcePageName | The name of the source page to copy. Will be empty. |
| StatusMessage | The message to describe the status. |
| WorkItemId | The work item id to track the status of the copy job if the copy job is in progress. |

The following table explains the copy job's state:

| Status | Explanation |
| :---------- | :---------- | 
| Queued | The copy operation was queued for execution. |
| CreateAssetsFolderStart | We've started creating a folder to place all associated assets used on this page. |
| CreateAssetsFolderEnd | We've finished creating a folder to place all associated assets used on this page. |
| CopyAssetsStart | We've started copying associated assets used on this page. |
| CopyAssetsEnd | We've finished copying associated assets used on this page. |
| CreatePageStart | We've started creating a new page. |
| CreatePageEnd | We've finished creating a new page. |
| Succeeded | The copy operation was successful. |
| Deleting | The copy operation was deleted. |
| Failed | The copy operation failed. |
| JobNotFound | The copy operation wasn't found. |

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPOPersonalSitePageCopyProgress -DestinationSite 'https://contoso.sharepoint.com/sites/testsite' -WorkItemId 1a95eb18-f68d-4dd4-9aaf-b47cf05cf02a
```

Example 1 shows how a SharePoint Administrator can check the status of a copy operation using a work item ID.


## PARAMETERS

### -DestinationSite

Specifies the URL of the destination SharePoint site to which the SharePoint page has been copied to.

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

### -WorkItemId

Specifies the GUID of the work item created for the copy job if it is asynchronous.

```yaml
Type: Guid
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

[Get-SPOSitePages.md](./Get-SPOSitePages.md)
