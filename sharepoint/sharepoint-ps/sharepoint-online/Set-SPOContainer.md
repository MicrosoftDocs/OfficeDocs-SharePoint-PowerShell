---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Set-SPOContainer
Applicable: SharePoint Embedded
title: Set-SPOContainer
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Set-SPOContainer

## SYNOPSIS

Sets or updates one or more property values for a container in SharePoint Embedded.

## SYNTAX

### ParamSet1

```powershell
Set-SPOContainer [-Identity] <SPOContainerPipeBind> [-BlockDownloadPolicy <Boolean>]
 [-ExcludeBlockDownloadPolicyContainerOwners <Boolean>] [-ReadOnlyForBlockDownloadPolicy <Boolean>] [<CommonParameters>]
```

### ParamSet2

```powershell
Set-SPOContainer [-Identity] <SPOContainerPipeBind> [-ConditionalAccessPolicy <SPOConditionalAccessPolicyType>]
 [-LimitedAccessFileType <SPOLimitedAccessFileType>] [-AllowEditing <Boolean>]
 [-ReadOnlyForUnmanagedDevices <Boolean>] [-AuthenticationContextName <String>] [<CommonParameters>]
```

### ParamSet3

```powershell
Set-SPOContainer [-Identity] <SPOContainerPipeBind> [[-SensitivityLabel] <String>] [<CommonParameters>]
```


### ParamSet4

```powershell
Set-SPOContainer [-Identity] <SPOContainerPipeBind> [-RemoveLabel] [<CommonParameters>]
```

### ParamSet5

```powershell
Set-SPOContainer [-Identity] <SPOContainerPipeBind>
 [-SharingDomainRestrictionMode <SharingDomainRestrictionModes>] [-SharingAllowedDomainList <String>]
 [-SharingBlockedDomainList <String>] [<CommonParameters>]
```

## DESCRIPTION

For any parameters that are passed in, the `Set-SPOContainer` cmdlet sets or updates the setting for the active container identified by the parameter `Identity`. The cmdlet throws an error if the identity of an archived container is provided. 

You must be a SharePoint Embedded Administrator to run the cmdlet.


For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the online documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).

## EXAMPLES

### Example 1

```powershell
Set-SPOContainer -Identity https://contoso.sharepoint.com/contentstorage/CSP_33a63968-abae-49a3-a255-f83d0ab2260a/ -BlockDownloadPolicy $true
```

Example 1 sets the Block Download policy on the Container mentioned in the Identity parameter. 

### Example 2

```powershell
Set-SPOContainer -Identity https://contoso.sharepoint.com/contentstorage/CSP_33a63968-abae-49a3-a255-f83d0ab2260a/ -ConditionalAccessPolicy AllowLimitedAccess 
```

In this example, limited access is provided to content residing in the container.

### Example 3

```powershell
Set-SPOContainer -Identity https://contoso.sharepoint.com/contentstorage/CSP_33a63968-abae-49a3-a255-f83d0ab2260a/ -SensitivityLabel ab310e93-9f19-43f2-bc19-bf3386dc0956
```
This example sets a sensitivity label on the container.

### Example 4
```powershell
Set-SPOContainer -Identity https://contoso.sharepoint.com/contentstorage/CSP_33a63968-abae-49a3-a255-f83d0ab2260a/ -RemoveLabel
```
This example removes any previously set sensitivity label on the container.

## PARAMETERS

### -Identity

Use this parameter to specify the container url.

```yaml
Type: String
Applicable: SharePoint Embedded
Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowEditing

Prevents users from editing Office files in the browser and copying and pasting Office file contents out of the browser window.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ConditionalAccess
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationContextName

The conditional access authentication context name.

```yaml
Type: String
Parameter Sets: ConditionalAccess
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### -BlockDownloadPolicy
As a SharePoint Embedded Administrator, you can block the download of files from SharePoint Embedded containers. This feature does not need Microsoft Entra Conditional Access policies. This feature can be set for individual containers but not at the organization level.

Blocking the download of files allows users to remain productive while addressing the risk of accidental data loss. Users have browser-only access with no ability to download, print, or sync files. They also won't be able to access content through apps, including the Microsoft Office desktop apps. When web access is limited, users will see the following message at the top of containers: "Your organization doesn't allow you to download, print, or sync from this Container. For help contact your IT department." Read the full documentation for advanced capabilities at [Block download policy for SharePoint Containers and OneDrive](/sharepoint/block-download-from-sites).

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Embedded
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionalAccessPolicy
Read the [Control access from unmanaged devices](/sharepoint/control-access-from-unmanaged-devices) documentation to understand Conditional Access Policy usage in SharePoint Embedded container.

Possible values:
- AllowFullAccess: Allows full access from desktop apps, mobile apps, and the web.
- AllowLimitedAccess: Allows limited, web-only access.
- BlockAccess: Blocks access.

```yaml
Type: SPOConditionalAccessPolicyType
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Embedded
Required: False
Position: Named
Default value: AllowFullAccess
Accept pipeline input: False
Accept wildcard characters: False
```

### -SensitivityLabel
Specifies the unique identifier (GUID) of the SensitivityLabel.

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Embedded
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLabel
This parameter allows you to remove the assigned sensitivity label on a container.

```yaml
Type: SwitchParameter
Parameter Sets: ParamSet5
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeBlockDownloadPolicyContainerOwners
Controls if container owners are excluded from block download policy.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: BlockDownloadPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitedAccessFileType
The following parameters can be used with -ConditionalAccessPolicy AllowLimitedAccess for both the organization-wide setting and the container-level setting.

OfficeOnlineFilesOnly: Allows users to preview only Office files in the browser. This option increases security but may be a barrier to user productivity.

LimitedAccessFileType WebPreviewableFiles (default): Allows users to preview Office files and other file types (such as PDF files and images) in the browser. Note that the contents of file types other than Office files are handled in the browser. This option optimizes for user productivity but offers less security for files that aren't Office files.

LimitedAccessFileType OtherFiles: Allows users to download files that can't be previewed, such as .zip and .exe. This option offers less security.

```yaml
Type: SPOLimitedAccessFileType
Parameter Sets: ConditionalAccess
Aliases:
Accepted values: OfficeOnlineFilesOnly, WebPreviewableFiles, OtherFiles

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReadOnlyForBlockDownloadPolicy
Controls if read-only should be enabled for block download policy.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: BlockDownloadPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReadOnlyForUnmanagedDevices
Controls whether unmanaged devices have read-only access.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ConditionalAccess
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingAllowedDomainList
Specifies a list of email domains that are allowed for sharing with the external collaborators. Use the space character as the delimiter for entering multiple values. For example, "contoso.com fabrikam.com".

```yaml
Type: String
Parameter Sets: AllowDenyDomain
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingBlockedDomainList
Specifies a list of email domains that are blocked or prohibited for sharing with the external collaborators. Use space character as the delimiter for entering multiple values. For example, "contoso.com fabrikam.com".

```yaml
Type: String
Parameter Sets: AllowDenyDomain
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingDomainRestrictionMode
Specifies the sharing mode for external domains.

Possible values are:

None - Do not restrict sharing by domain
AllowList - Sharing is allowed only with external users that have account on domains specified with -SharingAllowedDomainList
BlockList - Sharing is allowed with external users in all domains except in domains specified with -SharingBlockedDomainList

```yaml
Type: SharingDomainRestrictionModes
Parameter Sets: AllowDenyDomain
Aliases:
Accepted values: None, AllowList, BlockList

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### CommonParameters
This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).




## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Set-SPOTenant](./set-spotenant.md)

[Get-SPOContainer](./Get-SPOContainer.md)
