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

### SetPolicy
```
Set-SPOListVersionPolicy [-Site] <SpoSitePipeBind> -List <SPOListPipeBind>
 -EnableAutoExpirationVersionTrim <Boolean> [-ExpireVersionsAfterDays <Int32>] [-MajorVersionLimit <Int32>]
 [-MajorWithMinorVersionsLimit <Int32>] [-FileTypes <String[]>] [<CommonParameters>]
```

### RemovePolicy
```
Set-SPOListVersionPolicy [-Site] <SpoSitePipeBind> -List <SPOListPipeBind>
 -RemoveVersionExpirationFileTypeOverride <String[]> [<CommonParameters>]
```

### SyncPolicy
```
Set-SPOListVersionPolicy [-Site] <SpoSitePipeBind> -List <SPOListPipeBind> [-FileTypes <String[]>] [-Sync]
 [-ExcludeDefaultPolicy] [<CommonParameters>]
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

Example 3 sets manual version histroy limits on the document library called "Documents" by limiting the number of versions with no time limits.

### Example 4
```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -EnableAutoExpirationVersionTrim $true -FileTypes @("Video", "Audio")
```
Example 4 sets automatic version history limit override for video and audio file types on the document library called "Documents".

### EXAMPLE 5

```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -MajorWithMinorVersionsLimit 20 -ExpireVersionsAfterDays 30 -FileTypes @("Video", "Audio")
```

Example 5 sets manual version history limit override for video and audio file types on the document library called "Documents" by limiting the number of versions and the time (in days) versions are kept.

### EXAMPLE 6

```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -MajorWithMinorVersionsLimit 20 -ExpireVersionsAfterDays 0 -FileTypes @("Video", "Audio")
```

Example 6 sets manual version history limit override for video and audio file types on the document library called "Documents" by limiting the number of versions with no time limits.

### EXAMPLE 7

```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -Sync
```

Example 7 sets the version history limits (include file type overrides) to that of the tenant or site (if the site this document library is in has broken inheritance for version history limits).

### EXAMPLE 8

```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -Sync -FileTypes @("Video", "Audio")
```

Example 8 sets the default version history limits and overrides for video and audio file types to that of the tenant or site (if the site this document library is in has broken inheritance for version history limits).

### EXAMPLE 9

```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -Sync -FileTypes @()
```

Example 9 sets the default version history limit to that of the tenant or site (if the site this document library is in has broken inheritance for version history limits).

### EXAMPLE 10

```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -Sync -FileTypes @("Video", "Audio") -ExcludeDefaultPolicy
```

Example 10 sets the only the version history limit overrides for video and audio file types to that of the tenant or site (if the site this document library is in has broken inheritance for version history limits).

### EXAMPLE 11


```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -Sync -ExcludeDefaultPolicy
```

Example 10 sets the version history limit overrides for all file types to that of the tenant or site (if the site this document library is in has broken inheritance for version history limits).

### EXAMPLE 12


```powershell
Set-SPOListVersionPolicy -Site https://contoso.sharepoint.com/sites/site1 -List "Documents" -RemoveVersionExpirationFileTypeOverride @("Video", "Audio")
```

Example 12 removes the version history limit overrides for video and audio file types so that they follow the default version history limits.

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
Type: Boolean
Parameter Sets: SetPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeDefaultPolicy
> Applicable: SharePoint Online

Indicates whether to synchronize the default version policy to the default policy of the tenant or the site (if the site this document library is in has broken inheritance for version history limits).

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

```yaml
Type: SwitchParameter
Parameter Sets: SyncPolicy
Aliases:

Required: False
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
Type: Int32
Parameter Sets: SetPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileTypes
> Applicable: SharePoint Online

An array of file type names. The supported file type names are:
- Audio
- OutlookPST
- Video

Apply the version history limits to a set of file types so that they no longer follow the default version history limits. It is used in combination with the following parameters: 
- [EnableAutoExpirationVersionTrim](#-enableautoexpirationversiontrim)
- [MajorVersionLimit](#-majorversionlimit)
- [ExpireVersionsAfterDays](#-expireversionsafterdays)

Or apply the version history limit override for the file types of the tenant or the site (if the site this document library is in has broken inheritance for version history limits) by using the [Sync](#-sync) parameter. For more information about this option, please refer to the documentation for the [Sync](#-sync) parameter.

```yaml
Type: String[]
Parameter Sets: SetPolicy, SyncPolicy
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
Type: Int32
Parameter Sets: SetPolicy
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
Type: Int32
Parameter Sets: SetPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveVersionExpirationFileTypeOverride
An array of file type names. Removes the version history limit override from a set of file types so that they will follow the default version history limits. 

```yaml
Type: String[]
Parameter Sets: RemovePolicy
Aliases:

Required: True
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

### -Sync
Apply the version history limits of the tenant or the site (if the site this document library is in has broken inheritance for version history limits).

You may use the following parameters in combination to update only the default policy or a set of file type overrides:
- [ExcludeDefaultPolicy](#-excludedefaultpolicy): if set, it will not update the default policy.
- [FileTypes](#-filetypes): 
  - if set, it will update the specified file types; 
  - if not set, it will update all file type overrides;
  - if set to an empty array (i.e. `@()`), it will not update any file type overrides.
    
> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

```yaml
Type: SwitchParameter
Parameter Sets: SyncPolicy
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

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

### Microsoft.Online.SharePoint.PowerShell.SPOListPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOListVersionPolicy](Get-SPOListVersionPolicy.md)
