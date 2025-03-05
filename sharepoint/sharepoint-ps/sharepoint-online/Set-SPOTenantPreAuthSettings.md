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

Sets the configuration of pre-authentication.

## SYNTAX

### IsDisabled
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled <Boolean> [<CommonParameters>]
```

### AddListItem
```powershell
Set-SPOTenantPreAuthSettings [-Add] -Type <TenantPreAuthSettingsListType> [-IncludedApps <String>]
 [-ExcludedApps <String>] [-IncludedFeatures <String>] [-ExcludedFeatures <String>] [<CommonParameters>]
```

### RemoveListItem
```powershell
Set-SPOTenantPreAuthSettings [-Remove] -Id <String> [<CommonParameters>]
```

## DESCRIPTION

You can use this cmdlet to configure or disable the pre-authentication feature within SharePoint Online. The disablement can be combined with switches to support granular pre-authentication management for specific apps and features at the tenant level.  

> [!NOTE]
> **What is pre-authentication?**
>
> SharePoint includes self-issued tokens in URLs called pre-authentication URLs (also known as tempauth URLs) to provide temporary access to a SharePoint resource, which helps support more rich user experiences. For example, a common scenario is downloading a file using a URL that includes a token in the `tempauth` query parameter like the following:
>
> `https://<tenant>.sharepoint.com/sites/samplesite/_layouts/15/download.aspx?UniqueId=<id>&tempauth=v1.ey...`
>
> But this feature is currently being deprecated, so this cmdlet lets you control the use of pre-authentication in various use cases.

> [!IMPORTANT]
> The settings leverage an order of precedence: 
> 1. Deny
> 2. Allow
> 3. IsDisabled
>
> Additionally, as the use of this cmdlet can disable functionality in your SharePoint Online tenant, it is _highly recommended_ to test and evaluate each change in a test tenant ahead of making changes in a production environment. 

You must be a SharePoint Administrator to run the cmdlet. 

## EXAMPLES

### Example 1
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled $true 

Set-SPOTenantPreAuthSettings -Add -Type Allow -IncludedApps "029e7c27-4b9c-4f8b-ba32-b96249468d42,0ab82eba-96c7-4681-9f75-c18437e20d0e"
```
This example disables pre-authentication overall and adds a setting that allows two apps to use pre-authentication for all features.

### Example 2
```powershell
Set-SPOTenantPreAuthSettings -Add -Type Allow -IncludedApps "029e7c27-4b9c-4f8b-ba32-b96249468d42,0ab82eba-96c7-4681-9f75-c18437e20d0e" -ExcludedApps "" -IncludedFeatures "" -ExcludedFeatures ""
```
This example performs the same function as example 1 except in this case the switches for `-ExcludedApps`, `-IncludedFeatures`, and `-ExcludedFeatures` are added to the cmdlet.

These switches are assumed to take the default value of `""` if not used with the cmdlet and example 2 is used to demonstrate the complete set of switches only. 

### Example 3
```powershell
Set-SPOTenantPreAuthSettings -Remove -Id "368dde6f-c857-4383-a8a7-02a04a294e6d"
```
This example will remove an existing item from the current list of items. The remove switch can remove allow or deny entries from the list.

### Example 4
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled $true 

Set-SPOTenantPreAuthSettings -Add -Type Allow -ExcludedApps "029e7c27-4b9c-4f8b-ba32-b96249468d42" -ExcludedFeatures "Download,WebRenderingEmbed" 
```
This example disables pre-authentication overall and allows all apps apart from one to use pre-authentication for all features except for `"Download"` and `"WebRenderingEmbed"`. 

In this case, the app `"029e7c27-4b9c-4f8b-ba32-b96249468d42"` will always be denied from using pre-authentication since it is excluded from the allow list setting. Any other app will be allowed to use pre-authentication for any feature apart from `"Download"` and `"WebRenderingEmbed"`. 

### Example 5
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled $true

Set-SPOTenantPreAuthSettings -Add -Type Allow -IncludedApps "029e7c27-4b9c-4f8b-ba32-b96249468d42" -IncludedFeatures "OfficeOnline,WebRenderingEmbed,Download"

Set-SPOTenantPreAuthSettings -Add -Type Deny -IncludedApps "029e7c27-4b9c-4f8b-ba32-b96249468d42,0ab82eba-96c7-4681-9f75-c18437e20d0e"
```
This example disables pre-authentication overall but contains an overlap between the settings in the Allow list and Deny list. It first allows an app to use pre-authentication for the `"OfficeOnline"`, `"WebRenderingEmbed"`, and `"Download"` features. But in the final execution of the cmdlet, it denies the same app from using pre-authentication for all features. 

In this case, the app `"029e7c27-4b9c-4f8b-ba32-b96249468d42"` would not be allowed to use pre-authentication for any of the allow-listed features despite having the setting. This is because the Deny list takes precedence over the Allow list. 

### Example 6
```powershell
Set-SPOTenantPreAuthSettings -IsDisabled $false

Set-SPOTenantPreAuthSettings -Add -Type Deny -IncludedApps "Empty"
```
This example enables pre-authentication overall and denies requests that are not coming from an app (e.g. requests coming via a browser) from using pre-authentication for all features. 

> [!NOTE]
> The `"Empty"` value for `-IncludedApps` or `-ExcludedApps` is different from an empty string `""`. The rules are as follows:
> - `"Empty"` represents any requests that are not coming from an app (e.g. direct requests from the browser) and will not have an app ID associated with it
> - `""` can mean several things:
>   - If you have `–IncludedApps "" -ExcludedApps ""`, it means that the setting applies to all
>   - If you have `–IncludedApps "" -ExcludedApps "029e7c27-4b9c-4f8b-ba32-b96249468d42"`, it means that the setting applies to all apps apart from `"029e7c27-4b9c-4f8b-ba32-b96249468d42"`.
>   - If you have `–IncludedApps "029e7c27-4b9c-4f8b-ba32-b96249468d42" and -ExcludedApps ""`, it means that the setting only applies to the app `"029e7c27-4b9c-4f8b-ba32-b96249468d42"`
>   - You cannot have a setting with `–IncludedApps "029e7c27-4b9c-4f8b-ba32-b96249468d42" –ExcludedApps "029e7c27-4b9c-4f8b-ba32-b96249468d42"`

## PARAMETERS

### -Add

This parameter specifies that the operation of the cmdlet is to Add a setting to the allow list or deny list.

```yaml
Type: SwitchParameter
Parameter Sets: AddListItem
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedApps

This parameter value contains the apps ids to configure within the `-ExcludedApps` scope. Possible values include: `""`, `"Empty"`, or a comma-separated list of app IDs.

```yaml
Type: String
Parameter Sets: AddListItem
Aliases:

Required: False
Position: Named
Default value: ""
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedFeatures

This parameter value contains the feature names to configure within the `-ExcludedFeatures` scope. Possible values include: `""` or a comma-separated list of feature names (see NOTES section below).

```yaml
Type: String
Parameter Sets: AddListItem
Aliases:

Required: False
Position: Named
Default value: ""
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id

This parameter identifies the list item setting to remove from the current configuration. It is only required with the `-Remove` parameter.

```yaml
Type: String
Parameter Sets: RemoveListItem
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludedApps

This parameter value contains the app ids to configure within the `-IncludedApps` scope. Possible values include: `""`, `"Empty"`, or a comma-separated list of app IDs.

```yaml
Type: String
Parameter Sets: AddListItem
Aliases:

Required: False
Position: Named
Default value: ""
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludedFeatures

This parameter value contains the feature names to configure within the `-IncludedFeatures` scope. Possible values include: `""` or a comma-separated list of feature names (see NOTES section below).

```yaml
Type: String
Parameter Sets: AddListItem
Aliases:

Required: False
Position: Named
Default value: ""
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsDisabled

This parameter allows the administrator to toggle pre-authentication for all apps and features to be either enabled or disabled.

```yaml
Type: Boolean
Parameter Sets: IsDisabled
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Remove

This parameter specifies that the operation of the cmdlet is to Remove a setting from the allow list or deny list.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveListItem
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type

This parameter indicates whether the cmdlet is interacting with the allow list or the deny list. 

```yaml
Type: TenantPreAuthSettingsListType
Parameter Sets: AddListItem
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-5.1).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

The `-IncludedFeatures` and `-ExcludedFeatures` use feature names from the following table. It explicitly mentions if the feature will be broken if it is disabled via the PowerShell cmdlet.

| Feature name         | Description                                                              | Additional Information                                                                                     |
|----------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| DataFormWebpart      | Scenarios involved with DataFormWebParts to display/interact with SharePoint data. | [DataFormWebPart Properties (Microsoft.SharePoint.WebPartPages) - Microsoft Learn ](/previous-versions/office/developer/sharepoint-2010/ms369119(v=office.14)) |
| Download             | Scenarios for getting pre-authenticated download URLs. 3rd party application and some 1st party applications may be broken. | [OAuth 2.0 and OpenID Connect protocols on the Microsoft identity platform - Microsoft Learn ](/entra/identity-platform/v2-protocols) |
| OfficeOnline         | Office on the web scenarios. Performance might be impacted.              |                                                                                                            |
| SearchPreview        | Scenarios involved in generating previews/thumbnails/conversions for search query results. Experience might be broken. |                                                              |
| SharePointConnector  | Scenarios involved with SharePoint Connectors            | [SharePoint Connectors - Microsoft Learn](/connectors/sharepointonline/)                     |
| Thumbnail            | Scenarios for getting pre-authenticated thumbnail generation URLs.       |                                                                                                            |
| UploadSession        | Scenarios for creating upload sessions. 3rd party application and some 1st party applications may be broken |                                                                         |
| Video                | Playing Video hosted on SharePoint might be broken                       |                                                                                                            |
| WebRendering         | Scenarios for rendering previews of files in browser.                    |                                                                                                            |
| WebRenderingEmbed    | Embed SharePoint files in another application. 3rd party application and some 1st party applications may be broken | [Embed Web Part](https://support.microsoft.com/office/add-content-to-your-page-using-the-embed-web-part-721f3b2f-437f-45ef-ac4e-df29dba74de8) |
| Whiteboard           | Teams integration with Whiteboard app will be broken for anonymous and guest users. | [Use Whiteboard in a Teams meeting - Microsoft Support](https://support.microsoft.com/office/use-whiteboard-in-a-teams-meeting-26f87802-b37f-4af0-806d-af79fbfb8ae6) |

## RELATED LINKS

- [Get-SPOTenantPreAuthSettings](Get-SPOTenantPreAuthSettings.md)
- [Clear-SPOTenantPreAuthSettings](Clear-SPOTenantPreAuthSettings.md)
