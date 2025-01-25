---
external help file: sharepointonline.xml
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

### ParamSet1

```powershell
Set-SPOSite
 [-AddRestrictedAccessControlGroups [Guid[]]]
 [-AllowDownloadingNonWebViewableFiles <Boolean>]
 [-AllowEditing <Boolean>]
 [-AllowSelfServiceUpgrade <Boolean>]
 [-AnonymousLinkExpirationInDays <Int32>]
 [-AuthenticationContextAccessType <SPOAuthenticationContextPolicyAccessType>]
 [-AuthenticationContextName <String>]
 [-BlockDownloadLinksFileType <BlockDownloadLinksFileTypes>]
 [-BlockDownloadPolicy <Boolean>]
 [-ClearRestrictedAccessControl <SwitchParameter>]
 [-CommentsOnSitePagesDisabled <Boolean>]
 [-ConditionalAccessPolicy <SPOConditionalAccessPolicyType>]
 [-DefaultLinkPermission <SharingPermissionType>]
 [-DefaultLinkToExistingAccess <Boolean>]
 [-DefaultShareLinkRole <SharingRole>]
 [-DefaultShareLinkScope <SharingScope>]
 [-DefaultSharingLinkType <SharingLinkType>]
 [-DenyAddAndCustomizePages <Boolean>]
 [-DisableAppViews <AppViewsPolicy>]
 [-DisableCompanyWideSharingLinks <CompanyWideSharingLinksPolicy>]
 [-DisableFlows <FlowsPolicy>]
 [-ExcludeBlockDownloadPolicySiteOwners <Boolean>]
 [-ExcludedBlockDownloadGroupIds [Guid[]]]
 [-ExternalUserExpirationInDays <Int32>]
 [-HidePeoplePreviewingFiles <Boolean>]
 [-HidePeopleWhoHaveListsOpen <Boolean>]
 [-HubSiteId <Guid>]
 [-Identity <SpoSitePipeBind>]
 [-InformationBarriersMode <String>]
 [-LimitedAccessFileType <SPOLimitedAccessFileType>]
 [-LockState <String>]
 [-LoopDefaultSharingLinkRole <SharingRole>]
 [-LoopDefaultSharingLinkScope <SharingScope>]
 [-MediaTranscription <MediaTranscriptionPolicyType>]
 [-OverrideBlockUserInfoVisibility <String>]
 [-OverrideSharingCapability <Boolean>]
 [-OverrideTenantAnonymousLinkExpirationPolicy <Boolean>]
 [-OverrideTenantExternalUserExpirationPolicy <Boolean>]
 [-Owner <String>]
 [-ReadOnlyForBlockDownloadPolicy <Boolean>]
 [-ReadOnlyForUnmanagedDevices <Boolean>]
 [-RemoveLabel <SwitchParameter>]
 [-RemoveRestrictedAccessControlGroups [Guid[]]]
 [-RequestFilesLinkEnabled <Boolean>]
 [-RequestFilesLinkExpirationInDays <Int32>]
 [-ResourceQuotaWarningLevel <Double>]
 [-RestrictContentOrgWideSearch <Boolean>]
 [-RestrictedAccessControl <Boolean>]
 [-RestrictedAccessControlGroups [Guid[]]]
 [-RestrictedToGeo <RestrictedToRegion>]
 [-SandboxedCodeActivationCapability <SandboxedCodeActivationCapabilities>]
 [-SensitivityLabel <String>]
 [-SharingAllowedDomainList <String>]
 [-SharingBlockedDomainList <String>]
 [-SharingCapability <SharingCapabilities>]
 [-SharingDomainRestrictionMode <SharingDomainRestrictionModes>]
 [-ShowPeoplePickerSuggestionsForGuestUsers <Boolean>]
 [-SocialBarOnSitePagesDisabled <Boolean>]
 [-StorageQuota <Int64>]
 [-StorageQuotaReset <SwitchParameter>]
 [-StorageQuotaWarningLevel <Int64>]
 [-Title <String>]
 [<CommonParameters>]
```

### ParamSet2

```powershell
Set-SPOSite [-Identity] <SpoSitePipeBind> [-EnablePWA <Boolean>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ParamSet3

```powershell
Set-SPOSite [-Identity] <SpoSitePipeBind> [-Confirm] [-DisableSharingForNonOwners] [-WhatIf]
 [<CommonParameters>]
```

### ParamSet4 (valid for Group Site Collection)

```powershell
Set-SPOSite [-Identity] <SpoSitePipeBind> [-AllowSelfServiceUpgrade <Boolean>] [-Confirm]
 [-DenyAddAndCustomizePages <Boolean>] [-LockState <String>] [-NoWait] [-Owner <String>]
 [-ResourceQuotaWarningLevel <Double>]
 [-SandboxedCodeActivationCapability <SandboxedCodeActivationCapabilities>]
 [-SharingCapability <SharingCapabilities>] [-StorageQuota <Int64>] [-StorageQuotaWarningLevel <Int64>]
 [<CommonParameters>]
```

### SetSiteFileVersionPolicy

```powershell
Set-SPOSite [-Identity] <SpoSitePipeBind>
 [-EnableAutoExpirationVersionTrim <Boolean>]
 [-MajorVersionLimit <int>]
 [-MajorWithMinorVersionsLimit <int>]
 [-ExpireVersionsAfterDays <int>]
 [-ApplyToNewDocumentLibraries]
 [-ApplyToExistingDocumentLibraries]
 [-InheritVersionPolicyFromTenant]
 [<CommonParameters>]
```

### ClearGroupId

```powershell
Set-SPOSite [-Identity] <SpoSitePipeBind> [-ClearGroupId] [<CommonParameters>]
```

## DESCRIPTION

For any parameters that are passed in, the `Set-SPOSite` cmdlet sets or updates the setting for the site collection identified by parameter Identity.

You must be a SharePoint Online administrator and be a site collection administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).

For OneDrive for Business site collection, the only valid parameters are Identity, AllowDownloadingNonWebViewableFiles, AllowEditing, ConditionalAccessPolicy, DefaultLinkPermission, DefaultSharingLinkType, DisableCompanyWideSharingLinks, LimitedAccessFileType, LockState, Owner, SharingAllowedDomainList, SharingBlockedDomainList, SharingCapability, SharingDomainRestrictionMode, ShowPeoplePickerSuggestionsForGuestUsers, StorageQuota, and StorageWarningLevel.

For Groups site collection, the only valid parameters are Identity, AllowSelfServiceUpgrade, DefaultLinkPermission, DefaultSharingLinkType, DenyAddAndCustomizePages, DisableCompanyWideSharingLinks, DisableSharingForNonOwners, LockState, Owner, ResourceQuota, ResourceQuotaWarningLevel, SandboxedCodeActivationCapability, SharingCapability, ShowPeoplePickerSuggestionsForGuestUsers, SocialBarOnSitePagesDisabled, StorageQuota, StorageQuotaReset, and StorageQuotaWarningLevel.

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

Example 11 sets automatic version history limits at site level. Automatic setting will be applied to all new document libraries created in the site and a background request will be created to asynchronously process the update on existing document libraries that have versioning enabled.

### EXAMPLE 12

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -MajorWithMinorVersionsLimit 20 -ExpireVersionsAfterDays 30
```

Example 12 sets manual version history limits at site level by limiting the number of versions and the time (in days) versions are kept. The new document libraries will use this version setting. Also it creates a job to set this manual version setting for existing document libraries that enabled versioning.

### EXAMPLE 13

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -MajorWithMinorVersionsLimit 20 -ExpireVersionsAfterDays 0
```

Example 13 sets manual version history limits at site level by limiting the number of versions with no time limits. The new document libraries will use this version setting. Also it creates a job to set this manual version setting for existing document libraries that enabled versioning.

### Example 14

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $true -ApplyToNewDocumentLibraries
```

Example 14 sets automatic version history limits at site level. The new document libraries will use this version setting.

### EXAMPLE 15

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -ExpireVersionsAfterDays 30 -ApplyToNewDocumentLibraries
```

Example 15 sets manual version history limits at site level by limiting the number of versions and the time (in days) versions are kept. The new document libraries will use this version setting.

### EXAMPLE 16

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -ExpireVersionsAfterDays 0 -ApplyToNewDocumentLibraries
```

Example 16 sets manual version history limits at site level by limiting the number of versions with no time limits. The new document libraries will use this version setting.

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

Example 20 clears the file version setting at site level. The new document libraries will use the Tenant Level setting. It won't impact the existing document libraries.

## PARAMETERS

### -EnablePWA

Determines whether site can include Project Web App.
For more information about Project Web App, see Plan SharePoint groups in Project Server.

```yaml
Type: Boolean
Parameter Sets: ParamSet2
Aliases:
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

Specifies the URL of the site collection to update.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AllowSelfServiceUpgrade

Determines whether site collection administrators can upgrade their site collections.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DenyAddAndCustomizePages

Determines whether the Add And Customize Pages right is denied on the site collection.
For more information about permission levels, see User permissions and permission levels in SharePoint.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSharingForNonOwners

This parameter prevents non-owners from inviting new users to the site.

```yaml
Type: SwitchParameter
Parameter Sets: ParamSet3
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LockState

Sets the lock state on a site.
Valid values are: NoAccess, ReadOnly and Unlock.
When the lock state of a site is ReadOnly, a message will appear on the site stating that the site is under maintenance and it is read-only.
When the lock state of a site is NoAccess, all traffic to the site will be blocked.
If parameter NoAccessRedirectUrl in the `Set-SPOTenant` cmdlet is set, traffic to sites that have a lock state NoAccess will be redirected to that URL.
If parameter NoAccessRedirectUrl is not set, a 403 error will be returned.
It isn't possible to set the lock state on the root site collection.

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaTranscription

When the feature is enabled, videos can have transcripts generated on demand or generated automatically in certain scenarios. This is the default because the policy is default on. If a video owner decides they don't want the transcript, they can always hide or delete it from that video.
Possible values:

- Enabled
- Disabled

```yaml
Type: MediaTranscriptionPolicyType
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait

Specifies to continue executing script immediately.

```yaml
Type: SwitchParameter
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Owner

Specifies the owner of the site collection. Changing the Owner of a OneDrive is not supported and causes many experiences to break.

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceQuotaWarningLevel

Specifies the warning level in megabytes of the site collection to warn the site collection administrator that the site is approaching the resource quota.

```yaml
Type: Double
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictedAccessControl

Sets access restriction policy by group membership.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -SensitivityLabel

Used to specify the unique identifier (GUID) of the SensitivityLabel.

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SandboxedCodeActivationCapability

PARAMVALUE: Unknown | Check | Disabled | Enabled

```yaml
Type: SandboxedCodeActivationCapabilities
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockDownloadLinksFileType

The valid values are:

- WebPreviewableFiles
- ServerRenderedFilesOnly

**Note**: ServerRendered (Office Only) and WebPreviewable (All supported files).

The site's value is compared with the tenant level setting and the stricter one wins. For example, if the tenant is set to ServerRenderedFilesOnly then that will be used even if the site is set to WebPreviewableFiles.

```yaml
Type: BlockDownloadLinksFileTypes
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: WebPreviewableFiles
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingCapability

Determines what level of sharing is available for the site.

The valid values are:

- Disabled - Sharing outside your organization is disabled.
- ExistingExternalUserSharingOnly - Allow sharing only with the external users that already exist in your organization's directory.
- ExternalUserSharingOnly - External user sharing (share by email) is enabled, but anonymous link sharing is disabled.
- ExternalUserAndGuestSharing - External user sharing (share by email) and anonymous link sharing are both enabled.

For more information about sharing, see Turn external sharing on or off for SharePoint Online (<https://learn.microsoft.com/sharepoint/turn-external-sharing-on-or-off>).

```yaml
Type: SharingCapabilities
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuota

Specifies the storage quota in megabytes of the site collection.

```yaml
Type: Int64
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaWarningLevel

Specifies the warning level in megabytes of the site collection to warn the site collection administrator that the site is approaching the storage quota.

```yaml
Type: Int64
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title

Specifies the title of the site collection.

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

The WhatIf switch doesn't work on this cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowDownloadingNonWebViewableFiles

Specifies if non web viewable files can be downloaded.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommentsOnSitePagesDisabled

Use this parameter to disable Comments section on Site Pages.
The parameter can't be used for Groups Site Collections.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SocialBarOnSitePagesDisabled

Disables or enables the Social Bar for Site Collection.

The Social Bar will appear on all modern SharePoint pages with the exception of the home page of a site. It will give users the ability to like a page, see the number of views, likes, and comments on a page, and see the people who have liked a page.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAppViews

**Note**: This parameter has been retired and no longer functions.

Disables the Power Apps button.
Possible values:

- Disabled
- NotDisabled
- Unknown (not settable)

```yaml
Type: AppViewsPolicy
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableCompanyWideSharingLinks

Disables People in your organization links. For more information, see [People in your organization sharing links](https://learn.microsoft.com/microsoft-365/solutions/microsoft-365-limit-sharing#people-in-your-organization-sharing-links).

Possible values

- Disabled
- NotDisabled
- Unknown (not settable)

```yaml
Type: CompanyWideSharingLinksPolicy
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableFlows

**Note**: This parameter has been retired and no longer functions.

Disables the Power Automate button.
Possible values

- Disabled
- NotDisabled

```yaml
Type: FlowsPolicy
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictedToGeo

PARAMVALUE: NoRestriction | BlockMoveOnly | BlockFull | Unknown

```yaml
Type: RestrictedToRegion
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingAllowedDomainList

Specifies a list of email domains that are allowed for sharing with the external collaborators. Use the space character as the delimiter for entering multiple values. For example, "contoso.com fabrikam.com".

For additional information about how to restrict a domain sharing, see [Restrict sharing of SharePoint and OneDrive content by domain](https://learn.microsoft.com/sharepoint/restricted-domains-sharing).

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingBlockedDomainList

Specifies a list of email domains that are blocked or prohibited for sharing with the external collaborators. Use space character as the delimiter for entering multiple values. For example, "contoso.com fabrikam.com".

For additional information about how to restrict a domain sharing, see [Restrict sharing of SharePoint and OneDrive content by domain](https://learn.microsoft.com/sharepoint/restricted-domains-sharing).

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingDomainRestrictionMode

Specifies the sharing mode for external domains.

Possible values are:

- None - Do not restrict sharing by domain
- AllowList - Sharing is allowed only with external users that have account on domains specified with -SharingAllowedDomainList
- BlockList - Sharing is allowed with external users in all domains except in domains specified with -SharingBlockedDomainList

For additional information about how to restrict a domain sharing, see [Restrict sharing of SharePoint and OneDrive content by domain](https://learn.microsoft.com/sharepoint/restricted-domains-sharing).

```yaml
Type: SharingDomainRestrictionModes
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowPeoplePickerSuggestionsForGuestUsers

To enable the option to search for existing guest users at site collection level, set this parameter to $true.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaReset

Resets the OneDrive for Business storage quota to the tenant's new default storage space.

```yaml
Type: SwitchParameter
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultSharingLinkType

The default link type for the site collection. To be replaced by DefaultShareLinkScope.

PARAMVALUE: None | AnonymousAccess | Internal | Direct

- None - Respect the organization default sharing link type
- AnonymousAccess - Sets the default sharing link for this site to an Anonymous Access or Anyone link
- Internal - Sets the default sharing link for this site to the "organization" link or company shareable link
- Direct - Sets the default sharing link for this site to the "Specific people" link

```yaml
Type: SharingLinkType
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultLinkToExistingAccess

When set to TRUE, the DefaultSharingLinkType will be overriden and the default sharing link will a People with Existing Access link (which does not modify permissions). When set to FALSE (the default), the DefaultSharingLinkType parameter controls the default sharing link type.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultLinkPermission

The default link permission for the site collection. To be replaced by DefaultShareLinkRole.

PARAMVALUE: None | View | Edit

- None - Respect the organization default link permission
- View - Sets the default link permission for the site to "view" permissions
- Edit - Sets the default link permission for the site to "edit" permissions

```yaml
Type: SharingPermissionType
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoopDefaultSharingLinkScope

Gets or sets default share link scope for fluid on the site.

The valid values are:

- Anyone
- Organization
- SpecificPeople
- Uninitialized

```yaml
Type: SharingScope
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: Uninitialized
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoopDefaultSharingLinkRole

Gets or sets default share link role for fluid on the site.

The valid values are:

- Edit
- None
- RestrictedView
- Review
- View

```yaml
Type: SharingRole
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideTenantAnonymousLinkExpirationPolicy

Choose whether to override the anonymous or anyone link expiration policy on this site.

PARAMVALUE: None | False | True

- None - Respect the organization-level policy for anonymous or anyone link expiration
- False - Respect the organization-level policy for anonymous or anyone link expiration
- True - Override the organization-level policy for anonymous or anyone link expiration (can be more or less restrictive)

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AnonymousLinkExpirationInDays

Specifies all anonymous/anyone links that have been created (or will be created) will expire after the set number of days. Only applies if OverrideTenantAnonymousLinkExpirationPolicy is set to true.

The valid number should be between 1 and 730. To remove the expiration requirement, set the value to zero (0).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideTenantExternalUserExpirationPolicy

Choose whether to override the external user expiration policy on this site.

Possible values:

- None: Respect the organization-level policy for external user expiration.
- False: Respect the organization-level policy for external user expiration.
- True: Override the organization-level policy for external user expiration (can be more or less restrictive).

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalUserExpirationInDays

Specifies all external user expiration which will expire after the set number of days. Only applies if OverrideTenantExternalUserExpirationPolicy is set to true.

The maximum value is 730. To remove the expiration requirement, set the value to zero (0).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestFilesLinkEnabled

Enables or disables the Request Files link on the site.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestFilesLinkExpirationInDays

Specifies the number of days before a Request Files link expires for the site.

The value can be from 0 to 730 days.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionalAccessPolicy

Please read [Control access from unmanaged devices](/sharepoint/control-access-from-unmanaged-devices) documentation here to understand Conditional Access Policy usage in SharePoint Online.

Possible values:

- AllowFullAccess: Allows full access from desktop apps, mobile apps, and the web.
- AllowLimitedAccess: Allows limited, web-only access.
- BlockAccess: Blocks Access.
- AuthenticationContext: Assign a Microsoft Entra authentication context. Must add the AuthenticationContextName. Please read [Configure authentication contexts](/azure/active-directory/conditional-access/concept-conditional-access-cloud-apps#configure-authentication-contexts).

```yaml
Type: SPOConditionalAccessPolicyType
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: AllowFullAccess
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationContextName

The conditional access authentication context name.

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowEditing

Prevents users from editing Office files in the browser and copying and pasting Office file contents out of the browser window.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitedAccessFileType

The following parameters can be used with -ConditionalAccessPolicy AllowLimitedAccess for both the organization-wide setting and the site-level setting.

- OfficeOnlineFilesOnly: Allows users to preview only Office files in the browser. This option increases security but may be a barrier to user productivity.

- LimitedAccessFileType WebPreviewableFiles (default): Allows users to preview Office files and other file types (such as PDF files and images) in the browser. Note that the contents of file types other than Office files are handled in the browser. This option optimizes for user productivity but offers less security for files that aren't Office files.

- LimitedAccessFileType OtherFiles: Allows users to download files that can't be previewed, such as .zip and .exe. This option offers less security.

```yaml
Type: SPOLimitedAccessFileType
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: WebPreviewableFiles
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddInformationSegment

This parameter allows you to add a segment to a SharePoint site. This parameter is only applicable for tenants who have enabled Microsoft 365 Information barriers capability. Please read https://learn.microsoft.com/sharepoint/information-barriers documentation to understand Information barriers in SharePoint Online.

**Note**: This parameter is available only in SharePoint Online Management Shell Version 16.0.19927.12000 or later.

```yaml
Type: GUID
Required: False
Position: Named
Default value: None
```

### -RemoveInformationSegment

This parameter allows you to remove a segment from a SharePoint site. This parameter is only applicable for tenants who have enabled Microsoft 365 Information barriers capability. Please read https://learn.microsoft.com/sharepoint/information-barriers documentation to understand Information barriers with SharePoint Online.

**Note**: This parameter is available only in SharePoint Online Management Shell Version 16.0.19927.12000 or later.

```yaml
Type: GUID
Required: False
Position: Named
Default value: None
```

### -RemoveLabel

This parameter allows you to remove the assigned sensitivity label on a site.

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

### -BlockDownloadPolicy

As a SharePoint administrator in Microsoft 365, you can block the download of files from SharePoint sites or OneDrive. This feature does not need Microsoft Entra Conditional Access policies. This feature can be set for individual sites but not at the organization level.

Blocking the download of files allows users to remain productive while addressing the risk of accidental data loss. Users have browser-only access with no ability to download, print, or sync files. They also won't be able to access content through apps, including the Microsoft Office desktop apps. When web access is limited, users will see the following message at the top of sites: "Your organization doesn't allow you to download, print, or sync from this site. For help contact your IT department." Read the full documentation for advanced capabilities at [Block download policy for SharePoint sites and OneDrive](https://learn.microsoft.com/sharepoint/block-download-from-sites).

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideBlockUserInfoVisibility

Choose whether to override the Block User Info Visibility policy on this site.

PARAMVALUE:

- OrganizationDefault (default) - Respect the organization-level Block User Info Visibility policy.

- ApplyToNoUsers – No users are prevented from accessing User Info when they have Limited Access permission only on the site.

- ApplyToAllUsers – All users (internal or external) are prevented from accessing User Info if they have Limited Access permission only on the site.

- ApplyToGuestAndExternalUsers – Only external or guest users are prevented from accessing User Info if they have Limited Access permission only on the site.

- ApplyToInternalUsers – Only internal users are prevented from accessing User Info if they have Limited Access permission only on the site.

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: OrganizationDefault
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoExpirationVersionTrim

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
Type: Boolean
Parameter Sets: SetSiteFileVersionPolicy
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorVersionLimit

When version history limits are managed manually (`EnableAutoExpirationVersionTrim $false`), admins will need to set the limits to the number of major versions (`MajorVersionLimit`) and the time period the versions are stored (`ExpireVersionsAfterDays`). Please check the description of `EnableAutoExpirationVersionTrim` for more details.

PARAMVALUE: Int32

```yaml
Type: Int32
Parameter Sets: SetSiteFileVersionPolicy
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorWithMinorVersionsLimit

When version history limits are managed manually (`EnableAutoExpirationVersionTrim $false`), admins will need to set the limits to the number of major versions (`MajorVersionLimit`), the number of major with minor versions (`MajorWithMinorVersionsLimit`) and the time period the versions are stored (`ExpireVersionsAfterDays`). Please check the description of `EnableAutoExpirationVersionTrim` for more details.

PARAMVALUE: Int32

```yaml
Type: Int32
Parameter Sets: SetSiteFileVersionPolicy
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpireVersionsAfterDays

When version history limits are managed manually (`EnableAutoExpirationVersionTrim $false`), admins will need to set the limits to the number of major versions (`MajorVersionLimit`), the number of major with minor versions (`MajorWithMinorVersionsLimit`) and the time period the versions are stored (`ExpireVersionsAfterDays`). Please check the description of `EnableAutoExpirationVersionTrim` for more details.

PARAMVALUE: Int32

```yaml
Type: Int32
Parameter Sets: SetSiteFileVersionPolicy
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToNewDocumentLibraries

Apply the version history limits setting to new document libraries.

```yaml
Type: Int32
Parameter Sets: SetSiteFileVersionPolicy
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToExistingDocumentLibraries

Create a job to apply the version history limits setting to existing document libraries.

```yaml
Type: Int32
Parameter Sets: SetSiteFileVersionPolicy
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InheritVersionPolicyFromTenant

Clear the file version setting at site level. The new document libraries will use the Tenant Level setting. It won't impact the existing document libraries.

```yaml
Type: Int32
Parameter Sets: SetSiteFileVersionPolicy
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideSharingCapability

Determines whether it should override the sharing capability on its partition. For example, if the tenant sharing capability is `ExternalUserAndGuestSharing`, the core partition sharing capability is `Disabled`, and the sharing capability defined on the site collection is `ExternalUserAndGuestSharing`, the effective site sharing capability should be `Disabled` (the most restrictive one among tenant, partition, and site collecction) if `OverrideSharingCapability` is `false`. If `OverrideSharingCapability` is `true`, it skips checking partition sharing capability and the effective site sharing capability should be `ExternalUserAndGuestSharing`.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultShareLinkScope

The default share link scope on the site. It replaces `DefaultSharingLinkType`.

The valid values are:

- Anyone
- Organization
- SpecificPeople
- Uninitialized

```yaml
Type: SharingScope
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: Uninitialized
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultShareLinkRole

The default share link role for the site collection. It replaces `DefaultLinkPermission`.

The valid values are:

- Edit
- None
- RestrictedView
- Review
- View

```yaml
Type: SharingRole
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HidePeoplePreviewingFiles

This setting disables the feature in OneDrive and SharePoint file previewing that displays the presence of other users on the file. It does not affect any experiences outside of the previewer.

PARAMVALUE: False | True

If set to True, the presence of other users on the file will no longer be displayed.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -HidePeopleWhoHaveListsOpen

This setting disables the feature in Microsoft Lists that displays the presence of other users on the list and its items when they are viewing.

PARAMVALUE: False | True

If set to True, the presence of other users on the list and its items will no longer be displayed. List presence is enabled by default.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearGroupId

This parameter allows you to remove the assigned Microsoft 365 group ID on a site, when the group is permanently deleted.

```yaml
Type: SwitchParameter
Parameter Sets: ClearGroupId
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
Parameter Sets: (All)
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedBlockDownloadGroupIds

Exempts users from specified groups from the block download policy and they can fully download any content for the site.

```yaml
Type: Guid[]
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeBlockDownloadPolicySiteOwners

Controls if site owners are excluded from block download policy.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReadOnlyForBlockDownloadPolicy

Controls if read-only should be enabled for block download policy.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeBlockDownloadSharePointGroups

Specifies the groups excluded from the block download policy.

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationContextAccessType

Controls whether Authentication Context Limited Access is enabled for a site.

The valid values are:

- AllowLimitedAccess
- BlockAccess

```yaml
Type: SPOAuthenticationContextPolicyAccessType
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HubSiteId

Sets the hub site for a specified SharePoint site.

```yaml
Type: GUID
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationBarriersMode

Specifies the information barrier mode.

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictContentOrgWideSearch

Controls whether org-wide content search is enabled for a site.

PARAMVALUE: False | True

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictedAccessControlGroups

Specifies the IDs of groups that have access under an access restriction policy.

```yaml
Type: Guid[]
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRestrictedAccessControlGroups

Specifies the IDs of groups to be added to an access restriction policy and gain access.

```yaml
Type: Guid[]
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRestrictedAccessControlGroups

Specifies the IDs of groups to be removed from access restriction policy and lose access.

```yaml
Type: Guid[]
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearRestrictedAccessControl

Clears the list of groups that are given access via an access restriction policy.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
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

[Getting started with SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Set-SPOTenant](Set-SPOTenant.md)
