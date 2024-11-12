---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spotenanttempauthsettings
applicable: SharePoint Online
title: Set-SPOTenantTempAuthSettings
schema: 2.0.0
author: laurenwong
ms.author: laurenwong
ms.reviewer:
manager: bhaveshd
---

# Set-SPOTenantTempAuthSettings

## SYNOPSIS

Sets the temp auth settings for the tenant.

## SYNTAX

```powershell
Set-SPOTenantTempAuthSettings -IsDisabled <bool>  [<CommonParameters>]
```

```powershell
Set-SPOTenantTempAuthSettings -Add -Type {Allow | Deny} [-AppIds <string>] [-Features <string>]
[<CommonParameters>]
```

```powershell
Set-SPOTenantTempAuthSettings -Remove -Type {Allow | Deny} -AppIds <string> -Features <string>
[<CommonParameters>]
```

## DESCRIPTION

Sets the temp auth settings for the tenant.

## EXAMPLES

### Example 1
```powershell
Set-SPOTenantTempAuthSettings -IsDisabled $true
```
Example 1 sets disables temp auth for the tenant.

## PARAMETERS

### -IsDisabled

Indicates whether temp auth is disabled for the tenant.

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: IsDisabled
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
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

### -AppIds

String containing a comma-separated list of app ids for the allow list or deny list setting.

POSSIBLE VALUES:
| Value | Description |
|------|------|
| "All" | Default. The allow or deny list setting will apply to all apps. |
| "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111" | The allow or deny list setting will apply to only the apps in the list. |
| "None" | The allow or deny list setting will apply to none of the apps. |

```yaml
Type: String
Parameter Sets: AddListItem
Applicable: SharePoint Online
Required: False
Position: Named
Default value: "All"
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveListItem
Applicable: SharePoint Online
Required: True
Position: Named
Default value: "All"
Accept pipeline input: False
Accept wildcard characters: False
```

### -Features

String containing a comma-separated list of features for the allow list or deny list setting.

POSSIBLE VALUES:
| Value | Description |
|------|------|
| "All" | Default. The allow or deny list setting will apply to all features. |
| "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111" | The allow or deny list setting will apply to only the features in the list. See below for a list of available features. |

| Feature Name          |
|-----------------------|
| "Whiteboard"          |
| "S2S"                 |
| "Exception"           |
| "Download"            |
| "WebRendering"        |
| "WebRenderingEmbed"   |
| "WebRenderingPreview" |
| "NonPreAuth"          |
| "LegacyProofToken"    |
| "SharePointDataConnector" |
| "DataFormWebpart"     |
| "Esign"               |
| "SharePointConnector" |
| "WAC"                 |
| "Video"               |
| "Sharing"             |
| "CDN"                 |
| "Loop"                |
| "SearchPreview"       |
| "SyncClient"          |
| "Monitoring"          |
| "Stream"              |
| "MoveCopyJob"         |
| "PreAuthUrls"         |
| "UploadSession"       |
| "Transform"           |
| "Thumbnail"           |
| "Embed"               |
| "VroomContent"        |
| "S2S-PAC"             |
| "PAC"                 |
| "VideoPlayback"       |
| "AudioTrackUpload"    |


```yaml
Type: String
Parameter Sets: AddListItem
Applicable: SharePoint Online
Required: False
Position: Named
Default value: "All"
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveListItem
Applicable: SharePoint Online
Required: True
Position: Named
Default value: "All"
Accept pipeline input: False
Accept wildcard characters: False
```

## RELATED LINKS

[Get-SPOTenantTempAuthSettings](Get-SPOTenantTempAuthSettings.md)
