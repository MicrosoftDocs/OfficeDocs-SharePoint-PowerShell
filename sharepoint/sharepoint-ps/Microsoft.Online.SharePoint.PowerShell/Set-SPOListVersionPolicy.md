---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spolistversionpolicy
applicable: SharePoint Online
title: Set-SPOListVersionPolicy
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Set-SPOListVersionPolicy

## SYNOPSIS

Sets the version policy setting on the document library.

## SYNTAX

```
Set-SPOListVersionPolicy [-Site] <SpoSitePipeBind> -List <SPOListPipeBind>
 -EnableAutoExpirationVersionTrim <Boolean> [-ExpireVersionsAfterDays <Int32>] [-MajorVersionLimit <Int32>]
 [-MajorWithMinorVersionsLimit <Int32>] [<CommonParameters>]
```

## DESCRIPTION

Sets the version policy setting on the document library.

## EXAMPLES

### Example 1
```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -EnableAutoExpirationVersionTrim $true
```
Example 1 sets automatic version history limits on the document library called "Documents".

### EXAMPLE 2

```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -MajorWithMinorVersionsLimit 20 -ExpireVersionsAfterDays 30
```

Example 2 sets manual version histroy limits on the document library called "Documents" by limiting the number of versions and the time (in days) versions are kept.

### EXAMPLE 3

```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -MajorWithMinorVersionsLimit 20 -ExpireVersionsAfterDays 0
```

Example 3 sets manual version histroy limits on the document library called "Documents" by limiting the number of versions with no time limits. The new document libraries will use this version setting.

## PARAMETERS

### -EnableAutoExpirationVersionTrim

> Applicable: SharePoint Online
Global and SharePoint Administrators can set document library level version history limits settings that universally apply to new versions created.

When version history limits are managed automatically, SharePoint employs an algorithm behind the scenes that deletes (thins out) intermittent older versions that are least likely to be needed, while preserving sufficient high-value versions - more versions in the recent past and fewer farther back in time - in case restores are required.

The valid values are:

- True - Version history limits for new versions created on the document library will be managed automatically.
- False - Version history limits for new Versions created on the document library will be managed manually by setting limits to the number of major versions (`MajorVersionLimit`), number of major with minor versions (`MajorWithMinorVersionsLimit`) and time set (`ExpireVersionsAfterDays`). Review the documentation of both parameters to manage your organization's version limits manually.

> [!NOTE]
> When version history limits are managed manually (`EnableAutoExpirationVersionTrim $false`), `MajorVersionLimit`, `MajorWithMinorVersionsLimit` and `ExpireVersionsAfterDays` are required parameters with the following acceptable values:
> a. `MajorVersionLimit` accepts values from 1 through 50,000 (inclusive).
> b. `MajorWithMinorVersionsLimit` accepts values from 0 through 50,000 (inclusive).
> c. `ExpireVersionsAfterDays` accepts values of 0 to Never Expire or values >= 30 to delete versions that exceed that time period.
> When Version history limits are managed automatically (`EnableAutoExpirationVersionTrim $true`), setting `MajorVersionLimit` or `ExpireVersionsAfterDays` will result in an error as the count limits are set by the service.

PARAMVALUE: $true | $false

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpireVersionsAfterDays

> Applicable: SharePoint Online
When version history limits are managed manually (`EnableAutoExpirationVersionTrim $false`), admins will need to set the limits to the number of major versions (`MajorVersionLimit`), the number of major with minor versions (`MajorWithMinorVersionsLimit`) and the time period the versions are stored (`ExpireVersionsAfterDays`). Please check the description of `EnableAutoExpirationVersionTrim` for more details.

PARAMVALUE: Int32

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

### -List

The document library name or Id.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOListPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MajorVersionLimit

> Applicable: SharePoint Online
When version history limits are managed manually (`EnableAutoExpirationVersionTrim $false`), admins will need to set the limits to the number of major versions (`MajorVersionLimit`) and the time period the versions are stored (`ExpireVersionsAfterDays`). Please check the description of `EnableAutoExpirationVersionTrim` for more details.

PARAMVALUE: Int32

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

### -MajorWithMinorVersionsLimit

> Applicable: SharePoint Online
When version history limits are managed manually (`EnableAutoExpirationVersionTrim $false`), admins will need to set the limits to the number of major versions (`MajorVersionLimit`), the number of major with minor versions (`MajorWithMinorVersionsLimit`) and the time period the versions are stored (`ExpireVersionsAfterDays`). Please check the description of `EnableAutoExpirationVersionTrim` for more details.

PARAMVALUE: Int32

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

Specifies the URL of the site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

### Microsoft.Online.SharePoint.PowerShell.SPOListPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOListVersionPolicy](Get-SPOListVersionPolicy.md)
