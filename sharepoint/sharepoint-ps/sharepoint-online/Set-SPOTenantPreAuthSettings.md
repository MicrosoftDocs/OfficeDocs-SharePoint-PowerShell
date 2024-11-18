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

SharePoint embeds self-issued tokens into some URLs called pre auth URLs or temp auth URLs to provide temporary access to a SharePoint resource, which helps support more rich user experiences. For example, a common scenario is downloading a file using a pre auth URL that includes the token in the `tempauth` query parameter like so: `https://<tenant>.sharepoint.com/sites/samplesite/_layouts/15/download.aspx?UniqueId=<id>&tempauth=v1.ey...`.

However, pre auth is currently being deprecated. So this command lets you control whether you want to disable the use of pre auth overall and define special cases to allow or deny the use of pre auth in based on app id and feature. 

## SYNTAX

```powershell
Set-SPOTenantPreAuthSettings -IsDisabled <bool> [<CommonParameters>]
```

```powershell
Set-SPOTenantPreAuthSettings -Add -Type {Allow | Deny} [-AppIds <string>] [-Features <string>] [<CommonParameters>]
```

```powershell
Set-SPOTenantPreAuthSettings -Remove -Type {Allow | Deny} -AppIds <string> -Features <string> [<CommonParameters>]
```

## DESCRIPTION

Sets the pre auth settings for the tenant.

> [!NOTE]
> The precedence for the 3 main settings is as follows:
> 1. Deny
> 2. Allow
> 3. IsDisabled

> [!NOTE]
> If there are any overlapping settings (meaning that they apply to the same app id and feature) within the Allow or Deny list, the last setting that comes in the list wins and essentially overwrites the previous settings.

## EXAMPLES

### Example 1
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled $true

Set-SPOTenantPreAuthSettings -Add -Type Allow -AppIds "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111" -Features "All"
```
This example disables pre auth for the tenant overall and adds 2 apps to the allow list so that both can continue using pre auth for all features, while the rest of the apps and features are denied from using pre auth.

### Example 2
```powershell
Set-SPOTenantPreAuthSettings -Remove -Type Allow -AppIds "00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111" -Features "All"
```
This example removes an existing setting from the allow list.

### Example 3
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled $true

Set-SPOTenantPreAuthSettings -Add -Type Allow -AppIds "00000000-0000-0000-0000-000000000000" -Features "All"

Set-SPOTenantPreAuthSettings -Add -Type Deny -AppIds "00000000-0000-0000-0000-000000000000" -Features "Download,Embed"
```
This example disables pre auth for the tenant overall and allows app id 00000000-0000-0000-0000-000000000000 to continue using pre auth for all features apart from the Download and Embed features.

In this case, the app with id 00000000-0000-0000-0000-000000000000 will not be allowed to use pre auth for the Download and Embed features, but it can use pre auth for all other features. This happens because the deny list takes precedence over the allow list, so for any overlapping settings between the two lists, the deny list will win (see the first note in the description).

### Example 4
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled $true

Set-SPOTenantPreAuthSettings -Add -Type Allow -AppIds "None" -Features "Download,Embed"

Set-SPOTenantPreAuthSettings -Add -Type Allow -AppIds "11111111-1111-1111-1111-111111111111" -Features "All"
```
This example disables pre auth for the tenant overall, but it has overlapping settings in the allow list. The first setting says that none of the apps are allowed to use pre auth for the Download and Embed features. The second setting says that the app with id 11111111-1111-1111-1111-111111111111 is allowed to use pre auth for all features. 

In this case, pre auth will be allowed for all features including Download and Embed for the app with id 11111111-1111-1111-1111-111111111111 even though we said that no apps can use preauth for those two features. This happens because the second allow list setting overwrites the first allow list setting (see the second note in the description).

If you swapped the order of the allow list settings, pre auth will no longer be allowed for the Download and Embed features for the app with id 11111111-1111-1111-1111-111111111111. But all other features should still be allowed to continue using pre auth for that app.  

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

### -AppIds

String containing a comma-separated list of app ids for the allow list or deny list setting.

Possible Values:
- `"All"`: Default. The allow or deny list setting will apply to all apps.
- A comma-separated list of app ids (e.g. `"00000000-0000-0000-0000-000000000000,11111111-1111-1111-1111-111111111111"`): The allow or deny list setting will apply to only the apps in the list.
- `"None"`: The allow or deny list setting will apply to none of the apps.

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
- `"All"`: Default. The allow or deny list setting will apply to all features.
- A comma-separated list of feature names (e.g. `"Whiteboard,Download,WAC"`): The allow or deny list setting will apply to only the features in the list (see the list below for all available features).

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

[Get-SPOTenantPreAuthSettings](Get-SPOTenantPreAuthSettings.md)
