---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/copy-spopersonalsitepage
applicable: SharePoint Online
title: Copy-SPOPersonalSitePage
schema: 2.0.0
author: xuyangzou
ms.author: xuyangzou, spodeanu
ms.reviewer:
---

# Copy-SPOPersonalSitePage

## SYNOPSIS

This cmdlet command allows you to relocate existing SharePoint pages by utilizing an existing copy operation. We will also copy any assets associated with the SharePoint pages to the new destination. We offer two methods for relocating pages:
- Copy: This method keeps the original page intact while creating a duplicate at the new location.
- Move: This method creates a new copy at the new location and deletes the original page from the source.

## SYNTAX

### CopySinglePage

```powershell
Copy-SPOPersonalSitePage -SourceSite <SpoSitePipeBind> -DestinationSite <SpoSitePipeBind> -PageName <String> -DeleteSourcePage <Boolean> [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The Copy-SPOPersonalSitePage cmdlet allows a SharePoint Administrator to copy one or more SharePoint pages from a selected source to a chosen destination SharePoint site. If the '-DeleteSourcePage' parameter is set to '$true', the source page(s) will be deleted after the copy operation, effectively moving the page(s).

> [!NOTE]
> The Copy-SPOPersonalSitePage cmdlet may not be available in all tenants as the feature rollout could be in progress. If the feature has not been enabled in your tenant, attempting to run this cmdlet will result in an error.

**Where can I move the existing page(s) to and from?**

| Source | Destination |
| :------------------- | :---------- | 
| SharePoint pages library in OneDrive for Business  | SharePoint pages library in OneDrive for Business | 
| SharePoint pages library in OneDrive for Business | SharePoint site | 
| SharePoint site    | SharePoint site | 

### How do I query the status of my copy operation?

After the cmdlet is executed, you'll see the status code of the copy operation. If the copy was successful, we'll provide the URL for the new page.

If the copy is still in progress, you'll get a message with a URL. You can paste this link into your browser to check the status of the copy job. The 'JobState' property will show a number indicating the job's status.

```powershell
https://contoso.sharepoint.com/sites/testsite/_api/sitepages/pages/CopyToStatus('243925c7-cea7-4430-bb90-299ed9122d0b').
```
The following table explains the meaning of each number that indicates the job’s status:
| Number | Code status | Explanation |
| :----- | :---------- | :---------- | 
| 0 | Queued | The copy operation was queued for execution. |
| 1 | CreateAssetsFolderStart | We’ve started creating a folder to place all associated assets used on this page. |
| 2 | CreateAssetsFolderEnd | We’ve finished creating a folder to place all associated assets used on this page. |
| 3 | CopyAssetsStart | We’ve started copying associated assets used on this page. |
| 4 | CopyAssetsEnd | We’ve finished copying associated assets used on this page. |
| 5 | CreatePageStart | We’ve started creating a new page. |
| 6 | CreatePageEnd | We’ve finished creating a new page. |
| 7 | Succeeded | The copy operation was successful. |
| 8 | Deleting | The copy operation was deleted. |
| 9 | Failed | The copy operation failed. |
| 10 | JobNotFound | The copy operation wasn’t found. |

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Copy-SPOPersonalSitePage -SourceSite 'https://contoso-my.sharepoint.com/personal/testuser_onmicrosoft_com' -DestinationSite 'https://contoso-my.sharepoint.com/sites/testsite' -PageName 'TestPage.aspx' -Confirm 
```

Example 1 demonstrates how a SharePoint Administrator can copy the SharePoint page named `TestPage.aspx` from `testuser`'s SharePoint pages library in OneDrive to the `testsite` SharePoint site with confirmation. The source page will not be deleted.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Copy-SPOPersonalSitePage -SourceSite 'https://contoso-my.sharepoint.com/personal/testuser_onmicrosoft_com' -DestinationSite 'https://contoso-my.sharepoint.com/sites/testsite' -PageName 'TestPage.aspx' -DeleteSourcePage $true
```

Example 2 demonstrates how a SharePoint Administrator can move the SharePoint page named `TestPage.aspx` from `testuser`'s SharePoint pages library in OneDrive for Business to the `testsite` SharePoint site. The source page will be deleted after the copy operation.

### -----------------------EXAMPLE 3-----------------------------

```powershell
Copy-SPOPersonalSitePage -SourceSite 'https://contoso-my.sharepoint.com/sites/sourcesite' -DestinationSite 'https://contoso-my.sharepoint.com/sites/testsite' -PageName 'TestPage.aspx' -DeleteSourcePage $true -Confirm
```

Example 3 demonstrates how a SharePoint Administrator can copy the SharePoint page named `TestPage.aspx` from a SharePoint site name `sourcesite` to the `testsite` SharePoint site with confirmation. The source page will be deleted after the copy operation.

## PARAMETERS

### -SourceSite

Specifies the URL of the source SharePoint site containing the SharePoint pages to copy.

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

### -DestinationSite

Specifies the URL of the destination SharePoint site where the SharePoint pages will be copied to.

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

### -PageName

Specifies the name of the SharePoint page to copy. This parameter is required when not using the `-AllPages` switch.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteSourcePage

Indicates whether to delete the source SharePoint page(s) after copying. If set to $true, the operation will move the SharePoint page(s) instead of copying.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## NOTES

### Will SharePoint pages retain their version history after the move?
Currently, only the latest published version will be transferred.

### Can recipients of SharePoint pages I shared with continue to access them after the move?
All permissions will be removed once the pages are moved.

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
