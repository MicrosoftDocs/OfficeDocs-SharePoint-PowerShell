---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spotenanttempauthsettings
applicable: SharePoint Online
title: Set-SPOTenantTempAuthSettings
schema: 2.0.0
author: lw-msft
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
Set-SPOTenantTempAuthSettings -Add -Type {Allow | Deny} [-AppIds <string>] [-Features <string>] [<CommonParameters>]
```

```powershell
Set-SPOTenantTempAuthSettings -Remove -Type {Allow | Deny} -AppIds <string> -Features <string> [<CommonParameters>]
```

## DESCRIPTION

Sets the temp auth settings for the tenant.

## EXAMPLES

### Example 1
```powershell
Set-SPOTenantTempAuthSettings -IsDisabled $true

Set-SPOTenantTempAuthSettings -Add -Type Allow -AppIds "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111" -Features "All"
```
This example disables temp auth for the tenant overall, and adds 2 apps to the allow list so that both apps can continue using tempAuth for all features.

### Example 2
```powershell
Set-SPOTenantTempAuthSettings -Remove -Type Allow -AppIds "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111" -Features "All"
```
This example removes an existing setting from the allow list.

### Example 3
```powershell
Set-SPOTenantTempAuthSettings -IsDisabled $true

Set-SPOTenantTempAuthSettings -Add -Type Allow -AppIds "00000000-0000-0000-0000-000000000000" -Features "Download"

Set-SPOTenantTempAuthSettings -Add -Type Deny -AppIds "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111" -Features "All"
```
This example disables temp auth for the tenant overall, allows app id 00000000-0000-0000-0000-000000000000 to continue using temp auth for the Download feature, and denies apps with ids 00000000-0000-0000-0000-000000000000 and 11111111-1111-1111-1111-111111111111 from using temp auth for all features.

In this case, the app with id 00000000-0000-0000-0000-000000000000 will not be allowed to use temp auth for the Download feature even though we have already allow listed the app to use the feature. This is because there is also a setting that explicitly denies the same app from using temp auth for all features in the deny list, which takes precedence over the allow list.

> [!NOTE]
> The precedence for the settings is as follows:
> 1. DenyList 
> 2. AllowList
> 3. IsDisabled

### Example 4
```powershell
Set-SPOTenantTempAuthSettings -IsDisabled $true

Set-SPOTenantTempAuthSettings -Add -Type Allow -AppIds "None" -Features "Download,Embed"

Set-SPOTenantTempAuthSettings -Add -Type Allow -AppIds "11111111-1111-1111-1111-111111111111" -Features "All"
```
This example disables temp auth for the tenant overall, but it has overlapping settings in the allow list. The first setting says that none of the apps are allowed to use temp auth for the Download and Embed features. The second setting says that the app with id 11111111-1111-1111-1111-111111111111 is allowed to use tempAuth for all features. 

In this case, temp auth will still be allowed in the Download and Embed features for the app with id 11111111-1111-1111-1111-111111111111 because the second allow list setting takes precedence over the first allow list setting.

> [!NOTE]
> If there are overlapping settings within the same AllowList or DenyList, the last setting that comes in the list takes precedence.

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

Possible Values:
- "All": Default. The allow or deny list setting will apply to all apps.
- A comma-separated list of app ids (e.g. "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111"): The allow or deny list setting will apply to only the apps in the list.
- "None": The allow or deny list setting will apply to none of the apps.

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Features

String containing a comma-separated list of features for the allow list or deny list setting.

Possible Values:
- "All": Default. The allow or deny list setting will apply to all features.
- A comma-separated list of feature names (e.g. "Whiteboard,Download,WAC"): The allow or deny list setting will apply to only the features in the list. See the list below for all available features.

Feature Names:
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
- "S2S-PAC"
- "PAC"
- "VideoPlayback"
- "AudioTrackUpload"


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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Get-SPOTenantTempAuthSettings](Get-SPOTenantTempAuthSettings.md)
