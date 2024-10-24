---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/copy-spopersonalsitepage
applicable: SharePoint Online
title: Copy-SPOPersonalSitePage
schema: 2.0.0
author: xuyangzo
ms.author: xuyangzou
ms.reviewer:
---

# Copy-SPOPersonalSitePage

## SYNOPSIS

This cmdlet command allows you to relocate existing SharePoint pages by utilizing an existing copy operation. We will also copy any assets associated with the SharePoint pages to the new destination. We offer two methods for relocating pages:
- Copy: This method keeps the original page intact while creating a duplicate at the new location.
- Move: This method creates a new copy at the new location and deletes the original page from the source.

## SYNTAX

```powershell
Copy-SPOPersonalSitePage -SourceSite <SpoSitePipeBind> -DestinationSite <SpoSitePipeBind> -PageName <String> -DeleteSourcePage <SwitchParameter> [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The Copy-SPOPersonalSitePage cmdlet allows a SharePoint Administrator to copy one or more SharePoint pages from a selected source to a chosen destination SharePoint site. If the `-DeleteSourcePage` parameter is set to `$true`, the source page(s) will be deleted after the copy operation, effectively moving the page(s).

> [!NOTE]
> This cmdlet may not be available in all tenants as the feature rollout could be in progress. If the feature has not been enabled in your tenant, attempting to run this cmdlet will result in an error.

**Where can I move the existing page(s) to and from?**

| Source | Destination |
| :------------------- | :---------- | 
| SharePoint pages library in OneDrive for Business  | SharePoint pages library in OneDrive for Business | 
| SharePoint pages library in OneDrive for Business | SharePoint site | 
| SharePoint site    | SharePoint site | 

**How do I query the status of my copy operation?**

After this cmdlet is executed, you'll receive the following information:

| Property | Description |
| :------- | :---------- |
| ErrorMessage | We will show the corresponding error message, if any error occurs. |
| JobState | The current state of the job. |
| NewPageUrl | 	The URL of the new page if the copy operation has completed. |
| SourcePageName | The name of the source page to be copied. |
| StatusMessage | A message describing the current status. |
| WorkItemId | The work item ID used to track the status of the copy job. If the copy operation is complete, this will be `00000000-0000-0000-0000-000000000000`. |

- If the copy is successful, the URL for the new page will be provided.
- If the copy is still in progress, you will receive the work item ID. You can use the [Get-SPOPersonalSitePageCopyProgress](./Get-SPOPersonalSitePageCopyProgress.md) command to check the status of the URL.

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
Copy-SPOPersonalSitePage -SourceSite 'https://contoso-my.sharepoint.com/personal/testuser_onmicrosoft_com' -DestinationSite 'https://contoso.sharepoint.com/sites/testsite' -PageName 'TestPage.aspx' -Confirm 
```

Example 1 demonstrates how a SharePoint Administrator can copy the SharePoint page named `TestPage.aspx` from `testuser`'s SharePoint pages library in OneDrive for Business to the `testsite` SharePoint site with confirmation. The source page will not be deleted.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Copy-SPOPersonalSitePage -SourceSite 'https://contoso-my.sharepoint.com/personal/testuser_onmicrosoft_com' -DestinationSite 'https://contoso.sharepoint.com/sites/testsite' -PageName 'TestPage.aspx' -DeleteSourcePage
```

Example 2 demonstrates how a SharePoint Administrator can move the SharePoint page named `TestPage.aspx` from `testuser`'s SharePoint pages library in OneDrive for Business to the `testsite` SharePoint site. The source page will be deleted after the copy operation.

### -----------------------EXAMPLE 3-----------------------------

```powershell
Copy-SPOPersonalSitePage -SourceSite 'https://contoso.sharepoint.com/sites/sourcesite' -DestinationSite 'https://contoso.sharepoint.com/sites/testsite' -PageName 'TestPage.aspx' -DeleteSourcePage -Confirm
```

Example 3 demonstrates how a SharePoint Administrator can copy the SharePoint page named `TestPage.aspx` from a SharePoint site name `sourcesite` to the `testsite` SharePoint site with confirmation. The source page will be deleted after the copy operation.

### -----------------------EXAMPLE 4-----------------------------

```powershell
Copy-SPOPersonalSitePage -SourceSite 'https://contoso-my.sharepoint.com/personal/testuser1_onmicrosoft_com' -DestinationSite 'https://contoso-my.sharepoint.com/personal/testuser2_onmicrosoft_com' -PageName 'TestPage.aspx' -DeleteSourcePage -Confirm
```

Example 4 demonstrates how a SharePoint Administrator can move the SharePoint page named `TestPage.aspx` from `testuser1`'s SharePoint pages library in OneDrive for Business to `testuser2`'s SharePoint pages library in OneDrive for Business with confirmation. The source page will be deleted after the copy operation.

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

Specifies the name of the SharePoint page to copy. This parameter is required when not using the `-AllPages` switch. Note that `-PageName` refers to the name of a SharePoint page that ends with the suffix .aspx, such as page.aspx.

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

Indicates whether to delete the source SharePoint page(s) after copying. If specified, the operation will move the SharePoint page(s) instead of copying.

```yaml
Type: SwitchParameter
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

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Notes

**Question: Will SharePoint pages retain their version history after the move?**

Answer: Currently, only the latest published version will be transferred.

**Question: Can recipients of SharePoint pages I shared with continue to access them after the move?**

Answer: All permissions will be removed once the pages are moved.

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOPersonalSitePageCopyProgress.md](./Get-SPOPersonalSitePageCopyProgress.md)

[Get-SPOSitePages.md](./Get-SPOSitePages.md)
