---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# New-SPOSiteManageVersionPolicyJob

## SYNOPSIS
Starts a background job that manages the file versions and version history limits of all of its document libraries.

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

## SYNTAX

### MandatoryTrimOptionalSync
```powershell
New-SPOSiteManageVersionPolicyJob [-Identity] <SpoSitePipeBind> [-FileTypes <String[]>] [-ExcludeDefaultPolicy]
 [-TrimUseListPolicy] [-SyncListPolicy] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MandatorySync
```
New-SPOSiteManageVersionPolicyJob [-Identity] <SpoSitePipeBind> [-FileTypes <String[]>] [-ExcludeDefaultPolicy]
 [-SyncListPolicy] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Starts a background job that does one or more of the following: 

- sets the version history limits of all document libraries to that of the site;

- trims version in all document libraries according to each list's version history limits.

This effect can be applied to default version history limits, or a set of file types. Supported file types are:

- Audio

- OutlookPST

- Video

## EXAMPLES

### Example 1

```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -SyncListPolicy -FileTypes @("Video","Audio") 
```

Apply the site video, audio, and default version history limits to existing document libraries. If the site is not broken inheritance for version history limits, then it applies the tenant version history limits.

### Example 2


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -SyncListPolicy -FileTypes @("Video","Audio") -ExcludeDefaultPolicy
```

Apply the site video, audio version history limits to existing document libraries. If the site is not broken inheritance for version history limits, then it applies the tenant version history limits.

### Example 3


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -SyncListPolicy -FileTypes @()
```

Apply the site default version history limits to existing document libraries. If the site is not broken inheritance for version history limits, then it applies the tenant version history limits.

### Example 4


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -SyncListPolicy
```

Apply the site version history limits (including file type overrides) to existing document libraries. If the site is not broken inheritance for version history limits, then it applies the tenant version history limits.

### Example 5


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -SyncListPolicy -ExcludeDefaultPolicy
```

Apply the site level all file type version history limit overrides to existing document libraries. If the site is not broken inheritance for version history limits, then it applies the tenant version history limits.

### Example 6

```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -TrimUseListPolicy -FileTypes @("Video","Audio") 
```

Trim video and audio file versions, and the file versions that don't have a file type override, based on each document library's version history limits.

### Example 7


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -TrimUseListPolicy -FileTypes @("Video","Audio") -ExcludeDefaultPolicy
```

Trim video and audio file versions based on each document library's version history limits.

### Example 8


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -TrimUseListPolicy -FileTypes @()
```

Trim file versions that don't have a file type override based on each document library's version history limits.

### Example 9


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -TrimUseListPolicy
```

Trim all file versions based on each document library's version history limits.

### Example 10


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -TrimUseListPolicy -ExcludeDefaultPolicy
```

Trim all file versions that have a file type override based on each document library's version history limits.


### Example 11

```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -SyncListPolicy -FileTypes @("Video","Audio") 
```

Apply the site video, audio, and default version history limits to existing document libraries. If the site is not broken inheritance for version history limits, then it applies the tenant version history limits. Then trim video and audio file versions, and the file versions that don't have a file type override, based on each document library's version history limits.

### Example 12


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -SyncListPolicy -TrimUseListPolicy -FileTypes @("Video","Audio") -ExcludeDefaultPolicy
```

Apply the site video, audio version history limits to existing document libraries. If the site is not broken inheritance for version history limits, then it applies the tenant version history limits. Then trim video and audio file versions based on each document library's version history limits.

### Example 13


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -SyncListPolicy -TrimUseListPolicy -FileTypes @()
```

Apply the site default version history limits to existing document libraries. If the site is not broken inheritance for version history limits, then it applies the tenant version history limits. Then trim file versions that don't have a file type override based on each document library's version history limits.

### Example 14


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -SyncListPolicy -TrimUseListPolicy
```

Apply the site version history limits (including file type overrides) to existing document libraries. If the site is not broken inheritance for version history limits, then it applies the tenant version history limits. Then trim all file versions based on each document library's version history limits.

### Example 15


```powershell
New-SPOSiteManageVersionPolicyJob -Identity $siteUrl -SyncListPolicy -TrimUseListPolicy -ExcludeDefaultPolicy
```

Apply the site level all file type version history limit overrides to existing document libraries. If the site is not broken inheritance for version history limits, then it applies the tenant version history limits. Then trim all file versions that have a file type override based on each document library's version history limits.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeDefaultPolicy
Indicates whether to update the default version history limits and/or to trim file versions that don't have an override.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileTypes
An array of file type names. The supported file type names are:

- Audio

- OutlookPST

- Video

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
> Applicable: SharePoint Online

Specifies the URL of the site collection.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SyncListPolicy
Indicates whether to update all of the document libraries' version history limits to that of the site. Or if the site is not broken inheritance for version history limits, then it applies the tenant version history limits.

```yaml
Type: SwitchParameter
Parameter Sets: MandatoryTrimOptionalSync
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: MandatorySync
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrimUseListPolicy
Indicates whether to trim existing versions.

```yaml
Type: SwitchParameter
Parameter Sets: MandatoryTrimOptionalSync
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
[Get-SPOSiteManageVersionPolicyJobProgress](Get-SPOSiteManageVersionPolicyJobProgress.md)
[Remove-SPOSiteManageVersionPolicyJob](Remove-SPOSiteManageVersionPolicyJob.md)