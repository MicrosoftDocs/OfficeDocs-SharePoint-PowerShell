---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-sposite
applicable: SharePoint Online
title: Set-SPOSite
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Set-SPOSite

## SYNOPSIS

Sets or updates one or more properties' values for a site collection.

## SYNTAX

### None (Default)

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ParamSet1

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-Owner <String>] [-Title <String>] [-StorageQuota <Int64>]
 [-StorageQuotaWarningLevel <Int64>] [-ResourceQuota <Double>] [-ResourceQuotaWarningLevel <Double>]
 [-LocaleId <UInt32>] [-AllowSelfServiceUpgrade <Boolean>] [-NoWait] [-LockState <String>]
 [-DenyAddAndCustomizePages <Boolean>] [-SharingCapability <SharingCapabilities>]
 [-ShowPeoplePickerSuggestionsForGuestUsers <Boolean>] [-StorageQuotaReset]
 [-SandboxedCodeActivationCapability <SandboxedCodeActivationCapabilities>]
 [-DisableCompanyWideSharingLinks <CompanyWideSharingLinksPolicy>]
 [-SharingDomainRestrictionMode <SharingDomainRestrictionModes>] [-SharingAllowedDomainList <String>]
 [-SharingBlockedDomainList <String>] [-ConditionalAccessPolicy <SPOConditionalAccessPolicyType>]
 [-AllowDownloadingNonWebViewableFiles <Boolean>] [-LimitedAccessFileType <SPOLimitedAccessFileType>]
 [-AllowEditing <Boolean>] [-ReadOnlyForUnmanagedDevices <Boolean>] [-SensitivityLabel <String>]
 [-DisableAppViews <AppViewsPolicy>] [-DisableFlows <FlowsPolicy>]
 [-MediaTranscription <MediaTranscriptionPolicyType>] [-BlockDownloadPolicy <Boolean>]
 [-ExcludedBlockDownloadGroupIds <Guid[]>] [-ExcludeBlockDownloadPolicySiteOwners <Boolean>]
 [-ReadOnlyForBlockDownloadPolicy <Boolean>] [-ExcludeBlockDownloadSharePointGroups <String[]>]
 [-AuthenticationContextName <String>]
 [-AuthenticationContextAccessType <SPOAuthenticationContextPolicyAccessType>]
 [-RestrictedToGeo <RestrictedToRegion>] [-CommentsOnSitePagesDisabled <Boolean>] [-UpdateUserTypeFromAzureAD]
 [-SocialBarOnSitePagesDisabled <Boolean>] [-HubSiteId <Guid>] [-DefaultSharingLinkType <SharingLinkType>]
 [-DefaultLinkPermission <SharingPermissionType>] [-DefaultLinkToExistingAccess <Boolean>]
 [-DefaultLinkToExistingAccessReset] [-AnonymousLinkExpirationInDays <Int32>]
 [-OverrideTenantAnonymousLinkExpirationPolicy <Boolean>] [-ExternalUserExpirationInDays <Int32>]
 [-OverrideTenantExternalUserExpirationPolicy <Boolean>] [-InformationBarriersMode <String>]
 [-BlockDownloadLinksFileType <BlockDownloadLinksFileTypes>]
 [-OverrideBlockUserInfoVisibility <SiteUserInfoVisibilityPolicyValue>]
 [-LoopDefaultSharingLinkScope <SharingScope>] [-LoopDefaultSharingLinkRole <SharingRole>]
 [-RequestFilesLinkEnabled <Boolean>] [-RequestFilesLinkExpirationInDays <Int32>]
 [-OverrideSharingCapability <Boolean>] [-DefaultShareLinkScope <SharingScope>]
 [-DefaultShareLinkRole <SharingRole>] [-BlockGuestsAsSiteAdmin <SharingState>]
 [-RestrictContentOrgWideSearch <Boolean>] [-RestrictedContentDiscoveryforCopilotAndAgents <Boolean>]
 [-RestrictedAccessControl <Boolean>] [-RestrictedAccessControlGroups <Guid[]>]
 [-ListsShowHeaderAndNavigation <Boolean>] [-HidePeoplePreviewingFiles <Boolean>]
 [-HidePeopleWhoHaveListsOpen <Boolean>] [-AllowFileArchive <Boolean>]
 [-AllowWebPropertyBagUpdateWhenDenyAddAndCustomizePagesIsEnabled <Boolean>]
 [-DisableSiteBranding <Boolean>]
 [-IsAuthoritative <Boolean>]
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ParamSet2

```
Set-SPOSite [-Identity] <SpoSitePipeBind> -EnablePWA <Boolean> [-InformationBarriersMode <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ParamSet3

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-DisableSharingForNonOwners] [-InformationBarriersMode <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ParamSet5

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-RemoveLabel] [-InformationBarriersMode <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AddInformationBarrierSegments

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-AddInformationSegment <Guid[]>] [-InformationBarriersMode <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveInformationBarrierSegments

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-RemoveInformationSegment <Guid[]>]
 [-InformationBarriersMode <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ClearLockDown

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>] [-ClearSharingLockDown] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AddRestrictedAccessControlGroups

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>]
 [-AddRestrictedAccessControlGroups <Guid[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRestrictedAccessControlGroups

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>]
 [-RemoveRestrictedAccessControlGroups <Guid[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ClearRestrictedAccessControl

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>] [-ClearRestrictedAccessControl]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InheritVersionPolicyFromTenant

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>] [-InheritVersionPolicyFromTenant]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSiteFileVersionPolicy

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>]
 [-EnableAutoExpirationVersionTrim <Boolean>] [-ExpireVersionsAfterDays <Int32>] [-MajorVersionLimit <Int32>]
 [-MajorWithMinorVersionsLimit <Int32>] [-ApplyToNewDocumentLibraries] [-ApplyToExistingDocumentLibraries]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSiteFileTypeFileVersionPolicy

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>] [-EnableAutoExpirationVersionTrim <Boolean>] [-ExpireVersionsAfterDays <Int32>] [-MajorVersionLimit <Int32>] -FileTypesForVersionExpiration <String[]> [-ApplyToNewDocumentLibraries] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveSiteFileVersionPolicy

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>] [-ApplyToNewDocumentLibraries]
 -RemoveVersionExpirationFileTypeOverride <String[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ClearGroupId

```
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>] [-ClearGroupId] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

For any parameters that are passed in, the `Set-SPOSite` cmdlet sets or updates the setting for the site collection identified by parameter Identity.

You must be a SharePoint Online administrator and be a site collection administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

For OneDrive for Business site collection, the only valid parameters are Identity, AllowDownloadingNonWebViewableFiles, AllowEditing, ConditionalAccessPolicy, DefaultLinkPermission, DefaultSharingLinkType, DisableCompanyWideSharingLinks, LimitedAccessFileType, LockState, Owner, SharingAllowedDomainList, SharingBlockedDomainList, SharingCapability, SharingDomainRestrictionMode, ShowPeoplePickerSuggestionsForGuestUsers, StorageQuota, and StorageWarningLevel.

For Groups site collection, the only valid parameters are Identity, AllowSelfServiceUpgrade, DefaultLinkPermission, DefaultSharingLinkType, DenyAddAndCustomizePages, DisableCompanyWideSharingLinks, DisableSharingForNonOwners, LockState, Owner, ResourceQuota, ResourceQuotaWarningLevel, SandboxedCodeActivationCapability, SensitivityLabel, SharingCapability, ShowPeoplePickerSuggestionsForGuestUsers, SocialBarOnSitePagesDisabled, StorageQuota, StorageQuotaReset, and StorageQuotaWarningLevel.

## EXAMPLES

### Example 1

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -Owner joe.healy@contoso.com -NoWait
```

Example 1 updates the owner of site collection <https://contoso.sharepoint.com/sites/site1> to the person whose email address is joe.healy@contoso.com. This cmdlet is executed immediately without delay.

### Example 2

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -StorageQuota 1024
```

Example 2 updates the settings of site collection <https://contoso.sharepoint.com/sites/site1.> The storage quota is updated to 1024 megabytes (1 GB).

### Example 3

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com -StorageQuota 1500 -StorageQuotaWarningLevel 1400
```

This example updates the settings of site collection <https://contoso.sharepoint.com.> The storage quota is updated to 1500 megabytes and the storage quota warning level is updated to 1400 megabytes.

### Example 4

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com -DisableSharingForNonOwners
```

Example 4 prevents non-owners of a site from inviting new users to the site.

### Example 5

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/groupname -StorageQuota 3000 -StorageQuotaWarningLevel 2000
```

This example sets the quota for the site.

> [!NOTE]
> If Site Collection Storage Management is enabled for the tenant, you will not be able to set quota and will have a generic error returned. To workaround this issue, set the site collection storage management to "manual" temporarily, set your quotas and then set the site collection storage management setting back to its original setting.

### Example 6

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnablePWA $true
```

Example 6 enables the site "site1" to create Project Web Applications (PWA).

### Example 7

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -SharingCapability ExternalUserSharingOnly
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -SharingDomainRestrictionMode AllowList -SharingAllowedDomainList "contoso.com"
```

Example 7 sets the Sharing Capability to allow external users who accept sharing invitations and sign in as authenticated users, and then specifies an email domain that is allowed for sharing with the external collaborators.

### Example 8

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/research -AddInformationSegment a17efb47-e3c9-4d85-a188-1cd59c83de32
```

This example adds InformationSegment 'a17efb47-e3c9-4d85-a188-1cd59c83de32' to the site.

### Example 9

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/research -RemoveInformationSegment a17efb47-e3c9-4d85-a188-1cd59c83de32
```

In example, InformationSegment 'a17efb47-e3c9-4d85-a188-1cd59c83de32' is removed from the site.

### Example 10

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/research -ConditionalAccessPolicy AuthenticationContext -AuthenticationContextName "MFA"
```

In this example, an authentication context called MFA is attached to the site.

### Example 11

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $true
```

Example 11 sets automatic version history limits at the site level. Automatic setting will be applied to all new document libraries created in the site and a background request will be created to asynchronously process the update on existing document libraries that have versioning enabled.

### EXAMPLE 12

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -MajorWithMinorVersionsLimit 20 -ExpireVersionsAfterDays 30
```

Example 12 sets manual version history limits at the site level by limiting the number of versions and the time (in days) versions are kept. The new document libraries will use this version setting. Also it creates a job to set this manual version setting for existing document libraries that enabled versioning.

### EXAMPLE 13

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -MajorWithMinorVersionsLimit 20 -ExpireVersionsAfterDays 0
```

Example 13 sets manual version history limits at the site level by limiting the number of versions with no time limits. The new document libraries will use this version setting. Also it creates a job to set this manual version setting for existing document libraries that enabled versioning.

### Example 14

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $true -ApplyToNewDocumentLibraries
```

Example 14 sets automatic version history limits at the site level. The new document libraries will use this version setting.

### EXAMPLE 15

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -ExpireVersionsAfterDays 30 -ApplyToNewDocumentLibraries
```

Example 15 sets manual version history limits at the site level by limiting the number of versions and the time (in days) versions are kept. The new document libraries will use this version setting.

### EXAMPLE 16

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -ExpireVersionsAfterDays 0 -ApplyToNewDocumentLibraries
```

Example 16 sets manual version history limits at the site level by limiting the number of versions with no time limits. The new document libraries will use this version setting.

### Example 17

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $true -ApplyToExistingDocumentLibraries
```

Example 17 creates a job to set automatic version history limits for existing document libraries that enabled versioning.

### EXAMPLE 18

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -MajorWithMinorVersionsLimit 20 -ExpireVersionsAfterDays 30 -ApplyToExistingDocumentLibraries
```

Example 18 creates a job to set manual version history limits that limits the number of versions and the time (in days) versions are kept for existing document libraries that enabled versioning.

### EXAMPLE 19

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -MajorWithMinorVersionsLimit 20 -ExpireVersionsAfterDays 0 -ApplyToExistingDocumentLibraries
```

Example 19 creates a request to set manual version history limits that limits the number of versions with no time limits for existing document libraries that enabled versioning.

### EXAMPLE 20

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -InheritVersionPolicyFromTenant
```

Example 20 clears the file version setting at the site level. The new document libraries will use the Tenant Level setting. It won't impact the existing document libraries.

### Example 21


```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $true -FileTypesForVersionExpiration @("Video", "Audio") -ApplyToNewDocumentLibraries
```

Example 21 sets automatic version history limit override for video and audio file types at the site level. The new document libraries will use this version setting.

### Example 22


```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -ExpireVersionsAfterDays 30 
-FileTypesForVersionExpiration @("Video", "Audio") -ApplyToNewDocumentLibraries
```

Example 22 sets manual version history limit override for video and audio file types at the site level by limiting the number of versions and the time (in days) versions are kept. The new document libraries will use this version setting.

### Example 23


```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -ExpireVersionsAfterDays 0 
-FileTypesForVersionExpiration @("Video", "Audio") -ApplyToNewDocumentLibraries
```

Example 23 sets manual version history limit override for video and audio file types at the site level by limiting the number of versions with no time limits. The new document libraries will use this version setting.

### Example 24


```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -RemoveVersionExpirationFileTypeOverride @("Video", "Audio") -ApplyToNewDocumentLibraries
```

Example 24 removes the version history limit override for video and audio file types at the site level. The new document libraries will use this version setting.

## PARAMETERS

### -AddInformationSegment

This parameter allows you to add a segment to a SharePoint site. This parameter is only applicable for tenants who have enabled Microsoft 365 Information barriers capability. Please read https://learn.microsoft.com/sharepoint/information-barriers documentation to understand Information barriers in SharePoint Online.

**Note**: This parameter is available only in SharePoint Online Management Shell Version 16.0.19927.12000 or later.

```yaml
Type: System.Guid[]
Parameter Sets: AddInformationBarrierSegments
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRestrictedAccessControlGroups

> Applicable: SharePoint Online

Specifies the IDs of groups to be added to an access restriction policy and gain access.

```yaml
Type: System.Guid[]
Parameter Sets: AddRestrictedAccessControlGroups
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowDownloadingNonWebViewableFiles

> Applicable: SharePoint Online

Specifies if non web viewable files can be downloaded.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowEditing

> Applicable: SharePoint Online

Prevents users from editing Office files in the browser and copying and pasting Office file contents out of the browser window.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowFileArchive

> Applicable: SharePoint Online

This setting enables or disables the file archive feature for a SharePoint site. If this parameter is passed as true for a site and Microsoft 365 Archive is enabled at the tenant-level, then the site will allow file archive.

PARAMVALUE: False | True

If set to True, the feature will be enable. Feature is disabled by default.

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowSelfServiceUpgrade

> Applicable: SharePoint Online

Determines whether site collection administrators can upgrade their site collections.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowWebPropertyBagUpdateWhenDenyAddAndCustomizePagesIsEnabled

> Applicable: SharePoint Online

Enables or disables web property bag updates. When `AllowWebPropertyBagUpdateWhenDenyAddAndCustomizePagesIsEnabled` is set to `$true`, the web property bag can be updated even if the Add And Customize Pages right is denied on the site collection.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AnonymousLinkExpirationInDays

> Applicable: SharePoint Online

Specifies all anonymous/anyone links that have been created (or will be created) will expire after the set number of days. Only applies if OverrideTenantAnonymousLinkExpirationPolicy is set to true.

The valid number should be between 1 and 730. To remove the expiration requirement, set the value to zero (0).

```yaml
Type: System.Int32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToExistingDocumentLibraries

> Applicable: SharePoint Online

Create a job to apply the version history limits setting to existing document libraries.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSiteFileVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToNewDocumentLibraries

> Applicable: SharePoint Online

Apply the version history limits setting to new document libraries.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSiteFileVersionPolicy, RemoveSiteFileVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: SetSiteFileTypeFileVersionPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationContextAccessType

> Applicable: SharePoint Online

Controls whether Authentication Context Limited Access is enabled for a site.

The valid values are:

- AllowLimitedAccess
- BlockAccess

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SPOAuthenticationContextPolicyAccessType
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationContextName

> Applicable: SharePoint Online

The conditional access authentication context name.

```yaml
Type: System.String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockDownloadLinksFileType

> Applicable: SharePoint Online

The valid values are:

- WebPreviewableFiles
- ServerRenderedFilesOnly

**Note**: ServerRendered (Office Only) and WebPreviewable (All supported files).

The site's value is compared with the tenant level setting and the stricter one wins. For example, if the tenant is set to ServerRenderedFilesOnly then that will be used even if the site is set to WebPreviewableFiles.

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.BlockDownloadLinksFileTypes
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockDownloadPolicy

> Applicable: SharePoint Online

As a SharePoint administrator in Microsoft 365, you can block the download of files from SharePoint sites or OneDrive. This feature does not need Microsoft Entra Conditional Access policies. This feature can be set for individual sites but not at the organization level.

Blocking the download of files allows users to remain productive while addressing the risk of accidental data loss. Users have browser-only access with no ability to download, print, or sync files. They also won't be able to access content through apps, including the Microsoft Office desktop apps. When web access is limited, users will see the following message at the top of sites: "Your organization doesn't allow you to download, print, or sync from this site. For help contact your IT department." Read the full documentation for advanced capabilities at [Block download policy for SharePoint sites and OneDrive](/sharepoint/block-download-from-sites).

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockGuestsAsSiteAdmin

> Applicable: SharePoint Online

Whether to block guests as site admins.

```yaml
Type: Microsoft.SharePoint.Client.SharingState
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearGroupId

This parameter allows you to remove the assigned Microsoft 365 group ID on a site, when the group is permanently deleted.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClearGroupId
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearRestrictedAccessControl

> Applicable: SharePoint Online

Clears the list of groups that are given access via an access restriction policy.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClearRestrictedAccessControl
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearSharingLockDown

> Applicable: SharePoint Online

Whether to clear the sharing lockdown for the site.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClearLockDown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommentsOnSitePagesDisabled

> Applicable: SharePoint Online

Use this parameter to disable Comments section on Site Pages.
The parameter can't be used for Groups Site Collections.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionalAccessPolicy

> Applicable: SharePoint Online

Please read [Control access from unmanaged devices](/sharepoint/control-access-from-unmanaged-devices) documentation here to understand Conditional Access Policy usage in SharePoint Online.

Possible values:

- AllowFullAccess: Allows full access from desktop apps, mobile apps, and the web.
- AllowLimitedAccess: Allows limited, web-only access.
- BlockAccess: Blocks Access.
- AuthenticationContext: Assign a Microsoft Entra authentication context. Must add the AuthenticationContextName. Please read [Configure authentication contexts](/azure/active-directory/conditional-access/concept-conditional-access-cloud-apps#configure-authentication-contexts).

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SPOConditionalAccessPolicyType
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultLinkPermission

> Applicable: SharePoint Online

The default link permission for the site collection. To be replaced by DefaultShareLinkRole.

PARAMVALUE: None | View | Edit

- None - Respect the organization default link permission
- View - Sets the default link permission for the site to "view" permissions
- Edit - Sets the default link permission for the site to "edit" permissions

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingPermissionType
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultLinkToExistingAccess

> Applicable: SharePoint Online

When set to TRUE, the DefaultSharingLinkType will be overriden and the default sharing link will a People with Existing Access link (which does not modify permissions). When set to FALSE (the default), the DefaultSharingLinkType parameter controls the default sharing link type.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultLinkToExistingAccessReset

> Applicable: SharePoint Online

Whether to reset the default link to existing access to the site.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultShareLinkRole

> Applicable: SharePoint Online

The default share link role for the site collection. It replaces `DefaultLinkPermission`.

The valid values are:

- Edit
- None
- RestrictedView
- Review
- View

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingRole
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultShareLinkScope

> Applicable: SharePoint Online

The default share link scope on the site. It replaces `DefaultSharingLinkType`.

The valid values are:

- Anyone
- Organization
- SpecificPeople
- Uninitialized

```yaml
Type: Microsoft.SharePoint.Client.Sharing.SharingScope
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultSharingLinkType

> Applicable: SharePoint Online

The default link type for the site collection. To be replaced by DefaultShareLinkScope.

PARAMVALUE: None | AnonymousAccess | Internal | Direct

- None - Respect the organization default sharing link type
- AnonymousAccess - Sets the default sharing link for this site to an Anonymous Access or Anyone link
- Internal - Sets the default sharing link for this site to the "organization" link or company shareable link
- Direct - Sets the default sharing link for this site to the "Specific people" link

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingLinkType
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DenyAddAndCustomizePages

> Applicable: SharePoint Online

Determines whether the Add And Customize Pages right is denied on the site collection.
For more information about permission levels, see User permissions and permission levels in SharePoint.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAppViews

> Applicable: SharePoint Online

**Note**: This parameter has been retired and no longer functions.

Disables the Power Apps button.
Possible values:

- Disabled
- NotDisabled
- Unknown (not settable)

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.AppViewsPolicy
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableCompanyWideSharingLinks

> Applicable: SharePoint Online

Disables People in your organization links. For more information, see [People in your organization sharing links](/microsoft-365/solutions/microsoft-365-limit-sharing#people-in-your-organization-sharing-links).

Possible values

- Disabled
- NotDisabled
- Unknown (not settable)

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.CompanyWideSharingLinksPolicy
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableFlows

> Applicable: SharePoint Online

**Note**: This parameter has been retired and no longer functions.

Disables the Power Automate button.
Possible values

- Disabled
- NotDisabled

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.FlowsPolicy
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSharingForNonOwners

> Applicable: SharePoint Online

This parameter prevents non-owners from inviting new users to the site.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParamSet3
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSiteBranding

> Applicable: SharePoint Online

Enables or disables site branding. When `DisableSiteBranding` is set to `$true`, the site branding is disabled on the site collection.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsAuthoritative

> Applicable: SharePoint Online

When an admin with a Copilot license marks a site as authoritative, it signals to Microsoft Search, Microsoft 365 Copilot, and other AI agents that the content is official, trusted, and verified. This designation helps improve content discoverability and increases user confidence in AI-generated responses. 

PARAMVALUE: True | False

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoExpirationVersionTrim

> Applicable: SharePoint Online

SharePoint Administrators can set site-level version history limit settings that universally apply to new versions created on all new document libraries created on the site. Also can create request to set the version setting for existing libraries that enabled versioning.

When version history limits are managed automatically, SharePoint employs an algorithm behind the scenes that deletes (thins out) intermittent older versions that are least likely to be needed, while preserving sufficient high-value versions - more versions in the recent past and fewer farther back in time - in case restores are required.

The valid values are:

- True - Version history limits for new versions created on new/existing document libraries in the site will be managed automatically.
- False - Version history limits for new Versions created on new/existing document libraries in the site will be managed manually by setting limits to the number of major versions (`MajorVersionLimit`), number of major with minor versions (`MajorWithMinorVersionsLimit`) and time set (`ExpireVersionsAfterDays`). Review the documentation of both parameters to manage your organization's version limits manually.

> [!NOTE]
> When version history limits are managed manually (`EnableAutoExpirationVersionTrim $false`), `MajorVersionLimit` and `ExpireVersionsAfterDays` are both required parameters, `MajorWithMinorVersionsLimit` is also required for creating request for setting existing document libraries with the following acceptable values:
> a. `MajorVersionLimit` accepts values from 1 through 50,000 (inclusive).
> b. `MajorWithMinorVersionsLimit` accepts values from 0 through 50,000 (inclusive).
> c. `ExpireVersionsAfterDays` accepts values of 0 to Never Expire or values >= 30 to delete versions that exceed that time period.
> When version history limits are managed automatically (`EnableAutoExpirationVersionTrim $true`), setting `MajorVersionLimit` or `ExpireVersionsAfterDays` will result in an error as the count limits are set by the service.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: SetSiteFileVersionPolicy, SetSiteFileTypeFileVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnablePWA

> Applicable: SharePoint Online

Determines whether site can include Project Web App.
For more information about Project Web App, see Plan SharePoint groups in Project Server.

```yaml
Type: System.Boolean
Parameter Sets: ParamSet2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeBlockDownloadPolicySiteOwners

> Applicable: SharePoint Online

Controls if site owners are excluded from block download policy.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeBlockDownloadSharePointGroups

> Applicable: SharePoint Online

Specifies the groups excluded from the block download policy.

```yaml
Type: System.String[]
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedBlockDownloadGroupIds

> Applicable: SharePoint Online

Exempts users from specified groups from the block download policy and they can fully download any content for the site.

```yaml
Type: System.Guid[]
Parameter Sets: ParamSet1
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
Type: System.Int32
Parameter Sets: SetSiteFileVersionPolicy, SetSiteFileTypeFileVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalUserExpirationInDays

> Applicable: SharePoint Online

Specifies all external user expiration which will expire after the set number of days. Only applies if OverrideTenantExternalUserExpirationPolicy is set to true.

The maximum value is 730. To remove the expiration requirement, set the value to zero (0).

```yaml
Type: System.Int32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileTypesForVersionExpiration

> Applicable: SharePoint Online

An array of file type names. The supported file type names are:
- Audio
- OutlookPST
- Video

Apply the version history limits to a set of file types so that they no longer follow the default version history limits. It is used in combination with the following parameters: 
- [EnableAutoExpirationVersionTrim](#-EnableAutoExpirationVersionTrim)
- [MajorVersionLimit](#-MajorVersionLimit)
- [ExpireVersionsAfterDays](#-ExpireVersionsAfterDays)

This must be used with [ApplyToNewDocumentLibraries](#-ApplyToNewDocumentLibraries) switch set to true, because the version history limits are only applied on new document libraries in the site.

```yaml
Type: String[]
Parameter Sets: SetSiteFileTypeFileVersionPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HidePeoplePreviewingFiles

> Applicable: SharePoint Online

This setting disables the feature in OneDrive and SharePoint file previewing that displays the presence of other users on the file. It does not affect any experiences outside of the previewer.

PARAMVALUE: False | True

If set to True, the presence of other users on the file will no longer be displayed.

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HidePeopleWhoHaveListsOpen

> Applicable: SharePoint Online

This setting disables the feature in Microsoft Lists that displays the presence of other users on the list and its items when they are viewing.

PARAMVALUE: False | True

If set to True, the presence of other users on the list and its items will no longer be displayed. List presence is enabled by default.

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HubSiteId

> Applicable: SharePoint Online

Sets the hub site for a specified SharePoint site.

```yaml
Type: System.Guid
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Online

Specifies the URL of the site collection to update.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InformationBarriersMode

> Applicable: SharePoint Online

Specifies the information barrier mode.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InheritVersionPolicyFromTenant

> Applicable: SharePoint Online

Clear the file version setting at the site level. The new document libraries will use the Tenant Level setting. It won't impact the existing document libraries.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InheritVersionPolicyFromTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitedAccessFileType

> Applicable: SharePoint Online

The following parameters can be used with -ConditionalAccessPolicy AllowLimitedAccess for both the organization-wide setting and the site-level setting.

- OfficeOnlineFilesOnly: Allows users to preview only Office files in the browser. This option increases security but may be a barrier to user productivity.

- LimitedAccessFileType WebPreviewableFiles (default): Allows users to preview Office files and other file types (such as PDF files and images) in the browser. Note that the contents of file types other than Office files are handled in the browser. This option optimizes for user productivity but offers less security for files that aren't Office files.

- LimitedAccessFileType OtherFiles: Allows users to download files that can't be previewed, such as .zip and .exe. This option offers less security.

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SPOLimitedAccessFileType
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListsShowHeaderAndNavigation

> Applicable: SharePoint Online

Whether users see the full SharePoint chrome when they open a list.

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocaleId

Specifies the language of this site collection.
For more information, see Locale IDs Assigned by Microsoft (https://go.microsoft.com/fwlink/p/?LinkId=242911) (https://go.microsoft.com/fwlink/p/?LinkId=242911).

```yaml
Type: System.UInt32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LockState

> Applicable: SharePoint Online

Sets the lock state on a site.
Valid values are: NoAccess, ReadOnly and Unlock.
When the lock state of a site is ReadOnly, a message will appear on the site stating that the site is under maintenance and it is read-only.
When the lock state of a site is NoAccess, all traffic to the site will be blocked.
If parameter NoAccessRedirectUrl in the `Set-SPOTenant` cmdlet is set, traffic to sites that have a lock state NoAccess will be redirected to that URL.
If parameter NoAccessRedirectUrl is not set, a 403 error will be returned.
It isn't possible to set the lock state on the root site collection.

```yaml
Type: System.String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoopDefaultSharingLinkRole

> Applicable: SharePoint Online

Gets or sets default share link role for fluid on the site.

The valid values are:

- Edit
- None
- RestrictedView
- Review
- View

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingRole
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoopDefaultSharingLinkScope

> Applicable: SharePoint Online

Gets or sets default share link scope for fluid on the site.

The valid values are:

- Anyone
- Organization
- SpecificPeople
- Uninitialized

```yaml
Type: Microsoft.SharePoint.Client.Sharing.SharingScope
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorVersionLimit

> Applicable: SharePoint Online

When version history limits are managed manually (`EnableAutoExpirationVersionTrim $false`), admins will need to set the limits to the number of major versions (`MajorVersionLimit`) and the time period the versions are stored (`ExpireVersionsAfterDays`). Please check the description of `EnableAutoExpirationVersionTrim` for more details.

PARAMVALUE: Int32

```yaml
Type: System.Int32
Parameter Sets: SetSiteFileVersionPolicy, SetSiteFileTypeFileVersionPolicy
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
Parameter Sets: SetSiteFileVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaTranscription

> Applicable: SharePoint Online

When the feature is enabled, videos can have transcripts generated on demand or generated automatically in certain scenarios. This is the default because the policy is default on. If a video owner decides they don't want the transcript, they can always hide or delete it from that video.
Possible values:

- Enabled
- Disabled

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.MediaTranscriptionPolicyType
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait

> Applicable: SharePoint Online

Specifies to continue executing script immediately.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideBlockUserInfoVisibility

> Applicable: SharePoint Online

Choose whether to override the Block User Info Visibility policy on this site.

PARAMVALUE:

- OrganizationDefault (default) - Respect the organization-level Block User Info Visibility policy.
- ApplyToNoUsers – No users are prevented from accessing User Info when they have Limited Access permission only on the site.
- ApplyToAllUsers – All users (internal or external) are prevented from accessing User Info if they have Limited Access permission only on the site.
- ApplyToGuestAndExternalUsers – Only external or guest users are prevented from accessing User Info if they have Limited Access permission only on the site.
- ApplyToInternalUsers – Only internal users are prevented from accessing User Info if they have Limited Access permission only on the site.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SiteUserInfoVisibilityPolicyValue
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideSharingCapability

> Applicable: SharePoint Online

Determines whether it should override the sharing capability on its partition. For example, if the tenant sharing capability is `ExternalUserAndGuestSharing`, the core partition sharing capability is `Disabled`, and the sharing capability defined on the site collection is `ExternalUserAndGuestSharing`, the effective site sharing capability should be `Disabled` (the most restrictive one among tenant, partition, and site collecction) if `OverrideSharingCapability` is `false`. If `OverrideSharingCapability` is `true`, it skips checking partition sharing capability and the effective site sharing capability should be `ExternalUserAndGuestSharing`.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideTenantAnonymousLinkExpirationPolicy

> Applicable: SharePoint Online

Choose whether to override the anonymous or anyone link expiration policy on this site.

PARAMVALUE: None | False | True

- None - Respect the organization-level policy for anonymous or anyone link expiration
- False - Respect the organization-level policy for anonymous or anyone link expiration
- True - Override the organization-level policy for anonymous or anyone link expiration (can be more or less restrictive)

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideTenantExternalUserExpirationPolicy

> Applicable: SharePoint Online

Choose whether to override the external user expiration policy on this site.

Possible values:

- None: Respect the organization-level policy for external user expiration.
- False: Respect the organization-level policy for external user expiration.
- True: Override the organization-level policy for external user expiration (can be more or less restrictive).

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Owner

> Applicable: SharePoint Online

Specifies the owner of the site collection. Changing the Owner of a OneDrive is not supported and causes many experiences to break.

```yaml
Type: System.String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReadOnlyForBlockDownloadPolicy

> Applicable: SharePoint Online

Controls if read-only should be enabled for block download policy.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
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
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveInformationSegment

This parameter allows you to remove a segment from a SharePoint site. This parameter is only applicable for tenants who have enabled Microsoft 365 Information barriers capability. Please read https://learn.microsoft.com/sharepoint/information-barriers documentation to understand Information barriers with SharePoint Online.

**Note**: This parameter is available only in SharePoint Online Management Shell Version 16.0.19927.12000 or later.

```yaml
Type: System.Guid[]
Parameter Sets: RemoveInformationBarrierSegments
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLabel

This parameter allows you to remove the assigned sensitivity label on a site.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParamSet5
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRestrictedAccessControlGroups

> Applicable: SharePoint Online

Specifies the IDs of groups to be removed from access restriction policy and lose access.

```yaml
Type: System.Guid[]
Parameter Sets: RemoveRestrictedAccessControlGroups
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveVersionExpirationFileTypeOverride

> Applicable: SharePoint Online

An array of file type names. Removes the version history limits to a set of file types so that they will follow the default version history limits. 

This must be used with [ApplyToNewDocumentLibraries](#-ApplyToNewDocumentLibraries) switch set to true, because the version history limits are only applied on new document libraries in the site.

> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

```yaml
Type: String[]
Parameter Sets: RemoveSiteFileVersionPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestFilesLinkEnabled

> Applicable: SharePoint Online

Enables or disables the Request Files link on the site.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestFilesLinkExpirationInDays

> Applicable: SharePoint Online

Specifies the number of days before a Request Files link expires for the site.

The value can be from 0 to 730 days.

```yaml
Type: System.Int32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceQuota

Specifies the resource quota in megabytes of the site collection.
The default value is 0.
For more information, see Resource Usage Limits on Sandboxed Solutions in SharePoint 2010 (https://msdn.microsoft.com/en-us/library/gg615462.aspx) (https://msdn.microsoft.com/en-us/library/gg615462.aspx).

```yaml
Type: System.Double
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceQuotaWarningLevel

> Applicable: SharePoint Online

Specifies the warning level in megabytes of the site collection to warn the site collection administrator that the site is approaching the resource quota.

```yaml
Type: System.Double
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictContentOrgWideSearch

> Applicable: SharePoint Online

Controls whether org-wide content search is enabled for a site.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictedAccessControl

> Applicable: SharePoint Online

Sets access restriction policy by group membership.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictedAccessControlGroups

> Applicable: SharePoint Online

Specifies the IDs of groups that have access under an access restriction policy.

```yaml
Type: System.Guid[]
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictedContentDiscoveryforCopilotAndAgents

Sets or updates the site setting to host Agents by activating or deactivating the Restricted Content Discovery (RCD) for Agents. *Currently under private preview.*

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictedToGeo

> Applicable: SharePoint Online

PARAMVALUE: NoRestriction | BlockMoveOnly | BlockFull | Unknown

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.RestrictedToRegion
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SandboxedCodeActivationCapability

> Applicable: SharePoint Online

PARAMVALUE: Unknown | Check | Disabled | Enabled

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SandboxedCodeActivationCapabilities
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SensitivityLabel

> Applicable: SharePoint Online

Used to specify the unique identifier (GUID) of the SensitivityLabel.

```yaml
Type: System.String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingAllowedDomainList

> Applicable: SharePoint Online

Specifies a list of email domains that are allowed for sharing with the external collaborators. Use the space character as the delimiter for entering multiple values. For example, "contoso.com fabrikam.com".

For additional information about how to restrict a domain sharing, see [Restrict sharing of SharePoint and OneDrive content by domain](/sharepoint/restricted-domains-sharing).

```yaml
Type: System.String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingBlockedDomainList

> Applicable: SharePoint Online

Specifies a list of email domains that are blocked or prohibited for sharing with the external collaborators. Use space character as the delimiter for entering multiple values. For example, "contoso.com fabrikam.com".

For additional information about how to restrict a domain sharing, see [Restrict sharing of SharePoint and OneDrive content by domain](/sharepoint/restricted-domains-sharing).

```yaml
Type: System.String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingCapability

> Applicable: SharePoint Online

Determines what level of sharing is available for the site.

The valid values are:

- Disabled - Sharing outside your organization is disabled.
- ExistingExternalUserSharingOnly - Allow sharing only with the external users that already exist in your organization's directory.
- ExternalUserSharingOnly - External user sharing (share by email) is enabled, but anonymous link sharing is disabled.
- ExternalUserAndGuestSharing - External user sharing (share by email) and anonymous link sharing are both enabled.

For more information about sharing, see Turn external sharing on or off for SharePoint Online (<https://learn.microsoft.com/sharepoint/turn-external-sharing-on-or-off>).

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingCapabilities
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingDomainRestrictionMode

> Applicable: SharePoint Online

Specifies the sharing mode for external domains.

Possible values are:

- None - Do not restrict sharing by domain
- AllowList - Sharing is allowed only with external users that have account on domains specified with -SharingAllowedDomainList
- BlockList - Sharing is allowed with external users in all domains except in domains specified with -SharingBlockedDomainList

For additional information about how to restrict a domain sharing, see [Restrict sharing of SharePoint and OneDrive content by domain](/sharepoint/restricted-domains-sharing).

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingDomainRestrictionModes
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowPeoplePickerSuggestionsForGuestUsers

> Applicable: SharePoint Online

To enable the option to search for existing guest users at site collection level, set this parameter to $true.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SocialBarOnSitePagesDisabled

> Applicable: SharePoint Online

Disables or enables the Social Bar for Site Collection.

The Social Bar will appear on all modern SharePoint pages with the exception of the home page of a site. It will give users the ability to like a page, see the number of views, likes, and comments on a page, and see the people who have liked a page.

PARAMVALUE: False | True

```yaml
Type: System.Boolean
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuota

> Applicable: SharePoint Online

Specifies the storage quota in megabytes of the site collection.

```yaml
Type: System.Int64
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaReset

> Applicable: SharePoint Online

Resets the OneDrive for Business storage quota to the tenant's new default storage space.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaWarningLevel

> Applicable: SharePoint Online

Specifies the warning level in megabytes of the site collection to warn the site collection administrator that the site is approaching the storage quota.

```yaml
Type: System.Int64
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title

> Applicable: SharePoint Online

Specifies the title of the site collection.

```yaml
Type: System.String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateUserTypeFromAzureAD

> Applicable: SharePoint Online

Whether to update user types for all users in the site to match what's in Entra.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Online

The WhatIf switch doesn't work on this cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Set-SPOTenant](Set-SPOTenant.md)
