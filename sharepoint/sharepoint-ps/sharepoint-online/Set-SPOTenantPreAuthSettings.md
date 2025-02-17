---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spotenantpreauthsettings
applicable: SharePoint Online
title: Set-SPOTenantPreAuthSettings
schema: 2.0.0
author: lw-msft
ms.author: laurenwong
ms.reviewer:
manager: bhaveshd
---

# Set-SPOTenantPreAuthSettings

## SYNOPSIS

Sets the pre auth settings for the tenant. 

**What is pre auth?**

SharePoint includes self-issued tokens into URLs called pre auth URLs or temp auth URLs to provide temporary access to a SharePoint resource, which helps support more rich user experiences. For example, a common scenario is downloading a file using a pre auth URL that includes the token in the `tempauth` query parameter like so:

`https://<tenant>.sharepoint.com/sites/samplesite/_layouts/15/download.aspx?UniqueId=<id>&tempauth=v1.ey...`

However, pre auth is currently being deprecated. So this command lets you control whether you want to disable the use of pre auth overall and define any special cases to allow or deny the use of pre auth in based on app id and feature. 

## SYNTAX

```powershell
Set-SPOTenantPreAuthSettings -IsDisabled <bool> [<CommonParameters>]
```

```powershell
Set-SPOTenantPreAuthSettings
  -Add
  -Type {Allow | Deny}
  [-IncludedApps <string>]
  [-ExcludedApps <string>]
  [-IncludedFeatures <string>]
  [-ExcludedFeatures <string>]
  [<CommonParameters>]
```

```powershell
Set-SPOTenantPreAuthSettings
  -Remove
  -Type {Allow | Deny}
  [-IncludedApps <string>]
  [-ExcludedApps <string>]
  [-IncludedFeatures <string>]
  [-ExcludedFeatures <string>]
  [<CommonParameters>]
```

## DESCRIPTION

Sets the pre auth settings for the tenant.

> [!NOTE]
> The precedence for the 3 main settings is as follows:
> 1. Deny
> 2. Allow
> 3. IsDisabled

> [!NOTE]
> The -IncludedApps and -IncludedFeatures parameters alone should be enough for simpler configurations. However, there are some cases (like example 3) where the -ExcludedApps and -ExcludedFeatures parameters are useful to define exactly which apps are allowed/denied from using pre auth.

## EXAMPLES

### Example 1
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled $true

Set-SPOTenantPreAuthSettings -Add -Type Allow -IncludedApps "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111"
```
This example disables pre auth for the tenant overall and adds a setting that allows two apps continue using pre auth for all features, while the rest of the apps and features are denied from using pre auth.

> [!NOTE]
> This example relies on the default values for the `-ExcludedApps`, `-IncludedFeatures`, or `-ExcludedFeatures` parameters. The following would be an equivalent command, where empty quotes for -ExcludedApps mean that the rest of the apps are excluded from the setting and empty quotes for both -IncludedFeatures and -ExcludedFeatures mean that all features are included for the setting.
>  ```
> Set-SPOTenantPreAuthSettings -Add -Type Allow -IncludedApps "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111" -ExcludedApps "" -IncludedFeatures "" -ExcludedFeatures ""
>  ```

### Example 2
```powershell
Set-SPOTenantPreAuthSettings -Remove -Type Allow -IncludedApps "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111"
```
This example removes an existing setting from the allow list.

### Example 3
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled $true

Set-SPOTenantPreAuthSettings -Add -Type Allow -ExcludedApps "00000000-0000-0000-0000-000000000000" -ExcludedFeatures "Download,Embed"
```
This example disables pre auth for the tenant overall and allows all apps apart from 1 to continue using pre auth for all features except for Download and Embed. 

In this case, the app with id 00000000-0000-0000-0000-000000000000 will not be allowed to use pre auth for any feature because it is not an included app for the setting. Therefore, we will default to the IsDisabled setting, which disables the use of preAuth overall. Any other app will be allowed to use pre auth for all features except for Download and Embed.

### Example 4
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled $true

Set-SPOTenantPreAuthSettings -Add -Type Allow -IncludedApps "00000000-0000-0000-0000-000000000000" -IncludedFeatures "WAC,Embed,Download"

Set-SPOTenantPreAuthSettings -Add -Type Deny -IncludedApps "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111"
```
This example disables pre auth for the tenant overall, but it has overlapping settings between the allow and deny lists. The allow list setting tries to allow the app with id 00000000-0000-0000-0000-000000000000 to use pre auth for WAC, Embed, and Download features. But the deny list setting denies the same app from using pre auth for all features.

In this case, the app with id 00000000-0000-0000-0000-000000000000 will be denied from using pre auth for any feature (including all the allow-listed features) because the deny list takes precedence over the allow list. Any other app will be denied from using pre auth for any feature. 

## PARAMETERS

### -IsDisabled

Indicates whether pre auth is disabled for the tenant.

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: IsDisabled
Applicable: SharePoint Online
Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Add

Add a new setting to the allow list or deny list.

```yaml
Type: SwitchParameter
Parameter Sets: AddListItem
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Remove

Remove a setting from the allow list or deny list.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveListItem
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type

Indicates whether to update the allow list or deny list.

PARAMVALUE: Allow | Deny

```yaml
Type: ListType
Parameter Sets: AddListItem, RemoveListItem
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludedApps

String containing a comma-separated list of app ids that are included for the allow list or deny list setting.

Possible Values:
- `""`: Default. If both the -IncludedApps and -ExcludedApps parameters are empty strings, the allow or deny list setting will apply to all apps.
- A comma-separated list of app ids (e.g. `"00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111"`): The allow or deny list setting will apply to only the apps in the list and all other apps will be excluded from the setting.

```yaml
Type: String
Parameter Sets: AddListItem, RemoveListItem
Applicable: SharePoint Online
Required: False
Position: Named
Default value: ""
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedApps

String containing a comma-separated list of app ids that are excluded for the allow list or deny list setting.

Possible Values:
- `""`: Default. If both the -IncludedApps and -ExcludedApps parameters are empty strings, the allow or deny list setting will apply to all apps.
- A comma-separated list of app ids (e.g. `"00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111"`): The allow or deny list setting will not apply to the apps in the list and all other apps will be included for this setting.

```yaml
Type: String
Parameter Sets: AddListItem, RemoveListItem
Applicable: SharePoint Online
Required: False
Position: Named
Default value: ""
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludedFeatures

String containing a comma-separated list of features included for the allow list or deny list setting.

Possible Values:
- `""`: Default. If both the -IncludedFeatures and -ExcludedFeatures parameters are empty string, the allow or deny list setting will apply to all features.
- A comma-separated list of features (e.g. `"Whiteboard,Download,WAC"`): The allow or deny list setting will apply to only the features in the list (see the list below for all available features) and all other features will be excluded from the setting.

Features:
- "Whiteboard"
- "S2S"
- "Exception"
- "Download"
- "WebRendering"
- "WebRenderingEmbed"
- "WebRenderingPreview"
- "NonPreAuth"
- "LegacyProofToken"
- "SharePointDataConnector"
- "DataFormWebpart"
- "Esign"
- "SharePointConnector"
- "WAC"
- "Video"
- "Sharing"
- "CDN"
- "Loop"
- "SearchPreview"
- "SyncClient"
- "Monitoring"
- "Stream"
- "MoveCopyJob"
- "PreAuthUrls"
- "UploadSession"
- "Transform"
- "Thumbnail"
- "Embed"
- "VroomContent"
- "S2SPAC"
- "PAC"
- "VideoPlayback"
- "AudioTrackUpload"


```yaml
Type: String
Parameter Sets: AddListItem, RemoveListItem
Applicable: SharePoint Online
Required: False
Position: Named
Default value: ""
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedFeatures

String containing a comma-separated list of features excluded for the allow list or deny list setting.

Possible Values:
- `""`: Default. If both the -IncludedFeatures and -ExcludedFeatures parameters are empty string, the allow or deny list setting will apply to all features.
- A comma-separated list of features (e.g. `"Whiteboard,Download,WAC"`): The allow or deny list setting will not apply to the features in the list (see the list above for all available features) and all other features will be included for the setting.

```yaml
Type: String
Parameter Sets: AddListItem, RemoveListItem
Applicable: SharePoint Online
Required: False
Position: Named
Default value: ""
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Get-SPOTenantPreAuthSettings](Get-SPOTenantPreAuthSettings.md)
