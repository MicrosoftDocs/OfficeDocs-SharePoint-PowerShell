---
external help file: Microsoft.Online.SharePoint.Powershell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.Powershell
online version:
schema: 2.0.0
---

# Set-SPOSite

## SYNOPSIS
{{ Fill in the Synopsis }}

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
 [-DefaultLinkPermission <SharingPermissionType>] [-FileAnonymousLinkType <AnonymousLinkType>]
 [-FolderAnonymousLinkType <AnonymousLinkType>] [-DefaultLinkToExistingAccess <Boolean>]
 [-DefaultLinkToExistingAccessReset] [-AnonymousLinkExpirationInDays <Int32>]
 [-OverrideTenantAnonymousLinkExpirationPolicy <Boolean>] [-ExternalUserExpirationInDays <Int32>]
 [-OverrideTenantExternalUserExpirationPolicy <Boolean>] [-OrganizationSharingLinkMaxExpirationInDays <Int32>]
 [-OrganizationSharingLinkRecommendedExpirationInDays <Int32>]
 [-OverrideTenantOrganizationSharingLinkExpirationPolicy <Boolean>]
 [-AnyoneSharingLinkRecommendedExpirationInDays <Int32>] [-InformationBarriersMode <String>]
 [-BlockDownloadLinksFileType <BlockDownloadLinksFileTypes>]
 [-OverrideBlockUserInfoVisibility <SiteUserInfoVisibilityPolicyValue>]
 [-LoopDefaultSharingLinkScope <SharingScope>] [-LoopDefaultSharingLinkRole <SharingRole>]
 [-RequestFilesLinkEnabled <Boolean>] [-RequestFilesLinkExpirationInDays <Int32>]
 [-OverrideSharingCapability <Boolean>] [-DefaultShareLinkScope <SharingScope>]
 [-DefaultShareLinkRole <SharingRole>] [-BlockGuestsAsSiteAdmin <SharingState>]
 [-RestrictContentOrgWideSearch <Boolean>] [-RestrictedAccessControl <Boolean>]
 [-RestrictedAccessControlGroups <Guid[]>] [-ListsShowHeaderAndNavigation <Boolean>]
 [-HidePeoplePreviewingFiles <Boolean>] [-HidePeopleWhoHaveListsOpen <Boolean>]
 [-DefaultMainLinkScope <MainLinkAudience>] [-IsAuthoritative <Boolean>] [-AllowFileArchive <Boolean>]
 [-AllowWebPropertyBagUpdateWhenDenyAddAndCustomizePagesIsEnabled <Boolean>]
 [-DisableClassicPageBaselineSecurityMode <Boolean>] [-DisableSiteBranding <Boolean>] [-WhatIf] [-Confirm]
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
Set-SPOSite [-Identity] <SpoSitePipeBind> [-InformationBarriersMode <String>]
 [-EnableAutoExpirationVersionTrim <Boolean>] [-ExpireVersionsAfterDays <Int32>] [-MajorVersionLimit <Int32>]
 -FileTypesForVersionExpiration <String[]> [-ApplyToNewDocumentLibraries] [-WhatIf] [-Confirm]
 [<CommonParameters>]
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
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AddInformationSegment
{{ Fill AddInformationSegment Description }}

```yaml
Type: Guid[]
Parameter Sets: AddInformationBarrierSegments
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRestrictedAccessControlGroups
{{ Fill AddRestrictedAccessControlGroups Description }}

```yaml
Type: Guid[]
Parameter Sets: AddRestrictedAccessControlGroups
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowDownloadingNonWebViewableFiles
{{ Fill AllowDownloadingNonWebViewableFiles Description }}

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

### -AllowEditing
{{ Fill AllowEditing Description }}

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

### -AllowFileArchive
{{ Fill AllowFileArchive Description }}

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

### -AllowSelfServiceUpgrade
{{ Fill AllowSelfServiceUpgrade Description }}

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

### -AllowWebPropertyBagUpdateWhenDenyAddAndCustomizePagesIsEnabled
{{ Fill AllowWebPropertyBagUpdateWhenDenyAddAndCustomizePagesIsEnabled Description }}

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

### -AnonymousLinkExpirationInDays
{{ Fill AnonymousLinkExpirationInDays Description }}

```yaml
Type: Int32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AnyoneSharingLinkRecommendedExpirationInDays
{{ Fill AnyoneSharingLinkRecommendedExpirationInDays Description }}

```yaml
Type: Int32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToExistingDocumentLibraries
{{ Fill ApplyToExistingDocumentLibraries Description }}

```yaml
Type: SwitchParameter
Parameter Sets: SetSiteFileVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToNewDocumentLibraries
{{ Fill ApplyToNewDocumentLibraries Description }}

```yaml
Type: SwitchParameter
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
{{ Fill AuthenticationContextAccessType Description }}

```yaml
Type: SPOAuthenticationContextPolicyAccessType
Parameter Sets: ParamSet1
Aliases:
Accepted values: AllowLimitedAccess, BlockAccess

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationContextName
{{ Fill AuthenticationContextName Description }}

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockDownloadLinksFileType
{{ Fill BlockDownloadLinksFileType Description }}

```yaml
Type: BlockDownloadLinksFileTypes
Parameter Sets: ParamSet1
Aliases:
Accepted values: WebPreviewableFiles, ServerRenderedFilesOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockDownloadPolicy
{{ Fill BlockDownloadPolicy Description }}

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

### -BlockGuestsAsSiteAdmin
{{ Fill BlockGuestsAsSiteAdmin Description }}

```yaml
Type: SharingState
Parameter Sets: ParamSet1
Aliases:
Accepted values: Unspecified, On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearGroupId
{{ Fill ClearGroupId Description }}

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

### -ClearRestrictedAccessControl
{{ Fill ClearRestrictedAccessControl Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ClearRestrictedAccessControl
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearSharingLockDown
{{ Fill ClearSharingLockDown Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ClearLockDown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommentsOnSitePagesDisabled
{{ Fill CommentsOnSitePagesDisabled Description }}

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

### -ConditionalAccessPolicy
{{ Fill ConditionalAccessPolicy Description }}

```yaml
Type: SPOConditionalAccessPolicyType
Parameter Sets: ParamSet1
Aliases:
Accepted values: AllowFullAccess, AllowLimitedAccess, BlockAccess, AuthenticationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultLinkPermission
{{ Fill DefaultLinkPermission Description }}

```yaml
Type: SharingPermissionType
Parameter Sets: ParamSet1
Aliases:
Accepted values: None, View, Edit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultLinkToExistingAccess
{{ Fill DefaultLinkToExistingAccess Description }}

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

### -DefaultLinkToExistingAccessReset
{{ Fill DefaultLinkToExistingAccessReset Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultMainLinkScope
{{ Fill DefaultMainLinkScope Description }}

```yaml
Type: MainLinkAudience
Parameter Sets: ParamSet1
Aliases:
Accepted values: OnlyPeopleAdded, Organization, Anyone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultShareLinkRole
{{ Fill DefaultShareLinkRole Description }}

```yaml
Type: SharingRole
Parameter Sets: ParamSet1
Aliases:
Accepted values: None, View, Edit, Review, RestrictedView

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultShareLinkScope
{{ Fill DefaultShareLinkScope Description }}

```yaml
Type: SharingScope
Parameter Sets: ParamSet1
Aliases:
Accepted values: Anyone, Organization, SpecificPeople, Uninitialized

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultSharingLinkType
{{ Fill DefaultSharingLinkType Description }}

```yaml
Type: SharingLinkType
Parameter Sets: ParamSet1
Aliases:
Accepted values: None, Direct, Internal, AnonymousAccess

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DenyAddAndCustomizePages
{{ Fill DenyAddAndCustomizePages Description }}

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

### -DisableAppViews
{{ Fill DisableAppViews Description }}

```yaml
Type: AppViewsPolicy
Parameter Sets: ParamSet1
Aliases:
Accepted values: Unknown, Disabled, NotDisabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableClassicPageBaselineSecurityMode
{{ Fill DisableClassicPageBaselineSecurityMode Description }}

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

### -DisableCompanyWideSharingLinks
{{ Fill DisableCompanyWideSharingLinks Description }}

```yaml
Type: CompanyWideSharingLinksPolicy
Parameter Sets: ParamSet1
Aliases:
Accepted values: Unknown, Disabled, NotDisabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableFlows
{{ Fill DisableFlows Description }}

```yaml
Type: FlowsPolicy
Parameter Sets: ParamSet1
Aliases:
Accepted values: Unknown, Disabled, NotDisabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSharingForNonOwners
{{ Fill DisableSharingForNonOwners Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ParamSet3
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSiteBranding
{{ Fill DisableSiteBranding Description }}

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
{{ Fill EnableAutoExpirationVersionTrim Description }}

```yaml
Type: Boolean
Parameter Sets: SetSiteFileVersionPolicy, SetSiteFileTypeFileVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnablePWA
{{ Fill EnablePWA Description }}

```yaml
Type: Boolean
Parameter Sets: ParamSet2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeBlockDownloadPolicySiteOwners
{{ Fill ExcludeBlockDownloadPolicySiteOwners Description }}

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

### -ExcludeBlockDownloadSharePointGroups
{{ Fill ExcludeBlockDownloadSharePointGroups Description }}

```yaml
Type: String[]
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedBlockDownloadGroupIds
{{ Fill ExcludedBlockDownloadGroupIds Description }}

```yaml
Type: Guid[]
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpireVersionsAfterDays
{{ Fill ExpireVersionsAfterDays Description }}

```yaml
Type: Int32
Parameter Sets: SetSiteFileVersionPolicy, SetSiteFileTypeFileVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalUserExpirationInDays
{{ Fill ExternalUserExpirationInDays Description }}

```yaml
Type: Int32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileAnonymousLinkType
{{ Fill FileAnonymousLinkType Description }}

```yaml
Type: AnonymousLinkType
Parameter Sets: ParamSet1
Aliases:
Accepted values: None, View, Edit, ViewUpload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileTypesForVersionExpiration
{{ Fill FileTypesForVersionExpiration Description }}

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

### -FolderAnonymousLinkType
{{ Fill FolderAnonymousLinkType Description }}

```yaml
Type: AnonymousLinkType
Parameter Sets: ParamSet1
Aliases:
Accepted values: None, View, Edit, ViewUpload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HidePeoplePreviewingFiles
{{ Fill HidePeoplePreviewingFiles Description }}

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

### -HidePeopleWhoHaveListsOpen
{{ Fill HidePeopleWhoHaveListsOpen Description }}

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

### -HubSiteId
{{ Fill HubSiteId Description }}

```yaml
Type: Guid
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
{{ Fill Identity Description }}

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

### -InformationBarriersMode
{{ Fill InformationBarriersMode Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InheritVersionPolicyFromTenant
{{ Fill InheritVersionPolicyFromTenant Description }}

```yaml
Type: SwitchParameter
Parameter Sets: InheritVersionPolicyFromTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsAuthoritative
{{ Fill IsAuthoritative Description }}

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

### -LimitedAccessFileType
{{ Fill LimitedAccessFileType Description }}

```yaml
Type: SPOLimitedAccessFileType
Parameter Sets: ParamSet1
Aliases:
Accepted values: OfficeOnlineFilesOnly, WebPreviewableFiles, OtherFiles

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListsShowHeaderAndNavigation
{{ Fill ListsShowHeaderAndNavigation Description }}

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

### -LocaleId
{{ Fill LocaleId Description }}

```yaml
Type: UInt32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LockState
{{ Fill LockState Description }}

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoopDefaultSharingLinkRole
{{ Fill LoopDefaultSharingLinkRole Description }}

```yaml
Type: SharingRole
Parameter Sets: ParamSet1
Aliases:
Accepted values: None, View, Edit, Review, RestrictedView

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoopDefaultSharingLinkScope
{{ Fill LoopDefaultSharingLinkScope Description }}

```yaml
Type: SharingScope
Parameter Sets: ParamSet1
Aliases:
Accepted values: Anyone, Organization, SpecificPeople, Uninitialized

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorVersionLimit
{{ Fill MajorVersionLimit Description }}

```yaml
Type: Int32
Parameter Sets: SetSiteFileVersionPolicy, SetSiteFileTypeFileVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorWithMinorVersionsLimit
{{ Fill MajorWithMinorVersionsLimit Description }}

```yaml
Type: Int32
Parameter Sets: SetSiteFileVersionPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaTranscription
{{ Fill MediaTranscription Description }}

```yaml
Type: MediaTranscriptionPolicyType
Parameter Sets: ParamSet1
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
{{ Fill NoWait Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrganizationSharingLinkMaxExpirationInDays
{{ Fill OrganizationSharingLinkMaxExpirationInDays Description }}

```yaml
Type: Int32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrganizationSharingLinkRecommendedExpirationInDays
{{ Fill OrganizationSharingLinkRecommendedExpirationInDays Description }}

```yaml
Type: Int32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideBlockUserInfoVisibility
{{ Fill OverrideBlockUserInfoVisibility Description }}

```yaml
Type: SiteUserInfoVisibilityPolicyValue
Parameter Sets: ParamSet1
Aliases:
Accepted values: OrganizationDefault, ApplyToNoUsers, ApplyToGuestAndExternalUsers, ApplyToInternalUsers, ApplyToAllUsers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideSharingCapability
{{ Fill OverrideSharingCapability Description }}

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

### -OverrideTenantAnonymousLinkExpirationPolicy
{{ Fill OverrideTenantAnonymousLinkExpirationPolicy Description }}

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

### -OverrideTenantExternalUserExpirationPolicy
{{ Fill OverrideTenantExternalUserExpirationPolicy Description }}

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

### -OverrideTenantOrganizationSharingLinkExpirationPolicy
{{ Fill OverrideTenantOrganizationSharingLinkExpirationPolicy Description }}

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

### -Owner
{{ Fill Owner Description }}

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReadOnlyForBlockDownloadPolicy
{{ Fill ReadOnlyForBlockDownloadPolicy Description }}

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

### -ReadOnlyForUnmanagedDevices
{{ Fill ReadOnlyForUnmanagedDevices Description }}

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

### -RemoveInformationSegment
{{ Fill RemoveInformationSegment Description }}

```yaml
Type: Guid[]
Parameter Sets: RemoveInformationBarrierSegments
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLabel
{{ Fill RemoveLabel Description }}

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

### -RemoveRestrictedAccessControlGroups
{{ Fill RemoveRestrictedAccessControlGroups Description }}

```yaml
Type: Guid[]
Parameter Sets: RemoveRestrictedAccessControlGroups
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveVersionExpirationFileTypeOverride
{{ Fill RemoveVersionExpirationFileTypeOverride Description }}

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
{{ Fill RequestFilesLinkEnabled Description }}

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

### -RequestFilesLinkExpirationInDays
{{ Fill RequestFilesLinkExpirationInDays Description }}

```yaml
Type: Int32
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceQuota
{{ Fill ResourceQuota Description }}

```yaml
Type: Double
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceQuotaWarningLevel
{{ Fill ResourceQuotaWarningLevel Description }}

```yaml
Type: Double
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictContentOrgWideSearch
{{ Fill RestrictContentOrgWideSearch Description }}

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

### -RestrictedAccessControl
{{ Fill RestrictedAccessControl Description }}

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

### -RestrictedAccessControlGroups
{{ Fill RestrictedAccessControlGroups Description }}

```yaml
Type: Guid[]
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictedToGeo
{{ Fill RestrictedToGeo Description }}

```yaml
Type: RestrictedToRegion
Parameter Sets: ParamSet1
Aliases:
Accepted values: NoRestriction, BlockMoveOnly, BlockFull, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SandboxedCodeActivationCapability
{{ Fill SandboxedCodeActivationCapability Description }}

```yaml
Type: SandboxedCodeActivationCapabilities
Parameter Sets: ParamSet1
Aliases:
Accepted values: Unknown, Check, Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SensitivityLabel
{{ Fill SensitivityLabel Description }}

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingAllowedDomainList
{{ Fill SharingAllowedDomainList Description }}

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingBlockedDomainList
{{ Fill SharingBlockedDomainList Description }}

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingCapability
{{ Fill SharingCapability Description }}

```yaml
Type: SharingCapabilities
Parameter Sets: ParamSet1
Aliases:
Accepted values: Disabled, ExternalUserSharingOnly, ExternalUserAndGuestSharing, ExistingExternalUserSharingOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingDomainRestrictionMode
{{ Fill SharingDomainRestrictionMode Description }}

```yaml
Type: SharingDomainRestrictionModes
Parameter Sets: ParamSet1
Aliases:
Accepted values: None, AllowList, BlockList

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowPeoplePickerSuggestionsForGuestUsers
{{ Fill ShowPeoplePickerSuggestionsForGuestUsers Description }}

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

### -SocialBarOnSitePagesDisabled
{{ Fill SocialBarOnSitePagesDisabled Description }}

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

### -StorageQuota
{{ Fill StorageQuota Description }}

```yaml
Type: Int64
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaReset
{{ Fill StorageQuotaReset Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaWarningLevel
{{ Fill StorageQuotaWarningLevel Description }}

```yaml
Type: Int64
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title
{{ Fill Title Description }}

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateUserTypeFromAzureAD
{{ Fill UpdateUserTypeFromAzureAD Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ParamSet1
Aliases:

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

Required: False
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
