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

### What does this command do?
This cmdlet command enables you to relocate existing SharePoint pages by utilizing an existing copy operation. We will also copy any assets associated with the SharePoint pages to the new destination. We offer two methods for relocating pages:
- Copy: This method keeps the original page intact while creating a duplicate at the new location.
- Move: This method creates a new copy at the new location and deletes the original page from the source.

### Where can I move the existing page(s) to and from?

| Source | Destination |
| :------------------- | :---------- | 
| SharePoint pages library in OneDrive  | SharePoint pages library in OneDrive | 
| SharePoint pages library in OneDrive | SharePoint site | 
| SharePoint site    | SharePoint site | 

### How do I query the code status? 



## SYNTAX

### CopySinglePage

```powershell
Copy-SPOPersonalSitePage -SourceSite <SpoSitePipeBind> -DestinationSite <SpoSitePipeBind> -PageName <String> -DeleteSourcePage <Boolean> [-Confirm] [<CommonParameters>]
```

### CopyAllPages

```powershell
Copy-SPOPersonalSitePage -SourceSite <SpoSitePipeBind> -DestinationSite <SpoSitePipeBind> -AllPages -DeleteSourcePage <Boolean> -Confirm [<CommonParameters>]
```

## DESCRIPTION

The Copy-SPOPersonalSitePage cmdlet allows a SharePoint Online administrator to copy one or more SharePoint pages from a selected source to a chosen destination SharePoint site. If the -DeleteSourcePage parameter is set to $true, the source page(s) will be deleted after the copy operation, effectively moving the page(s).

> [!NOTE]
> This cmdlet may not be available in all tenants as the feature rollout could be in progress. If the feature has not been enabled in your tenant, attempting to run this cmdlet will result in an error.

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Copy-SPOPersonalSitePage -SourceSite 'https://prepspo-my.spgrid.com/personal/testuser_onmicrosoft_com' -DestinationSite 'https://prepspo.spgrid.com/sites/testsite' -PageName 'TestPage.aspx' -DeleteSourcePage $false -Confirm 
```

Example 1 demonstrates how a SharePoint Online administrator can copy the SharePoint page named `TestPage.aspx` from `testuser`'s SharePoint pages library in OneDrive to the `testsite` SharePoint site with confirmation. The source page will not be deleted.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Copy-SPOPersonalSitePage -SourceSite 'https://prepspo-my.spgrid.com/personal/testuser_onmicrosoft_com' -DestinationSite 'https://prepspo.spgrid.com/sites/testsite' -PageName 'TestPage.aspx' -DeleteSourcePage $true
```

Example 2 demonstrates how a SharePoint Online administrator can move the SharePoint page named `TestPage.aspx` from `testuser`'s SharePoint pages library in OneDrive to the `testsite` SharePoint site. The source page will be deleted after the copy operation.

### -----------------------EXAMPLE 3-----------------------------

```powershell
Copy-SPOPersonalSitePage -SourceSite 'https://prepspo-my.spgrid.com/personal/testuser_onmicrosoft_com' -DestinationSite 'https://prepspo.spgrid.com/sites/testsite' -AllPages -DeleteSourcePage $true -Confirm
```

Example 3 demonstrates how a SharePoint Online administrator can copy all SharePoint pages from `testuser`'s SharePoint pages library in OneDrive to the `testsite` SharePoint site with confirmation. All source pages will be deleted after the copy operation.

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

### -AllPages

Indicates that all SharePoint pages from the source SharePoint site are to be copied. This switch is required when copying all pages.

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

### Will SharePoint pages retain their version history after the move?
Currently, only the latest published version will be transferred.

### Can recipients of SharePoint pages I shared continue to access them after the move?
All permissions will be removed once the pages are moved.

## RELATED LINKS
