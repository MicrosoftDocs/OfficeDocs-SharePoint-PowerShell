---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spotenant
applicable: SharePoint Online
title: Set-SPOTenant
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Set-SPOTenant

## SYNOPSIS

Sets properties on the SharePoint Online organization.

## SYNTAX

### None (Default)
```
Set-SPOTenant [-MinCompatibilityLevel <Int32>] [-MaxCompatibilityLevel <Int32>]
 [-ExternalServicesEnabled <Boolean>] [-NoAccessRedirectUrl <String>] [-ArchiveRedirectUrl <String>]
 [-SharingCapability <SharingCapabilities>] [-DisplayStartASiteOption <Boolean>] [-StartASiteFormUrl <String>]
 [-ShowEveryoneClaim <Boolean>] [-ShowAllUsersClaim <Boolean>]
 [-ShowEveryoneExceptExternalUsersClaim <Boolean>]
 [-AllowEveryoneExceptExternalUsersClaimInPrivateSite <Boolean>] [-SearchResolveExactEmailOrUPN <Boolean>]
 [-OfficeClientADALDisabled <Boolean>] [-LegacyAuthProtocolsEnabled <Boolean>]
 [-LegacyBrowserAuthProtocolsEnabled <Boolean>] [-DisableCustomAppAuthentication <Boolean>]
 [-IsSharePointAddInsDisabled <Boolean>] [-IsSharePointAddInsBlocked <Boolean>]
 [-DisableSharePointStoreAccess <Boolean>] [-SiteOwnerManageLegacyServicePrincipalEnabled <Boolean>]
 [-RequireAcceptingAccountMatchInvitedAccount <Boolean>] [-ProvisionSharedWithEveryoneFolder <Boolean>]
 [-SignInAccelerationDomain <String>] [-EnableGuestSignInAcceleration <Boolean>]
 [-UsePersistentCookiesForExplorerView <Boolean>] [-ReSyncTenantPrivacyProfile]
 [-BccExternalSharingInvitations <Boolean>] [-BccExternalSharingInvitationsList <String>]
 [-PublicCdnEnabled <Boolean>] [-PublicCdnAllowedFileTypes <String>]
 [-RequireAnonymousLinksExpireInDays <Int32>] [-SharingAllowedDomainList <String>]
 [-SharingBlockedDomainList <String>] [-SharingDomainRestrictionMode <SharingDomainRestrictionModes>]
 [-OneDriveStorageQuota <Int64>] [-OneDriveForGuestsEnabled <Boolean>] [-IPAddressEnforcement <Boolean>]
 [-IPAddressAllowList <String>] [-IPAddressWACTokenLifetime <Int32>]
 [-EnableTenantRestrictionsInsights <Boolean>] [-EnablePromotedFileHandlers <Boolean>]
 [-UseFindPeopleInPeoplePicker <Boolean>] [-DefaultSharingLinkType <SharingLinkType>]
 [-ODBMembersCanShare <SharingState>] [-ODBAccessRequests <SharingState>]
 [-PreventExternalUsersFromResharing <Boolean>] [-ShowPeoplePickerSuggestionsForGuestUsers <Boolean>]
 [-AppOnlyBypassPeoplePickerPolicies <Boolean>] [-EnableDiscoverableByOrganizationForVideos <Boolean>]
 [-FileAnonymousLinkType <AnonymousLinkType>] [-FolderAnonymousLinkType <AnonymousLinkType>]
 [-NotifyOwnersWhenItemsReshared <Boolean>] [-NotifyOwnersWhenInvitationsAccepted <Boolean>]
 [-NotificationsInOneDriveForBusinessEnabled <Boolean>] [-NotificationsInSharePointEnabled <Boolean>]
 [-SelfServiceSiteCreationDisabled <Boolean>]
 [-SpecialCharactersStateInFileFolderNames <SpecialCharactersState>] [-OwnerAnonymousNotification <Boolean>]
 [-CommentsOnSitePagesDisabled <Boolean>] [-CommentsOnFilesDisabled <Boolean>]
 [-CommentsOnListItemsDisabled <Boolean>] [-ViewersCanCommentOnMediaDisabled <Boolean>]
 [-SocialBarOnSitePagesDisabled <Boolean>] [-OrphanedPersonalSitesRetentionPeriod <Int32>]
 [-PermissiveBrowserFileHandlingOverride <Boolean>] [-DisallowInfectedFileDownload <Boolean>]
 [-DefaultLinkPermission <SharingPermissionType>] [-CustomizedExternalSharingServiceUrl <String>]
 [-ConditionalAccessPolicyErrorHelpLink <String>] [-RestrictedAccessControlforSitesErrorHelpLink <String>]
 [-RestrictedAccessControlForOneDriveErrorHelpLink <String>]
 [-ApplyAppEnforcedRestrictionsToAdHocRecipients <Boolean>] [-FilePickerExternalImageSearchEnabled <Boolean>]
 [-EmailAttestationRequired <Boolean>] [-EmailAttestationReAuthDays <Int32>]
 [-SyncPrivacyProfileProperties <Boolean>] [-DisabledWebPartIds <Guid[]>]
 [-DisabledAdaptiveCardExtensionIds <Guid[]>] [-EnableMinimumVersionRequirement <Boolean>]
 [-MarkNewFilesSensitiveByDefault <SensitiveByDefaultState>] [-EnableAIPIntegration <Boolean>]
 [-SyncAadB2BManagementPolicy <Boolean>] [-AllowCommentsTextOnEmailEnabled <Boolean>]
 [-EnableAzureADB2BIntegration <Boolean>] [-DisableAddShortcutsToOneDrive <Boolean>]
 [-IncludeAtAGlanceInShareEmails <Boolean>] [-DisableWorkflow2010 <Boolean>] [-EnableAutoNewsDigest <Boolean>]
 [-StopNew2010Workflows <Boolean>] [-StopNew2013Workflows <Boolean>] [-DisableBackToClassic <Boolean>]
 [-ExternalUserExpirationRequired <Boolean>] [-ExternalUserExpireInDays <Int32>]
 [-BlockDownloadLinksFileType <BlockDownloadLinksFileTypes>] [-AnyoneLinkTrackUsers <Boolean>]
 [-BlockAppAccessWithAuthenticationContext <Boolean>] [-OneDriveLoopDefaultSharingLinkScope <SharingScope>]
 [-OneDriveLoopDefaultSharingLinkRole <SharingRole>] [-OneDriveRequestFilesLinkEnabled <Boolean>]
 [-OneDriveRequestFilesLinkExpirationInDays <Int32>] [-OneDriveSharingCapability <SharingCapabilities>]
 [-OneDriveDefaultShareLinkScope <SharingScope>] [-OneDriveDefaultShareLinkRole <SharingRole>]
 [-OneDriveDefaultLinkToExistingAccess <Boolean>] [-OneDriveBlockGuestsAsSiteAdmin <SharingState>]
 [-CoreLoopDefaultSharingLinkScope <SharingScope>] [-CoreLoopDefaultSharingLinkRole <SharingRole>]
 [-CoreSharingCapability <SharingCapabilities>] [-AllowSharingOutsideRestrictedAccessControlGroups <Boolean>]
 [-CoreRequestFilesLinkEnabled <Boolean>] [-CoreRequestFilesLinkExpirationInDays <Int32>]
 [-CoreDefaultShareLinkScope <SharingScope>] [-CoreDefaultShareLinkRole <SharingRole>]
 [-CoreDefaultLinkToExistingAccess <Boolean>] [-CoreBlockGuestsAsSiteAdmin <SharingState>]
 [-AllowAnonymousMeetingParticipantsToAccessWhiteboards <SharingState>] [-Workflows2013Enabled <Boolean>]
 [-IsFluidEnabled <Boolean>] [-IsWBFluidEnabled <Boolean>] [-IsCollabMeetingNotesFluidEnabled <Boolean>]
 [-IsLoopEnabled <Boolean>] [-DisableDocumentLibraryDefaultLabeling <Boolean>]
 [-ExtendPermissionsToUnprotectedFiles <Boolean>] [-EnableSensitivityLabelForPDF <Boolean>]
 [-BlockSendLabelMismatchEmail <Boolean>] [-LabelMismatchEmailHelpLink <String>]
 [-BlockUserInfoVisibility <String>] [-BlockUserInfoVisibilityInOneDrive <TenantBrowseUserInfoPolicyValue>]
 [-BlockUserInfoVisibilityInSharePoint <TenantBrowseUserInfoPolicyValue>]
 [-AllowOverrideForBlockUserInfoVisibility <Boolean>] [-DisablePersonalListCreation <Boolean>]
 [-DisableSpacesActivation <Boolean>] [-DisableVivaConnectionsAnalytics <Boolean>]
 [-InformationBarriersSuspension <Boolean>] [-IBImplicitGroupBased <Boolean>]
 [-AppBypassInformationBarriers <Boolean>] [-AppAccessInformationBarriersAllowList <Guid[]>]
 [-AllOrganizationSecurityGroupId <Guid>] [-DisableModernListTemplateIds <Guid[]>]
 [-EnableModernListTemplateIds <Guid[]>] [-HideSyncButtonOnTeamSite <Boolean>]
 [-AllowGuestUserShareToUsersNotInSiteCollection <Boolean>] [-StreamLaunchConfig <Int32>]
 [-DelegateRestrictedContentDiscoverabilityManagement <Boolean>]
 [-DelegateRestrictedAccessControlManagement <Boolean>] [-DisableOutlookPSTVersionTrimming <Boolean>]
 [-MediaTranscription <MediaTranscriptionPolicyType>]
 [-MediaTranscriptionAutomaticFeatures <MediaTranscriptionAutomaticFeaturesPolicyType>]
 [-ViewInFileExplorerEnabled <Boolean>] [-AuthContextResilienceMode <SPResilienceModeType>]
 [-ReduceTempTokenLifetimeEnabled <Boolean>] [-ReduceTempTokenLifetimeValue <Int32>]
 [-ShowOpenInDesktopOptionForSyncedFiles <Boolean>] [-ShowPeoplePickerGroupSuggestionsForIB <Boolean>]
 [-EnableRestrictedAccessControl <Boolean>] [-BlockDownloadFileTypePolicy <Boolean>]
 [-BlockDownloadFileTypeIds <SPBlockDownloadFileTypeId[]>] [-ExcludedBlockDownloadGroupIds <Guid[]>]
 [-TlsTokenBindingPolicyValue <SPOTlsTokenBindingPolicyValue>] [-RecycleBinRetentionPeriod <Int32>]
 [-IsEnableAppAuthPopUpEnabled <Boolean>] [-IsDataAccessInCardDesignerEnabled <Boolean>]
 [-MassDeleteNotificationDisabled <Boolean>] [-EnableAutoExpirationVersionTrim <Boolean>]
 [-EnableMediaReactions <Boolean>] [-BusinessConnectivityServiceDisabled <Boolean>]
 [-ExpireVersionsAfterDays <Int32>] [-MajorVersionLimit <Int32>] [-AllowSensitivityLabelOnRecords <Boolean>]
 [-DelayDenyAddAndCustomizePagesEnforcement <Boolean>]
 [-DelayDenyAddAndCustomizePagesEnforcementOnClassicPublishingSites <Boolean>]
 [-AllowClassicPublishingSiteCreation <Boolean>] [-WhoCanShareAnonymousAllowList <Guid[]>]
 [-WhoCanShareAuthenticatedGuestAllowList <Guid[]>]
 [-ResyncContentSecurityPolicyConfigurationEntries <Boolean>] [-ContentSecurityPolicyEnforcement <Boolean>]
 [-DocumentUnderstandingModelScope <SyntexFeatureScopeValue>]
 [-DocumentUnderstandingModelSelectedSitesList <String[]>]
 [-DocumentUnderstandingModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AIBuilderModelScope <SyntexFeatureScopeValue>] [-AIBuilderModelSelectedSitesList <String[]>]
 [-AIBuilderModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AIBuilderModelSelectedSitesIncludesContentCenters <Boolean>] [-PrebuiltModelScope <SyntexFeatureScopeValue>]
 [-PrebuiltModelSelectedSitesList <String[]>]
 [-PrebuiltModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-DocumentTranslationScope <SyntexFeatureScopeValue>] [-DocumentTranslationSelectedSitesList <String[]>]
 [-DocumentTranslationSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AutofillColumnsScope <SyntexFeatureScopeValue>] [-AutofillColumnsSelectedSitesList <String[]>]
 [-AutofillColumnsSelectedSitesListOperation <SelectedSitesListOperations>]
 [-OpticalCharacterRecognitionScope <SyntexFeatureScopeValue>]
 [-OpticalCharacterRecognitionSelectedSitesList <String[]>]
 [-OpticalCharacterRecognitionSelectedSitesListOperation <SelectedSitesListOperations>]
 [-DefaultContentCenterSite <String>]
 [-AllowWebPropertyBagUpdateWhenDenyAddAndCustomizePagesIsEnabled <Boolean>] [-EnforceRequestDigest <Boolean>]
 [<CommonParameters>]
```

### ParameterSetContentTypeSyncSiteTemplatesList
```
Set-SPOTenant [-MinCompatibilityLevel <Int32>] [-MaxCompatibilityLevel <Int32>]
 [-ExternalServicesEnabled <Boolean>] [-NoAccessRedirectUrl <String>] [-ArchiveRedirectUrl <String>]
 [-SharingCapability <SharingCapabilities>] [-DisplayStartASiteOption <Boolean>] [-StartASiteFormUrl <String>]
 [-ShowEveryoneClaim <Boolean>] [-ShowAllUsersClaim <Boolean>]
 [-ShowEveryoneExceptExternalUsersClaim <Boolean>]
 [-AllowEveryoneExceptExternalUsersClaimInPrivateSite <Boolean>] [-SearchResolveExactEmailOrUPN <Boolean>]
 [-OfficeClientADALDisabled <Boolean>] [-LegacyAuthProtocolsEnabled <Boolean>]
 [-LegacyBrowserAuthProtocolsEnabled <Boolean>] [-DisableCustomAppAuthentication <Boolean>]
 [-IsSharePointAddInsDisabled <Boolean>] [-IsSharePointAddInsBlocked <Boolean>]
 [-DisableSharePointStoreAccess <Boolean>] [-SiteOwnerManageLegacyServicePrincipalEnabled <Boolean>]
 [-RequireAcceptingAccountMatchInvitedAccount <Boolean>] [-ProvisionSharedWithEveryoneFolder <Boolean>]
 [-SignInAccelerationDomain <String>] [-EnableGuestSignInAcceleration <Boolean>]
 [-UsePersistentCookiesForExplorerView <Boolean>] -ContentTypeSyncSiteTemplatesList <String[]>
 [-ExcludeSiteTemplate] [-ReSyncTenantPrivacyProfile] [-BccExternalSharingInvitations <Boolean>]
 [-BccExternalSharingInvitationsList <String>] [-PublicCdnEnabled <Boolean>]
 [-PublicCdnAllowedFileTypes <String>] [-RequireAnonymousLinksExpireInDays <Int32>]
 [-SharingAllowedDomainList <String>] [-SharingBlockedDomainList <String>]
 [-SharingDomainRestrictionMode <SharingDomainRestrictionModes>] [-OneDriveStorageQuota <Int64>]
 [-OneDriveForGuestsEnabled <Boolean>] [-IPAddressEnforcement <Boolean>] [-IPAddressAllowList <String>]
 [-IPAddressWACTokenLifetime <Int32>] [-EnableTenantRestrictionsInsights <Boolean>]
 [-EnablePromotedFileHandlers <Boolean>] [-UseFindPeopleInPeoplePicker <Boolean>]
 [-DefaultSharingLinkType <SharingLinkType>] [-ODBMembersCanShare <SharingState>]
 [-ODBAccessRequests <SharingState>] [-PreventExternalUsersFromResharing <Boolean>]
 [-ShowPeoplePickerSuggestionsForGuestUsers <Boolean>] [-AppOnlyBypassPeoplePickerPolicies <Boolean>]
 [-EnableDiscoverableByOrganizationForVideos <Boolean>] [-FileAnonymousLinkType <AnonymousLinkType>]
 [-FolderAnonymousLinkType <AnonymousLinkType>] [-NotifyOwnersWhenItemsReshared <Boolean>]
 [-NotifyOwnersWhenInvitationsAccepted <Boolean>] [-NotificationsInOneDriveForBusinessEnabled <Boolean>]
 [-NotificationsInSharePointEnabled <Boolean>] [-SelfServiceSiteCreationDisabled <Boolean>]
 [-SpecialCharactersStateInFileFolderNames <SpecialCharactersState>] [-OwnerAnonymousNotification <Boolean>]
 [-CommentsOnSitePagesDisabled <Boolean>] [-CommentsOnFilesDisabled <Boolean>]
 [-CommentsOnListItemsDisabled <Boolean>] [-ViewersCanCommentOnMediaDisabled <Boolean>]
 [-SocialBarOnSitePagesDisabled <Boolean>] [-OrphanedPersonalSitesRetentionPeriod <Int32>]
 [-PermissiveBrowserFileHandlingOverride <Boolean>] [-DisallowInfectedFileDownload <Boolean>]
 [-DefaultLinkPermission <SharingPermissionType>] [-CustomizedExternalSharingServiceUrl <String>]
 [-ConditionalAccessPolicyErrorHelpLink <String>] [-RestrictedAccessControlforSitesErrorHelpLink <String>]
 [-RestrictedAccessControlForOneDriveErrorHelpLink <String>]
 [-ApplyAppEnforcedRestrictionsToAdHocRecipients <Boolean>] [-FilePickerExternalImageSearchEnabled <Boolean>]
 [-EmailAttestationRequired <Boolean>] [-EmailAttestationReAuthDays <Int32>]
 [-SyncPrivacyProfileProperties <Boolean>] [-DisabledWebPartIds <Guid[]>]
 [-DisabledAdaptiveCardExtensionIds <Guid[]>] [-EnableMinimumVersionRequirement <Boolean>]
 [-MarkNewFilesSensitiveByDefault <SensitiveByDefaultState>] [-EnableAIPIntegration <Boolean>]
 [-SyncAadB2BManagementPolicy <Boolean>] [-AllowCommentsTextOnEmailEnabled <Boolean>]
 [-EnableAzureADB2BIntegration <Boolean>] [-DisableAddShortcutsToOneDrive <Boolean>]
 [-IncludeAtAGlanceInShareEmails <Boolean>] [-DisableWorkflow2010 <Boolean>] [-EnableAutoNewsDigest <Boolean>]
 [-StopNew2010Workflows <Boolean>] [-StopNew2013Workflows <Boolean>] [-DisableBackToClassic <Boolean>]
 [-ExternalUserExpirationRequired <Boolean>] [-ExternalUserExpireInDays <Int32>]
 [-BlockDownloadLinksFileType <BlockDownloadLinksFileTypes>] [-AnyoneLinkTrackUsers <Boolean>]
 [-BlockAppAccessWithAuthenticationContext <Boolean>] [-OneDriveLoopDefaultSharingLinkScope <SharingScope>]
 [-OneDriveLoopDefaultSharingLinkRole <SharingRole>] [-OneDriveRequestFilesLinkEnabled <Boolean>]
 [-OneDriveRequestFilesLinkExpirationInDays <Int32>] [-OneDriveSharingCapability <SharingCapabilities>]
 [-OneDriveDefaultShareLinkScope <SharingScope>] [-OneDriveDefaultShareLinkRole <SharingRole>]
 [-OneDriveDefaultLinkToExistingAccess <Boolean>] [-OneDriveBlockGuestsAsSiteAdmin <SharingState>]
 [-CoreLoopDefaultSharingLinkScope <SharingScope>] [-CoreLoopDefaultSharingLinkRole <SharingRole>]
 [-CoreSharingCapability <SharingCapabilities>] [-AllowSharingOutsideRestrictedAccessControlGroups <Boolean>]
 [-CoreRequestFilesLinkEnabled <Boolean>] [-CoreRequestFilesLinkExpirationInDays <Int32>]
 [-CoreDefaultShareLinkScope <SharingScope>] [-CoreDefaultShareLinkRole <SharingRole>]
 [-CoreDefaultLinkToExistingAccess <Boolean>] [-CoreBlockGuestsAsSiteAdmin <SharingState>]
 [-AllowAnonymousMeetingParticipantsToAccessWhiteboards <SharingState>] [-Workflows2013Enabled <Boolean>]
 [-IsFluidEnabled <Boolean>] [-IsWBFluidEnabled <Boolean>] [-IsCollabMeetingNotesFluidEnabled <Boolean>]
 [-IsLoopEnabled <Boolean>] [-DisableDocumentLibraryDefaultLabeling <Boolean>]
 [-ExtendPermissionsToUnprotectedFiles <Boolean>] [-EnableSensitivityLabelForPDF <Boolean>]
 [-BlockSendLabelMismatchEmail <Boolean>] [-LabelMismatchEmailHelpLink <String>]
 [-BlockUserInfoVisibility <String>] [-BlockUserInfoVisibilityInOneDrive <TenantBrowseUserInfoPolicyValue>]
 [-BlockUserInfoVisibilityInSharePoint <TenantBrowseUserInfoPolicyValue>]
 [-AllowOverrideForBlockUserInfoVisibility <Boolean>] [-DisablePersonalListCreation <Boolean>]
 [-DisableSpacesActivation <Boolean>] [-DisableVivaConnectionsAnalytics <Boolean>]
 [-InformationBarriersSuspension <Boolean>] [-IBImplicitGroupBased <Boolean>]
 [-AppBypassInformationBarriers <Boolean>] [-AppAccessInformationBarriersAllowList <Guid[]>]
 [-AllOrganizationSecurityGroupId <Guid>] [-DisableModernListTemplateIds <Guid[]>]
 [-EnableModernListTemplateIds <Guid[]>] [-HideSyncButtonOnTeamSite <Boolean>]
 [-AllowGuestUserShareToUsersNotInSiteCollection <Boolean>] [-StreamLaunchConfig <Int32>]
 [-DelegateRestrictedContentDiscoverabilityManagement <Boolean>]
 [-DelegateRestrictedAccessControlManagement <Boolean>] [-DisableOutlookPSTVersionTrimming <Boolean>]
 [-MediaTranscription <MediaTranscriptionPolicyType>]
 [-MediaTranscriptionAutomaticFeatures <MediaTranscriptionAutomaticFeaturesPolicyType>]
 [-ViewInFileExplorerEnabled <Boolean>] [-AuthContextResilienceMode <SPResilienceModeType>]
 [-ReduceTempTokenLifetimeEnabled <Boolean>] [-ReduceTempTokenLifetimeValue <Int32>]
 [-ShowOpenInDesktopOptionForSyncedFiles <Boolean>] [-ShowPeoplePickerGroupSuggestionsForIB <Boolean>]
 [-EnableRestrictedAccessControl <Boolean>] [-BlockDownloadFileTypePolicy <Boolean>]
 [-BlockDownloadFileTypeIds <SPBlockDownloadFileTypeId[]>] [-ExcludedBlockDownloadGroupIds <Guid[]>]
 [-TlsTokenBindingPolicyValue <SPOTlsTokenBindingPolicyValue>] [-RecycleBinRetentionPeriod <Int32>]
 [-IsEnableAppAuthPopUpEnabled <Boolean>] [-IsDataAccessInCardDesignerEnabled <Boolean>]
 [-MassDeleteNotificationDisabled <Boolean>] [-EnableAutoExpirationVersionTrim <Boolean>]
 [-EnableMediaReactions <Boolean>] [-BusinessConnectivityServiceDisabled <Boolean>]
 [-ExpireVersionsAfterDays <Int32>] [-MajorVersionLimit <Int32>] [-AllowSensitivityLabelOnRecords <Boolean>]
 [-DelayDenyAddAndCustomizePagesEnforcement <Boolean>]
 [-DelayDenyAddAndCustomizePagesEnforcementOnClassicPublishingSites <Boolean>]
 [-AllowClassicPublishingSiteCreation <Boolean>] [-WhoCanShareAnonymousAllowList <Guid[]>]
 [-WhoCanShareAuthenticatedGuestAllowList <Guid[]>]
 [-ResyncContentSecurityPolicyConfigurationEntries <Boolean>] [-ContentSecurityPolicyEnforcement <Boolean>]
 [-DocumentUnderstandingModelScope <SyntexFeatureScopeValue>]
 [-DocumentUnderstandingModelSelectedSitesList <String[]>]
 [-DocumentUnderstandingModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AIBuilderModelScope <SyntexFeatureScopeValue>] [-AIBuilderModelSelectedSitesList <String[]>]
 [-AIBuilderModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AIBuilderModelSelectedSitesIncludesContentCenters <Boolean>] [-PrebuiltModelScope <SyntexFeatureScopeValue>]
 [-PrebuiltModelSelectedSitesList <String[]>]
 [-PrebuiltModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-DocumentTranslationScope <SyntexFeatureScopeValue>] [-DocumentTranslationSelectedSitesList <String[]>]
 [-DocumentTranslationSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AutofillColumnsScope <SyntexFeatureScopeValue>] [-AutofillColumnsSelectedSitesList <String[]>]
 [-AutofillColumnsSelectedSitesListOperation <SelectedSitesListOperations>]
 [-OpticalCharacterRecognitionScope <SyntexFeatureScopeValue>]
 [-OpticalCharacterRecognitionSelectedSitesList <String[]>]
 [-OpticalCharacterRecognitionSelectedSitesListOperation <SelectedSitesListOperations>]
 [-DefaultContentCenterSite <String>]
 [-AllowWebPropertyBagUpdateWhenDenyAddAndCustomizePagesIsEnabled <Boolean>] [-EnforceRequestDigest <Boolean>]
 [<CommonParameters>]
```

### ParamSetMultipleSites
```
Set-SPOTenant [-MinCompatibilityLevel <Int32>] [-MaxCompatibilityLevel <Int32>]
 [-ExternalServicesEnabled <Boolean>] [-NoAccessRedirectUrl <String>] [-ArchiveRedirectUrl <String>]
 [-SharingCapability <SharingCapabilities>] [-DisplayStartASiteOption <Boolean>] [-StartASiteFormUrl <String>]
 [-ShowEveryoneClaim <Boolean>] [-ShowAllUsersClaim <Boolean>]
 [-ShowEveryoneExceptExternalUsersClaim <Boolean>]
 [-AllowEveryoneExceptExternalUsersClaimInPrivateSite <Boolean>] [-SearchResolveExactEmailOrUPN <Boolean>]
 [-OfficeClientADALDisabled <Boolean>] [-LegacyAuthProtocolsEnabled <Boolean>]
 [-LegacyBrowserAuthProtocolsEnabled <Boolean>] [-DisableCustomAppAuthentication <Boolean>]
 [-IsSharePointAddInsDisabled <Boolean>] [-IsSharePointAddInsBlocked <Boolean>]
 [-DisableSharePointStoreAccess <Boolean>] [-SiteOwnerManageLegacyServicePrincipalEnabled <Boolean>]
 [-RequireAcceptingAccountMatchInvitedAccount <Boolean>] [-ProvisionSharedWithEveryoneFolder <Boolean>]
 [-SignInAccelerationDomain <String>] [-EnableGuestSignInAcceleration <Boolean>]
 [-UsePersistentCookiesForExplorerView <Boolean>] [-ReSyncTenantPrivacyProfile]
 [-BccExternalSharingInvitations <Boolean>] [-BccExternalSharingInvitationsList <String>]
 [-PublicCdnEnabled <Boolean>] [-PublicCdnAllowedFileTypes <String>]
 [-RequireAnonymousLinksExpireInDays <Int32>] [-SharingAllowedDomainList <String>]
 [-SharingBlockedDomainList <String>] [-SharingDomainRestrictionMode <SharingDomainRestrictionModes>]
 [-OneDriveStorageQuota <Int64>] [-OneDriveForGuestsEnabled <Boolean>] [-IPAddressEnforcement <Boolean>]
 [-IPAddressAllowList <String>] [-IPAddressWACTokenLifetime <Int32>]
 [-EnableTenantRestrictionsInsights <Boolean>] [-EnablePromotedFileHandlers <Boolean>]
 [-UseFindPeopleInPeoplePicker <Boolean>] [-DefaultSharingLinkType <SharingLinkType>]
 [-ODBMembersCanShare <SharingState>] [-ODBAccessRequests <SharingState>]
 [-PreventExternalUsersFromResharing <Boolean>] [-ShowPeoplePickerSuggestionsForGuestUsers <Boolean>]
 [-AppOnlyBypassPeoplePickerPolicies <Boolean>] [-EnableDiscoverableByOrganizationForVideos <Boolean>]
 [-FileAnonymousLinkType <AnonymousLinkType>] [-FolderAnonymousLinkType <AnonymousLinkType>]
 [-NotifyOwnersWhenItemsReshared <Boolean>] [-NotifyOwnersWhenInvitationsAccepted <Boolean>]
 [-NotificationsInOneDriveForBusinessEnabled <Boolean>] [-NotificationsInSharePointEnabled <Boolean>]
 [-SelfServiceSiteCreationDisabled <Boolean>]
 [-SpecialCharactersStateInFileFolderNames <SpecialCharactersState>] [-OwnerAnonymousNotification <Boolean>]
 [-CommentsOnSitePagesDisabled <Boolean>] [-CommentsOnFilesDisabled <Boolean>]
 [-CommentsOnListItemsDisabled <Boolean>] [-ViewersCanCommentOnMediaDisabled <Boolean>]
 [-SocialBarOnSitePagesDisabled <Boolean>] [-OrphanedPersonalSitesRetentionPeriod <Int32>]
 [-PermissiveBrowserFileHandlingOverride <Boolean>] [-DisallowInfectedFileDownload <Boolean>]
 [-DefaultLinkPermission <SharingPermissionType>] [-CustomizedExternalSharingServiceUrl <String>]
 [-ConditionalAccessPolicyErrorHelpLink <String>] [-RestrictedAccessControlforSitesErrorHelpLink <String>]
 [-SensitivityLabel <String>] [-RestrictedAccessControlForOneDriveErrorHelpLink <String>]
 [-ConditionalAccessPolicy <SPOConditionalAccessPolicyType>] [-AllowDownloadingNonWebViewableFiles <Boolean>]
 [-LimitedAccessFileType <SPOLimitedAccessFileType>] [-AllowEditing <Boolean>]
 [-ApplyAppEnforcedRestrictionsToAdHocRecipients <Boolean>] [-FilePickerExternalImageSearchEnabled <Boolean>]
 [-EmailAttestationRequired <Boolean>] [-EmailAttestationReAuthDays <Int32>]
 [-SyncPrivacyProfileProperties <Boolean>] [-DisabledWebPartIds <Guid[]>]
 [-DisabledAdaptiveCardExtensionIds <Guid[]>] [-EnableMinimumVersionRequirement <Boolean>]
 [-MarkNewFilesSensitiveByDefault <SensitiveByDefaultState>] [-EnableAIPIntegration <Boolean>]
 [-SyncAadB2BManagementPolicy <Boolean>] [-AllowCommentsTextOnEmailEnabled <Boolean>]
 [-EnableAzureADB2BIntegration <Boolean>] [-DisableAddShortcutsToOneDrive <Boolean>]
 [-IncludeAtAGlanceInShareEmails <Boolean>] [-DisableWorkflow2010 <Boolean>] [-EnableAutoNewsDigest <Boolean>]
 [-StopNew2010Workflows <Boolean>] [-StopNew2013Workflows <Boolean>] [-DisableBackToClassic <Boolean>]
 [-Sites <SpoSitePipeBind[]>] [-ExternalUserExpirationRequired <Boolean>] [-ExternalUserExpireInDays <Int32>]
 [-BlockDownloadLinksFileType <BlockDownloadLinksFileTypes>] [-AnyoneLinkTrackUsers <Boolean>]
 [-BlockAppAccessWithAuthenticationContext <Boolean>] [-OneDriveLoopDefaultSharingLinkScope <SharingScope>]
 [-OneDriveLoopDefaultSharingLinkRole <SharingRole>] [-OneDriveRequestFilesLinkEnabled <Boolean>]
 [-OneDriveRequestFilesLinkExpirationInDays <Int32>] [-OneDriveSharingCapability <SharingCapabilities>]
 [-OneDriveDefaultShareLinkScope <SharingScope>] [-OneDriveDefaultShareLinkRole <SharingRole>]
 [-OneDriveDefaultLinkToExistingAccess <Boolean>] [-OneDriveBlockGuestsAsSiteAdmin <SharingState>]
 [-CoreLoopDefaultSharingLinkScope <SharingScope>] [-CoreLoopDefaultSharingLinkRole <SharingRole>]
 [-CoreSharingCapability <SharingCapabilities>] [-AllowSharingOutsideRestrictedAccessControlGroups <Boolean>]
 [-CoreRequestFilesLinkEnabled <Boolean>] [-CoreRequestFilesLinkExpirationInDays <Int32>]
 [-CoreDefaultShareLinkScope <SharingScope>] [-CoreDefaultShareLinkRole <SharingRole>]
 [-CoreDefaultLinkToExistingAccess <Boolean>] [-CoreBlockGuestsAsSiteAdmin <SharingState>]
 [-AllowAnonymousMeetingParticipantsToAccessWhiteboards <SharingState>] [-Workflows2013Enabled <Boolean>]
 [-IsFluidEnabled <Boolean>] [-IsWBFluidEnabled <Boolean>] [-IsCollabMeetingNotesFluidEnabled <Boolean>]
 [-IsLoopEnabled <Boolean>] [-DisableDocumentLibraryDefaultLabeling <Boolean>]
 [-ExtendPermissionsToUnprotectedFiles <Boolean>] [-EnableSensitivityLabelForPDF <Boolean>]
 [-BlockSendLabelMismatchEmail <Boolean>] [-LabelMismatchEmailHelpLink <String>]
 [-BlockUserInfoVisibility <String>] [-BlockUserInfoVisibilityInOneDrive <TenantBrowseUserInfoPolicyValue>]
 [-BlockUserInfoVisibilityInSharePoint <TenantBrowseUserInfoPolicyValue>]
 [-AllowOverrideForBlockUserInfoVisibility <Boolean>] [-DisablePersonalListCreation <Boolean>]
 [-DisableSpacesActivation <Boolean>] [-DisableVivaConnectionsAnalytics <Boolean>]
 [-InformationBarriersSuspension <Boolean>] [-IBImplicitGroupBased <Boolean>]
 [-AppBypassInformationBarriers <Boolean>] [-AppAccessInformationBarriersAllowList <Guid[]>]
 [-AllOrganizationSecurityGroupId <Guid>] [-DisableModernListTemplateIds <Guid[]>]
 [-EnableModernListTemplateIds <Guid[]>] [-HideSyncButtonOnTeamSite <Boolean>]
 [-AllowGuestUserShareToUsersNotInSiteCollection <Boolean>] [-StreamLaunchConfig <Int32>]
 [-DelegateRestrictedContentDiscoverabilityManagement <Boolean>]
 [-DelegateRestrictedAccessControlManagement <Boolean>] [-DisableOutlookPSTVersionTrimming <Boolean>]
 [-MediaTranscription <MediaTranscriptionPolicyType>]
 [-MediaTranscriptionAutomaticFeatures <MediaTranscriptionAutomaticFeaturesPolicyType>]
 [-ViewInFileExplorerEnabled <Boolean>] [-AuthContextResilienceMode <SPResilienceModeType>]
 [-ReduceTempTokenLifetimeEnabled <Boolean>] [-ReduceTempTokenLifetimeValue <Int32>]
 [-ShowOpenInDesktopOptionForSyncedFiles <Boolean>] [-ShowPeoplePickerGroupSuggestionsForIB <Boolean>]
 [-EnableRestrictedAccessControl <Boolean>] [-BlockDownloadFileTypePolicy <Boolean>]
 [-BlockDownloadFileTypeIds <SPBlockDownloadFileTypeId[]>] [-ExcludedBlockDownloadGroupIds <Guid[]>]
 [-TlsTokenBindingPolicyValue <SPOTlsTokenBindingPolicyValue>] [-RecycleBinRetentionPeriod <Int32>]
 [-IsEnableAppAuthPopUpEnabled <Boolean>] [-IsDataAccessInCardDesignerEnabled <Boolean>]
 [-MassDeleteNotificationDisabled <Boolean>] [-EnableAutoExpirationVersionTrim <Boolean>]
 [-EnableMediaReactions <Boolean>] [-BusinessConnectivityServiceDisabled <Boolean>]
 [-ExpireVersionsAfterDays <Int32>] [-MajorVersionLimit <Int32>] [-AllowSensitivityLabelOnRecords <Boolean>]
 [-DelayDenyAddAndCustomizePagesEnforcement <Boolean>]
 [-DelayDenyAddAndCustomizePagesEnforcementOnClassicPublishingSites <Boolean>]
 [-AllowClassicPublishingSiteCreation <Boolean>] [-WhoCanShareAnonymousAllowList <Guid[]>]
 [-WhoCanShareAuthenticatedGuestAllowList <Guid[]>]
 [-ResyncContentSecurityPolicyConfigurationEntries <Boolean>] [-ContentSecurityPolicyEnforcement <Boolean>]
 [-DocumentUnderstandingModelScope <SyntexFeatureScopeValue>]
 [-DocumentUnderstandingModelSelectedSitesList <String[]>]
 [-DocumentUnderstandingModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AIBuilderModelScope <SyntexFeatureScopeValue>] [-AIBuilderModelSelectedSitesList <String[]>]
 [-AIBuilderModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AIBuilderModelSelectedSitesIncludesContentCenters <Boolean>] [-PrebuiltModelScope <SyntexFeatureScopeValue>]
 [-PrebuiltModelSelectedSitesList <String[]>]
 [-PrebuiltModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-DocumentTranslationScope <SyntexFeatureScopeValue>] [-DocumentTranslationSelectedSitesList <String[]>]
 [-DocumentTranslationSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AutofillColumnsScope <SyntexFeatureScopeValue>] [-AutofillColumnsSelectedSitesList <String[]>]
 [-AutofillColumnsSelectedSitesListOperation <SelectedSitesListOperations>]
 [-OpticalCharacterRecognitionScope <SyntexFeatureScopeValue>]
 [-OpticalCharacterRecognitionSelectedSitesList <String[]>]
 [-OpticalCharacterRecognitionSelectedSitesListOperation <SelectedSitesListOperations>]
 [-DefaultContentCenterSite <String>]
 [-AllowWebPropertyBagUpdateWhenDenyAddAndCustomizePagesIsEnabled <Boolean>] [-EnforceRequestDigest <Boolean>]
 [<CommonParameters>]
```

### InformationBarrier
```
Set-SPOTenant [-MinCompatibilityLevel <Int32>] [-MaxCompatibilityLevel <Int32>]
 [-ExternalServicesEnabled <Boolean>] [-NoAccessRedirectUrl <String>] [-ArchiveRedirectUrl <String>]
 [-SharingCapability <SharingCapabilities>] [-DisplayStartASiteOption <Boolean>] [-StartASiteFormUrl <String>]
 [-ShowEveryoneClaim <Boolean>] [-ShowAllUsersClaim <Boolean>]
 [-ShowEveryoneExceptExternalUsersClaim <Boolean>]
 [-AllowEveryoneExceptExternalUsersClaimInPrivateSite <Boolean>] [-SearchResolveExactEmailOrUPN <Boolean>]
 [-OfficeClientADALDisabled <Boolean>] [-LegacyAuthProtocolsEnabled <Boolean>]
 [-LegacyBrowserAuthProtocolsEnabled <Boolean>] [-DisableCustomAppAuthentication <Boolean>]
 [-IsSharePointAddInsDisabled <Boolean>] [-IsSharePointAddInsBlocked <Boolean>]
 [-DisableSharePointStoreAccess <Boolean>] [-SiteOwnerManageLegacyServicePrincipalEnabled <Boolean>]
 [-RequireAcceptingAccountMatchInvitedAccount <Boolean>] [-ProvisionSharedWithEveryoneFolder <Boolean>]
 [-SignInAccelerationDomain <String>] [-EnableGuestSignInAcceleration <Boolean>]
 [-UsePersistentCookiesForExplorerView <Boolean>] [-ReSyncTenantPrivacyProfile]
 [-BccExternalSharingInvitations <Boolean>] [-BccExternalSharingInvitationsList <String>]
 [-PublicCdnEnabled <Boolean>] [-PublicCdnAllowedFileTypes <String>]
 [-RequireAnonymousLinksExpireInDays <Int32>] [-SharingAllowedDomainList <String>]
 [-SharingBlockedDomainList <String>] [-SharingDomainRestrictionMode <SharingDomainRestrictionModes>]
 [-OneDriveStorageQuota <Int64>] [-OneDriveForGuestsEnabled <Boolean>] [-IPAddressEnforcement <Boolean>]
 [-IPAddressAllowList <String>] [-IPAddressWACTokenLifetime <Int32>]
 [-EnableTenantRestrictionsInsights <Boolean>] [-EnablePromotedFileHandlers <Boolean>]
 [-UseFindPeopleInPeoplePicker <Boolean>] [-DefaultSharingLinkType <SharingLinkType>]
 [-ODBMembersCanShare <SharingState>] [-ODBAccessRequests <SharingState>]
 [-PreventExternalUsersFromResharing <Boolean>] [-ShowPeoplePickerSuggestionsForGuestUsers <Boolean>]
 [-AppOnlyBypassPeoplePickerPolicies <Boolean>] [-EnableDiscoverableByOrganizationForVideos <Boolean>]
 [-FileAnonymousLinkType <AnonymousLinkType>] [-FolderAnonymousLinkType <AnonymousLinkType>]
 [-NotifyOwnersWhenItemsReshared <Boolean>] [-NotifyOwnersWhenInvitationsAccepted <Boolean>]
 [-NotificationsInOneDriveForBusinessEnabled <Boolean>] [-NotificationsInSharePointEnabled <Boolean>]
 [-SelfServiceSiteCreationDisabled <Boolean>]
 [-SpecialCharactersStateInFileFolderNames <SpecialCharactersState>] [-OwnerAnonymousNotification <Boolean>]
 [-CommentsOnSitePagesDisabled <Boolean>] [-CommentsOnFilesDisabled <Boolean>]
 [-CommentsOnListItemsDisabled <Boolean>] [-ViewersCanCommentOnMediaDisabled <Boolean>]
 [-SocialBarOnSitePagesDisabled <Boolean>] [-OrphanedPersonalSitesRetentionPeriod <Int32>]
 [-PermissiveBrowserFileHandlingOverride <Boolean>] [-DisallowInfectedFileDownload <Boolean>]
 [-DefaultLinkPermission <SharingPermissionType>] [-CustomizedExternalSharingServiceUrl <String>]
 [-ConditionalAccessPolicyErrorHelpLink <String>] [-RestrictedAccessControlforSitesErrorHelpLink <String>]
 [-RestrictedAccessControlForOneDriveErrorHelpLink <String>]
 [-ApplyAppEnforcedRestrictionsToAdHocRecipients <Boolean>] [-FilePickerExternalImageSearchEnabled <Boolean>]
 [-EmailAttestationRequired <Boolean>] [-EmailAttestationReAuthDays <Int32>]
 [-SyncPrivacyProfileProperties <Boolean>] [-DisabledWebPartIds <Guid[]>]
 [-DisabledAdaptiveCardExtensionIds <Guid[]>] [-EnableMinimumVersionRequirement <Boolean>]
 [-MarkNewFilesSensitiveByDefault <SensitiveByDefaultState>] [-EnableAIPIntegration <Boolean>]
 [-SyncAadB2BManagementPolicy <Boolean>] [-AllowCommentsTextOnEmailEnabled <Boolean>]
 [-EnableAzureADB2BIntegration <Boolean>] [-DisableAddShortcutsToOneDrive <Boolean>]
 [-IncludeAtAGlanceInShareEmails <Boolean>] [-DisableWorkflow2010 <Boolean>] [-EnableAutoNewsDigest <Boolean>]
 [-StopNew2010Workflows <Boolean>] [-StopNew2013Workflows <Boolean>] [-DisableBackToClassic <Boolean>]
 [-ExternalUserExpirationRequired <Boolean>] [-ExternalUserExpireInDays <Int32>]
 [-BlockDownloadLinksFileType <BlockDownloadLinksFileTypes>] [-AnyoneLinkTrackUsers <Boolean>]
 [-BlockAppAccessWithAuthenticationContext <Boolean>] [-OneDriveLoopDefaultSharingLinkScope <SharingScope>]
 [-OneDriveLoopDefaultSharingLinkRole <SharingRole>] [-OneDriveRequestFilesLinkEnabled <Boolean>]
 [-OneDriveRequestFilesLinkExpirationInDays <Int32>] [-OneDriveSharingCapability <SharingCapabilities>]
 [-OneDriveDefaultShareLinkScope <SharingScope>] [-OneDriveDefaultShareLinkRole <SharingRole>]
 [-OneDriveDefaultLinkToExistingAccess <Boolean>] [-OneDriveBlockGuestsAsSiteAdmin <SharingState>]
 [-CoreLoopDefaultSharingLinkScope <SharingScope>] [-CoreLoopDefaultSharingLinkRole <SharingRole>]
 [-CoreSharingCapability <SharingCapabilities>] [-AllowSharingOutsideRestrictedAccessControlGroups <Boolean>]
 [-CoreRequestFilesLinkEnabled <Boolean>] [-CoreRequestFilesLinkExpirationInDays <Int32>]
 [-CoreDefaultShareLinkScope <SharingScope>] [-CoreDefaultShareLinkRole <SharingRole>]
 [-CoreDefaultLinkToExistingAccess <Boolean>] [-CoreBlockGuestsAsSiteAdmin <SharingState>]
 [-AllowAnonymousMeetingParticipantsToAccessWhiteboards <SharingState>] [-Workflows2013Enabled <Boolean>]
 [-IsFluidEnabled <Boolean>] [-IsWBFluidEnabled <Boolean>] [-IsCollabMeetingNotesFluidEnabled <Boolean>]
 [-IsLoopEnabled <Boolean>] [-DisableDocumentLibraryDefaultLabeling <Boolean>]
 [-ExtendPermissionsToUnprotectedFiles <Boolean>] [-EnableSensitivityLabelForPDF <Boolean>]
 [-BlockSendLabelMismatchEmail <Boolean>] [-LabelMismatchEmailHelpLink <String>]
 [-BlockUserInfoVisibility <String>] [-BlockUserInfoVisibilityInOneDrive <TenantBrowseUserInfoPolicyValue>]
 [-BlockUserInfoVisibilityInSharePoint <TenantBrowseUserInfoPolicyValue>]
 [-AllowOverrideForBlockUserInfoVisibility <Boolean>] [-DisablePersonalListCreation <Boolean>]
 [-DisableSpacesActivation <Boolean>] [-DisableVivaConnectionsAnalytics <Boolean>]
 [-InformationBarriersSuspension <Boolean>] [-IBImplicitGroupBased <Boolean>]
 [-AppBypassInformationBarriers <Boolean>] [-DefaultOneDriveInformationBarrierMode <String>]
 [-AppAccessInformationBarriersAllowList <Guid[]>] [-AllOrganizationSecurityGroupId <Guid>]
 [-DisableModernListTemplateIds <Guid[]>] [-EnableModernListTemplateIds <Guid[]>]
 [-HideSyncButtonOnTeamSite <Boolean>] [-AllowGuestUserShareToUsersNotInSiteCollection <Boolean>]
 [-StreamLaunchConfig <Int32>] [-DelegateRestrictedContentDiscoverabilityManagement <Boolean>]
 [-DelegateRestrictedAccessControlManagement <Boolean>] [-DisableOutlookPSTVersionTrimming <Boolean>]
 [-MediaTranscription <MediaTranscriptionPolicyType>]
 [-MediaTranscriptionAutomaticFeatures <MediaTranscriptionAutomaticFeaturesPolicyType>]
 [-ViewInFileExplorerEnabled <Boolean>] [-AuthContextResilienceMode <SPResilienceModeType>]
 [-ReduceTempTokenLifetimeEnabled <Boolean>] [-ReduceTempTokenLifetimeValue <Int32>]
 [-ShowOpenInDesktopOptionForSyncedFiles <Boolean>] [-ShowPeoplePickerGroupSuggestionsForIB <Boolean>]
 [-EnableRestrictedAccessControl <Boolean>] [-BlockDownloadFileTypePolicy <Boolean>]
 [-BlockDownloadFileTypeIds <SPBlockDownloadFileTypeId[]>] [-ExcludedBlockDownloadGroupIds <Guid[]>]
 [-TlsTokenBindingPolicyValue <SPOTlsTokenBindingPolicyValue>] [-RecycleBinRetentionPeriod <Int32>]
 [-IsEnableAppAuthPopUpEnabled <Boolean>] [-IsDataAccessInCardDesignerEnabled <Boolean>]
 [-MassDeleteNotificationDisabled <Boolean>] [-EnableAutoExpirationVersionTrim <Boolean>]
 [-EnableMediaReactions <Boolean>] [-BusinessConnectivityServiceDisabled <Boolean>]
 [-ExpireVersionsAfterDays <Int32>] [-MajorVersionLimit <Int32>] [-AllowSensitivityLabelOnRecords <Boolean>]
 [-DelayDenyAddAndCustomizePagesEnforcement <Boolean>]
 [-DelayDenyAddAndCustomizePagesEnforcementOnClassicPublishingSites <Boolean>]
 [-AllowClassicPublishingSiteCreation <Boolean>] [-WhoCanShareAnonymousAllowList <Guid[]>]
 [-WhoCanShareAuthenticatedGuestAllowList <Guid[]>]
 [-ResyncContentSecurityPolicyConfigurationEntries <Boolean>] [-ContentSecurityPolicyEnforcement <Boolean>]
 [-DocumentUnderstandingModelScope <SyntexFeatureScopeValue>]
 [-DocumentUnderstandingModelSelectedSitesList <String[]>]
 [-DocumentUnderstandingModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AIBuilderModelScope <SyntexFeatureScopeValue>] [-AIBuilderModelSelectedSitesList <String[]>]
 [-AIBuilderModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AIBuilderModelSelectedSitesIncludesContentCenters <Boolean>] [-PrebuiltModelScope <SyntexFeatureScopeValue>]
 [-PrebuiltModelSelectedSitesList <String[]>]
 [-PrebuiltModelSelectedSitesListOperation <SelectedSitesListOperations>]
 [-DocumentTranslationScope <SyntexFeatureScopeValue>] [-DocumentTranslationSelectedSitesList <String[]>]
 [-DocumentTranslationSelectedSitesListOperation <SelectedSitesListOperations>]
 [-AutofillColumnsScope <SyntexFeatureScopeValue>] [-AutofillColumnsSelectedSitesList <String[]>]
 [-AutofillColumnsSelectedSitesListOperation <SelectedSitesListOperations>]
 [-OpticalCharacterRecognitionScope <SyntexFeatureScopeValue>]
 [-OpticalCharacterRecognitionSelectedSitesList <String[]>]
 [-OpticalCharacterRecognitionSelectedSitesListOperation <SelectedSitesListOperations>]
 [-DefaultContentCenterSite <String>]
 [-AllowWebPropertyBagUpdateWhenDenyAddAndCustomizePagesIsEnabled <Boolean>] [-EnforceRequestDigest <Boolean>]
 [<CommonParameters>]
```

## DESCRIPTION

You can use the `Set-SPOTenant` cmdlet to enable external services and to specify the versions in which site collections can be created.
You can also use the `Set-SPOSite` cmdlet together with the `Set-SPOTenant` cmdlet to block access to a site in your organization and redirect traffic to another site.

You must be a SharePoint Online administrator to run the cmdlet.

## EXAMPLES

### EXAMPLE 1

```powershell
Set-SPOSite -Identity https://contoso.sharepoint.com/sites/team1 -LockState NoAccess
Set-SPOTenant -NoAccessRedirectUrl 'https://www.contoso.com'
```

This example blocks access to <https://contoso.sharepoint.com/sites/team1> and redirects traffic to <https://www.contoso.com.>

### EXAMPLE 2

```powershell
Set-SPOTenant -ShowEveryoneExceptExternalUsersClaim $false
```

This example hides the "Everyone Except External Users" claim in People Picker.

### EXAMPLE 3

```powershell
Set-SPOTenant -ShowAllUsersClaim $false
```

This example hides the "All Users" claim group in People Picker.

### EXAMPLE 4

```powershell
Set-SPOTenant -UsePersistentCookiesForExplorerView $true
```

This example enables the use of special persisted cookie for Open with Explorer.

### EXAMPLE 5

```powershell
Set-SPOTenant -LegacyAuthProtocolsEnabled $True
```

This example enables legacy authentication protocols on the tenant. This can help to enable login in situations where the admin users get an error like "Cannot contact web site '<https://contoso-admin.sharepoint.com/'> or the web site does not support SharePoint Online credentials. The response status code is 'Unauthorized'.", and the underlying error is "Access denied. Before opening files in this location, you must first browse to the web site and select the option to login automatically."

### EXAMPLE 6

```powershell
Set-SPOTenant -ContentTypeSyncSiteTemplatesList MySites
```

This example enables Content Type Hub to push content types to all OneDrive for Business sites. There is no change in Content Type Publishing behavior for other sites.

### EXAMPLE 7

```powershell
Set-SPOTenant -ContentTypeSyncSiteTemplatesList MySites -ExcludeSiteTemplate
```

This example stops publishing content types to OneDrive for Business sites.

### EXAMPLE 8

```powershell
Set-SPOTenant -SearchResolveExactEmailOrUPN $true
```

This example disables starts with for all users/partial name search functionality for all SharePoint users, except SharePoint Admins.

### EXAMPLE 9

```powershell
Set-SPOTenant -UseFindPeopleInPeoplePicker $true
```

This example enables tenant admins to enable ODB and SPO to respect Exchange supports Address Book Policy (ABP) policies in the people picker.

### EXAMPLE 10

```powershell
Set-SPOTenant -ShowPeoplePickerSuggestionsForGuestUsers $true
```

This example enables the option to search for existing guest users at Tenant Level.

### EXAMPLE 11

```powershell
Set-SPOTenant -EnableAutoExpirationVersionTrim $true
```

This example sets automatic version history limits on all new document libraries at tenant level.

### EXAMPLE 12

```powershell
Set-SPOTenant -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -ExpireVersionsAfterDays 30
```

This example sets manual version history limits on all new document libraries at tenant level by limiting the number of major versions and the time (in days) versions are kept.

### EXAMPLE 13

```powershell
Set-SPOTenant -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -ExpireVersionsAfterDays 0
```

This example sets manual version history limits on all new document libraries at tenant level by limiting the number of major versions with no time limits.

### EXAMPLE 14

```powershell
Set-SPOTenant -SharingDomainRestrictionMode "AllowList" -SharingAllowedDomainList "contoso.com fabrikam.com"
```

This example enables users to share with external collaborators from those domains only.

### EXAMPLE 15

```powershell
Set-SPOTenant -SharingDomainRestrictionMode "BlockList" -SharingBlockedDomainList "contoso.com"
```

This example enables users to share with all external collaborators except for those on the BlockedDomainList.

### EXAMPLE 16

```powershell
Set-SPOTenant -EnableVersionExpirationSetting $true
```
The `EnableVersionExpirationSetting` parameter is no longer active, this feature is now automatically enabled for each tenant. Setting `EnableVersionExpirationSetting` to false would not disable the feature.
[Learn more about Version History Settings](/sharepoint/document-library-version-history-limits)

### EXAMPLE 17

```powershell
Set-SPOTenant -PrebuiltModelScope SelectedSites -PrebuiltModelSelectedSitesList "https://contoso.sharepoint.com/sites/site1","https://contoso.sharepoint.com/sites/site2" -PrebuiltModelSelectedSitesListOperation Append
```

This example sets the scope of the prebuilt model and [prebuilt document processing](/microsoft-365/syntex/prebuilt-overview) premium feature to `SelectedSites`, which limits the feature to only sites included in the selected sites list. This example also appends two sites to the feature's selected sites list.

Use of these parameters require the tenant to either have the required license or pay-as-you-go billing set up. For more information, visit [Licensing for Microsoft Syntex](/microsoft-365/syntex/syntex-licensing).

### EXAMPLE 18

```powershell
Set-SPOTenant -DefaultContentCenterSite "https://contoso.sharepoint.com/sites/contentcenter"
```

This example sets the tenant's default content center. It can only be used if the tenant does not already have a designated default content center. To learn more about content centers, visit [Create a content center in Microsoft Syntex](/microsoft-365/syntex/create-a-content-center).

Use of this parameter requires the tenant to either have the required license or pay-as-you-go billing set up. For more information, visit [Licensing for Microsoft Syntex](/microsoft-365/syntex/syntex-licensing).

### EXAMPLE 19

```powershell
$list = (Get-SPOTenant | Select-Object WhoCanShareAnonymousAllowList).WhoCanShareAnonymousAllowList
Set-SPOTenant –WhoCanShareAnonymousAllowList ($list + <new GUID>)
```

This example appends a security group to the WhoCanShareAnonymousAllowList. Similar code works for the WhoCanShareAuthenticatedGuestAllowList.

### EXAMPLE 20

```powershell
Set-SPOTenant –WhoCanShareAnonymousAllowList @()
```

This example empties the WhoCanShareAnonymousAllowList. Similar code works for the WhoCanShareAuthenticatedGuestAllowList.

### EXAMPLE 21
```powershell
Set-SPOTenant -DisabledAdaptiveCardExtensionIds 0d2d0fd0-9489-47ef-acfb-90edca009cba
```

This example disables the Power Apps Adaptive Card Extension.

## PARAMETERS

### -AllOrganizationSecurityGroupId

> Applicable: SharePoint Online

Sets the All-Organization Security Group by object ID. This group is then used for other features, such as "EnableDiscoverableByOrganizationForVideos", if enabled. If you change the group ID associated with the All-Organization Security Group, it will only be effective on new shares or permission events.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowAnonymousMeetingParticipantsToAccessWhiteboards
{{ Fill AllowAnonymousMeetingParticipantsToAccessWhiteboards Description }}

```yaml
Type: Microsoft.SharePoint.Client.SharingState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowClassicPublishingSiteCreation

> Applicable: SharePoint Online

This parameter allows creation of classic publishing site collections (templates BLANKINTERNETCONTAINER#0, CMSPUBLISHING#0 and BLANKINTERNET#0) and activation of classic publishing features in sites.

The valid values are:

* False (default) - Classic publishing site collections cannot be created and the publishing features cannot be activated in sites.
* True - Classic publishing site collections can be created and the publishing features can be activated in sites.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowCommentsTextOnEmailEnabled

> Applicable: SharePoint Online

When this parameter is true, the email notification that a user receives when is mentioned, includes the surrounding document context. Set it to false to disable this feature.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowDownloadingNonWebViewableFiles

> Applicable: SharePoint Online

This parameter has been deprecated.

```yaml
Type: Boolean
Parameter Sets: (All)
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

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: ParamSetMultipleSites
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowEveryoneExceptExternalUsersClaimInPrivateSite

> Applicable: SharePoint Online

When this parameter is true, the "Everyone except external users" claim is available in the People Picker of a private site. Set it to false to disable this feature.

The valid values are:

- True - The "Everyone except external users" claim is available in People Picker of a private site.
- False (default) - The "Everyone except external users" claim is not available in People Picker of a private site.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowGuestUserShareToUsersNotInSiteCollection

> Applicable: SharePoint Online

The AllowGuestUserShareToUsersNotInSiteCollection settings (defaulted to false) will allow guests to share to users not in the site.

The valid values are:

- False (default) – Guest users will only be able to share to users that exist within the current site.
- True – Guest users will be able to find user accounts in the directory by typing in the exact email address match.

Note: When the value is set to True, you will also need to enable [SharePoint and OneDrive integration with Microsoft Entra B2B](/sharepoint/sharepoint-azureb2b-integration) for the functionality to work.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowOverrideForBlockUserInfoVisibility

> Applicable: SharePoint Online

Allow organization level policy for Block User Info Visibility to be overridden for a SharePoint site or OneDrive. Use Set-SPOSite to override the policy for a SharePoint site or OneDrive.

The valid values are:

- False (default) – Do not allow the Block User Info Visibility policy to be overridden for a SharePoint site or OneDrive.

- True – Allow the Block User Info Visibility policy to be overridden for a SharePoint site or OneDrive.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowSensitivityLabelOnRecords

> Applicable: SharePoint Online

Allow Records to have sensitivity labels applied.

The valid values are:

- False (default) – Do not allow the the application of sensitivity labels to records.

- True – Allow the application of sensitivity labels to records.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowSharingOutsideRestrictedAccessControlGroups
{{ Fill AllowSharingOutsideRestrictedAccessControlGroups Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
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
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AnyoneLinkTrackUsers
{{ Fill AnyoneLinkTrackUsers Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppAccessInformationBarriersAllowList
{{ Fill AppAccessInformationBarriersAllowList Description }}

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppBypassInformationBarriers
{{ Fill AppBypassInformationBarriers Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyAppEnforcedRestrictionsToAdHocRecipients

> Applicable: SharePoint Online

When the feature is enabled, all guest users are subject to conditional access policy. By default guest users who are accessing SharePoint Online files with pass code are exempt from the conditional access policy.

The valid values are:

- False (default) - Guest access users are exempt from conditional access policy.
- True - Conditional access policy is also applied to guest users.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppOnlyBypassPeoplePickerPolicies
{{ Fill AppOnlyBypassPeoplePickerPolicies Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArchiveRedirectUrl
{{ Fill ArchiveRedirectUrl Description }}

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

### -AuthContextResilienceMode
{{ Fill AuthContextResilienceMode Description }}

```yaml
Type: Microsoft.SharePoint.Administration.SPResilienceModeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutofillColumnsScope
{{ Fill AutofillColumnsScope Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SyntexFeatureScopeValue
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutofillColumnsSelectedSitesList
{{ Fill AutofillColumnsSelectedSitesList Description }}

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutofillColumnsSelectedSitesListOperation
{{ Fill AutofillColumnsSelectedSitesListOperation Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SelectedSitesListOperations
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BccExternalSharingInvitations

> Applicable: SharePoint Online

When the feature is enabled, all external sharing invitations that are sent will blind copy the e-mail messages listed in the BccExternalSharingsInvitationList.

The valid values are:

- False (default) - BCC for external sharing is disabled.
- True - All external sharing invitations that are sent will blind copy the e-mail messages listed in the BccExternalSharingsInvitationList.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BccExternalSharingInvitationsList

> Applicable: SharePoint Online

Specifies a list of e-mail addresses to be BCC'd when the BCC for External Sharing feature is enabled.
Multiple addresses can be specified by creating a comma separated list with no spaces.

The valid values are:

- "" (default) - Blank by default, this will also clear any value that has been set.
- Single or Multiple e-mail addresses - joe@contoso.com or joe@contoso.com,bob@contoso.com

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

### -BlockAppAccessWithAuthenticationContext
{{ Fill BlockAppAccessWithAuthenticationContext Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockDownloadFileTypeIds
{{ Fill BlockDownloadFileTypeIds Description }}

```yaml
Type: Microsoft.SharePoint.Client.Administration.SPBlockDownloadFileTypeId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockDownloadFileTypePolicy
{{ Fill BlockDownloadFileTypePolicy Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
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

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.BlockDownloadLinksFileTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockSendLabelMismatchEmail

> Applicable: SharePoint Online

When a sensitivity label mismatch occurs between the label on the document uploaded and the label on the site, SharePoint Online captures an audit record, and sends an Incompatible sensitivity label detected email notification to the person who uploaded the document and the site owner. The notification contains details of the document which caused the problem and the label assigned to the document and to the site. The comparison happens between the priority of these two labels.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockUserInfoVisibility

> Applicable: SharePoint Online

This feature has not yet been rolled out to Production. Attempting to set this parameter before rollout is complete will result in an error message. More details on this feature will be available on release.

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

### -BlockUserInfoVisibilityInOneDrive

> Applicable: SharePoint Online

Blocks users from accessing User Info if they have Limited Access permission only to the OneDrive. The policy applies to all OneDrives in the organization.

The valid values are:

- ApplyToNoUsers – No users are prevented from accessing User Info when they have Limited Access permission only.

- ApplyToAllUsers – All users (internal or external) are prevented from accessing User Info if they have Limited Access permission only.

- ApplyToGuestAndExternalUsers (default) – Only external or guest users are prevented from accessing User Info if they have Limited Access permission only.

- ApplyToInternalUsers – Only internal users are prevented from accessing User Info if they have Limited Access permission only.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.TenantBrowseUserInfoPolicyValue
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockUserInfoVisibilityInSharePoint

> Applicable: SharePoint Online

Blocks users from accessing User Info if they have Limited Access permission only to a SharePoint site. The policy applies to all SharePoint sites in the organization.

The valid values are:
- ApplyToNoUsers (default) – No users are prevented from accessing User Info when they have Limited Access permission only to a SharePoint site.
- ApplyToAllUsers – All users (internal or external) are prevented from accessing User Info if they have Limited Access permission only to a SharePoint site.
- ApplyToGuestAndExternalUsers – Only external or guest users are prevented from accessing User Info if they have Limited Access permission only to a SharePoint site.
- ApplyToInternalUsers – Only internal users are prevented from accessing User Info if they have Limited Access permission only to a SharePoint site.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.TenantBrowseUserInfoPolicyValue
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BusinessConnectivityServiceDisabled

> Applicable: SharePoint Online
Prevents access to features that depend on the Business Connectivity Service (BCS), including external lists, external columns, and external content types.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommentsOnFilesDisabled

> Applicable: SharePoint Online

Disables or enables commenting functionality on the files.
PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommentsOnListItemsDisabled

> Applicable: SharePoint Online

Disables or enables commenting functionality on list items.
PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommentsOnSitePagesDisabled

> Applicable: SharePoint Online

Disables or enables commenting functionality on the site pages.
PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionalAccessPolicy

> Applicable: SharePoint Online

Please read [Control access from unmanaged devices](/sharepoint/control-access-from-unmanaged-devices ) documentation here to understand Conditional Access Policy usage in SharePoint Online.

PARAMVALUE: AllowFullAccess | AllowLimitedAccess | BlockAccess

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SPOConditionalAccessPolicyType
Parameter Sets: ParamSetMultipleSites
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionalAccessPolicyErrorHelpLink

> Applicable: SharePoint Online

A Link for help when Conditional Access Policy blocks a user. This should be in a valid URL format. A valid URL format that begins with https:// or https://.

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

### -ContentSecurityPolicyEnforcement
{{ Fill ContentSecurityPolicyEnforcement Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentTypeSyncSiteTemplatesList

By default Content Type Hub will no longer push content types to OneDrive for Business sites (formerly known as MySites).

In case you want the Content Type Hub to push content types to OneDrive for Business sites, use: `Set-SPOTenant -ContentTypeSyncSiteTemplatesList MySites`.

When the feature is enabled, the Content Type Hub will push content types to OneDrive for Business sites.

Once you have enabled Content Type publishing to OneDrive for Business sites, you can disable it later using: `Set-SPOTenant -ContentTypeSyncSiteTemplatesList MySites -ExcludeSiteTemplate`.

```yaml
Type: System.String[]
Parameter Sets: ParameterSetContentTypeSyncSiteTemplatesList
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreBlockGuestsAsSiteAdmin
{{ Fill CoreBlockGuestsAsSiteAdmin Description }}

```yaml
Type: Microsoft.SharePoint.Client.SharingState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreDefaultLinkToExistingAccess
{{ Fill CoreDefaultLinkToExistingAccess Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreDefaultShareLinkRole
{{ Fill CoreDefaultShareLinkRole Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreDefaultShareLinkScope
{{ Fill CoreDefaultShareLinkScope Description }}

```yaml
Type: Microsoft.SharePoint.Client.Sharing.SharingScope
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreLoopDefaultSharingLinkRole

> Applicable: SharePoint Online

This parameter sets the default share link role for Loop and Whiteboard files on SharePoint sites.

The valid values are:

- Edit
- View
- None
- Review
- RestrictedView

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreLoopDefaultSharingLinkScope

> Applicable: SharePoint Online

This parameter sets the default share link scope for Loop and Whiteboard files on SharePoint sites.

The valid values are:

- Anyone
- Organization
- SpecificPeople
- Uninitialized

```yaml
Type: Microsoft.SharePoint.Client.Sharing.SharingScope
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreRequestFilesLinkEnabled
{{ Fill CoreRequestFilesLinkEnabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreRequestFilesLinkExpirationInDays
{{ Fill CoreRequestFilesLinkExpirationInDays Description }}

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreSharingCapability
{{ Fill CoreSharingCapability Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingCapabilities
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomizedExternalSharingServiceUrl

> Applicable: SharePoint Online

Specifies a URL that will be appended to the error message that is surfaced when a user is blocked from sharing externally by policy. This URL can be used to direct users to internal portals to request help or to inform them about your organization's policies. An example value is "<https://www.contoso.com/sharingpolicies".>

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

### -DefaultContentCenterSite
{{ Fill DefaultContentCenterSite Description }}

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

### -DefaultLinkPermission

> Applicable: SharePoint Online

Lets administrators choose the default permission of the link in the sharing dialog box in OneDrive for Business and SharePoint Online. This applies to anonymous access, internal and direct links.

The valid values are View and Edit (default).

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingPermissionType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultOneDriveInformationBarrierMode
{{ Fill DefaultOneDriveInformationBarrierMode Description }}

```yaml
Type: System.String
Parameter Sets: InformationBarrier
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultSharingLinkType

> Applicable: SharePoint Online

Lets administrators choose the default link type in the sharing dialog box in OneDrive for Business and SharePoint Online.

For additional information about how to change the default link type, see Change the default link type when users get links for sharing.

> [!NOTE]
> Setting this value to "none" will default "get a link" to the most permissive link available (that is, if anonymous links are enabled, the default link will be anonymous access; if they are disabled then the default link will be internal.

The valid values are:

- None - Respect the organization default sharing link type
- Direct - Sets the default sharing link for this site to the Specific people link
- Internal - Sets the default sharing link for this site to the organization link or company shareable link
- AnonymousAccess - Sets the default sharing link for this site to an Anonymous Access or Anyone link

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingLinkType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DelayDenyAddAndCustomizePagesEnforcement
{{ Fill DelayDenyAddAndCustomizePagesEnforcement Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DelayDenyAddAndCustomizePagesEnforcementOnClassicPublishingSites
{{ Fill DelayDenyAddAndCustomizePagesEnforcementOnClassicPublishingSites Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DelegateRestrictedAccessControlManagement

> Applicable: SharePoint Online

Allows SharePoint administrators to delegate the management of Restricted access control policy on sites to site admins and owners.

The valid values are:
- True - Allow site admins and owners to manage Restricted access control policy
- False (default) - Do not allow site admins and owners to manage Restricted access control policy

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DelegateRestrictedContentDiscoverabilityManagement

> Applicable: SharePoint Online

Allows SharePoint administrators to delegate the management of Restricted content discoverability policy on sites to site admins and owners.

The valid values are:
- True - Allow site admins and owners to manage Restricted content discoverability policy
- False (default) - Do not allow site admins and owners to manage Restricted content discoverability policy

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAddShortcutsToOneDrive

> Applicable: SharePoint Online

When the feature is disabled ($true), the option [Add shortcut to My files](https://support.microsoft.com/office/add-shortcuts-to-shared-folders-in-onedrive-for-work-or-school-d66b1347-99b7-4470-9360-ffc048d35a33) will be removed; any folders that have already been added will remain on the user's computer.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableBackToClassic
{{ Fill DisableBackToClassic Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableCustomAppAuthentication

> Applicable: SharePoint Online

Prevents apps using an Azure Access Control (ACS) app-only access token to access SharePoint. ACS, a service of Microsoft Entra ID, has been retired on November 7, 2018. This retirement does not impact the SharePoint add-in model, which uses the https://accounts.accesscontrol.windows.net hostname (which is not impacted by this retirement). For new tenants, apps using an ACS app-only access token are disabled by default. We recommend using the Microsoft Entra app-only model which is modern and more secure. Note that marking this property to $true doesn't prevent creating apps in SharePoint that use an Azure Access Control (ACS) app-only access token. Marking this property to $true only ensures that such apps can't access SharePoint anymore.

Accepts a value of true or false. By default this feature is set to true.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisabledAdaptiveCardExtensionIds

> Applicable: SharePoint Online

Allows administrators to prevent certain Adaptive Card Extensions from being added to pages or rendering on pages on which they were previously added. Currently, only the following Adaptive Card Extensions can be disabled in such a manner:

| Adaptive Card Extension Name | GUID |
|---|---|
| Power Apps | 0d2d0fd0-9489-47ef-acfb-90edca009cba |

To disable a specific Adaptive Card Extension, you need to enter its GUID as the parameter. To view a list of disabled Adaptive Card Extensions, use [Get-SPOTenant](Get-SPOTenant.md) to get `DisabledAdaptiveCardExtensionIds`.

To re-enable some disabled Adaptive Card Extensions, use the `Set-SPOTenant` with the `-DisabledAdaptiveCardExtensionIds` parameter and corresponding GUIDs that you still want to keep disabling. To re-enable all disabled Adaptive Card Extensions, use `Set-SPOTenant -DisabledAdaptiveCardExtensionIds @()`.

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableDocumentLibraryDefaultLabeling

> Applicable: SharePoint Online

This switch allows tenant admins to disable the capability of configuring a default sensitivity label for a document library.

PARAMVALUE: True | False

> [!NOTE]
> When set to $true, users aren't able to apply a default sensitivity label for a document library. The default value is false.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisabledWebPartIds

> Applicable: SharePoint Online

Allows administrators to prevent certain web parts from being added to pages or rendering on pages on which they were previously added. Currently, only the following web parts can be disabled in such a manner:

- Amazon Kindle: 46698648-fcd5-41fc-9526-c7f7b2ace919
- YouTube: 544dd15b-cf3c-441b-96da-004d5a8cea1d
- Twitter: f6fdf4f8-4a24-437b-a127-32e66a5dd9b4
- Embed: 490d7c76-1824-45b2-9de3-676421c997fa
- Microsoft Bookings: d24a7165-c455-4d43-8bc8-fedb04d6c1b5
- Stream: 275c0095-a77e-4f6d-a2a0-6a7626911518

To disable a specific web part, you need to enter its GUID as the parameter. You can enter multiple GUIDs by using a comma to separate them, for example Set-SPOTenant -DisabledWebPartIds 46698648-fcd5-41fc-9526-c7f7b2ace919,544dd15b-cf3c-441b-96da-004d5a8cea1d. To view a list of disabled web parts, use Get-SPOTenant to get DisabledWebPartIds.

To re-enable some disabled web parts, use the Set-SPOTenant with the -DisabledWebPartIds parameter and corresponding GUIDs that you still want to keep disabling. To re-enable all disabled web parts, use Set-SPOTenant -DisabledWebPartIds @().

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableModernListTemplateIds
{{ Fill DisableModernListTemplateIds Description }}

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableOutlookPSTVersionTrimming

> Applicable: SharePoint Online

This parameter has no effect and it was used to opt-out of PST files retention policy changes as communicated in MC256835 (May 2021).
Starting August 16, 2021, the service started retaining 30 days worth of versions for any PST files stored in OneDrive for Business and SharePoint Online team site document libraries. This change was introduced to prevent cases of previous versions of PST files quickly consuming available storage. The change only impacts previous versions of PST files stored in your document library storage. As a best practice, PST files should not be uploaded on OneDrive for Business and SharePoint Online team site document libraries due to the impact on storage and network bandwidth.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePersonalListCreation
{{ Fill DisablePersonalListCreation Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSharePointStoreAccess

> Applicable: SharePoint Online

This feature allows the SharePoint Administrators to disable SharePoint Store access for all users in the tenant.

Accepts a value of true (enabled) to hide the SharePoint app store or false (disabled) to show the SharePoint app store. By default this feature is set to false.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSpacesActivation
{{ Fill DisableSpacesActivation Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableVivaConnectionsAnalytics
{{ Fill DisableVivaConnectionsAnalytics Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWorkflow2010
{{ Fill DisableWorkflow2010 Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisallowInfectedFileDownload

> Applicable: SharePoint Online

Prevents the Download button from being displayed on the Virus Found warning page.

Accepts a value of true (enabled) to hide the Download button or false (disabled) to display the Download button. By default this feature is set to false.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayStartASiteOption

> Applicable: SharePoint Online

Determines whether tenant users see the Start a Site menu option.

The valid values are:

- True (default) - Tenant users will see the Start a Site menu option.
- False - Start a Site is hidden from the menu.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DocumentTranslationScope
{{ Fill DocumentTranslationScope Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SyntexFeatureScopeValue
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DocumentTranslationSelectedSitesList
{{ Fill DocumentTranslationSelectedSitesList Description }}

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DocumentTranslationSelectedSitesListOperation
{{ Fill DocumentTranslationSelectedSitesListOperation Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SelectedSitesListOperations
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DocumentUnderstandingModelScope
{{ Fill DocumentUnderstandingModelScope Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SyntexFeatureScopeValue
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DocumentUnderstandingModelSelectedSitesList
{{ Fill DocumentUnderstandingModelSelectedSitesList Description }}

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DocumentUnderstandingModelSelectedSitesListOperation
{{ Fill DocumentUnderstandingModelSelectedSitesListOperation Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SelectedSitesListOperations
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailAttestationReAuthDays

> Applicable: SharePoint Online

Sets the number of days for email attestation re-authentication. Value can be from 1 to 365 days.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailAttestationRequired

> Applicable: SharePoint Online

Sets email attestation to required.

If people who use a verification code select to "stay signed in" in the browser, they must prove that they can access the same account that they used to redeem the sharing invitation. You can set the number of days for email attestation with **-EmailAttestationReAuthDays**. This setting affects only ad-hoc external recipients.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAIPIntegration

> Applicable: SharePoint Online

This parameter enables SharePoint to process the content of files stored in SharePoint and OneDrive with sensitivity labels that include encryption. For more information, see [Enable sensitivity labels for Office files in SharePoint and OneDrive](/microsoft-365/compliance/sensitivity-labels-sharepoint-onedrive-files).

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
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
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoNewsDigest

> Applicable: SharePoint Online

Enable or disable auto news digest. [Documentation](https://aka.ms/autonewsdigest) for auto news digest.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAzureADB2BIntegration

> Applicable: SharePoint Online

Enables OneDrive and SharePoint integration with Microsoft Entra B2B. For more information, see [SharePoint and OneDrive integration with Microsoft Entra B2B](/sharepoint/sharepoint-azureb2b-integration).

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDiscoverableByOrganizationForVideos
{{ Fill EnableDiscoverableByOrganizationForVideos Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableGuestSignInAcceleration

> Applicable: SharePoint Online

Accelerates guest-enabled site collections as well as member-only site collections when the SignInAccelerationDomain parameter is set.

> [!NOTE]
> If enabled, your identity provider must be capable of authenticating guest users. If it is not, guest users will be unable to log in and access content that was shared with them.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableMediaReactions
{{ Fill EnableMediaReactions Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableMinimumVersionRequirement

> Applicable: SharePoint Online

This parameter was used to opt-out of the versioning setting update. It has no effect as of today as versioning setting has already been rolled out.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableModernListTemplateIds
{{ Fill EnableModernListTemplateIds Description }}

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnablePromotedFileHandlers

> Applicable: SharePoint Online

This parameter is reserved for Microsoft internal use.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableRestrictedAccessControl
{{ Fill EnableRestrictedAccessControl Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSensitivityLabelforPDF

> Applicable: SharePoint Online

Allows tenant admins to turn on support for PDFs with sensitivity labels for the following scenarios:

- Applying a sensitivity label in Office for the web.
- Uploading a labeled document, and then extracting and displaying that sensitivity label.
- Search, eDiscovery, and data loss prevention.
- Auto-labeling policies and default sensitivity labels for SharePoint document libraries.

The valid values are:

- True - Enables support for PDFs.
- False (default) - Disables support for PDFs.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableTenantRestrictionsInsights
{{ Fill EnableTenantRestrictionsInsights Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnforceRequestDigest
{{ Fill EnforceRequestDigest Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
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
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeSiteTemplate

Excludes the specified template from Content Type hub content type synchronization. Must be used with `-ContentTypeSyncSiteTemplatesList [String[]]`.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetContentTypeSyncSiteTemplatesList
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
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendPermissionsToUnprotectedFiles
{{ Fill ExtendPermissionsToUnprotectedFiles Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalServicesEnabled

> Applicable: SharePoint Online

Enables external services for a tenant.
External services are defined as services that are not in the Office 365 datacenters.

The valid values are:

- True (default) - External services are enabled for the tenant.
- False - External services that are outside of the Office 365 datacenters cannot interact with SharePoint.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalUserExpirationRequired

> Applicable: SharePoint Online

Specifies whether to enable the external user expiration policy, where external users will be expired and removed from the site collection in a given number of days.

Note: Once the policy is enabled, expiration values will be set on external users as they join a site collection (via sharing links or via direct access). When the policy is disabled, it will no longer set expiration values on users, but it will not automatically clear expiration values set on existing users. The users can then have their expiration value cleared by a site collection administrator if required.

The valid values are:
True - Enables the Policy.
False (default) - Disables the policy.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalUserExpireInDays

> Applicable: SharePoint Online

Specifies the number of days before an external user will expire and be removed from the site collection if the policy is enabled. Value can be from 30 to 730 days.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileAnonymousLinkType

> Applicable: SharePoint Online

Anonymous access links can allow recipients to only view or view and edit. The value can be set separately for folders and files.

The valid values are:

- View
- Edit

```yaml
Type: Microsoft.SharePoint.Client.AnonymousLinkType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePickerExternalImageSearchEnabled

> Applicable: SharePoint Online

For Webparts that support inserting images, like for example Image or Hero webpart, the Web search (Powered by Bing) option will be available if enabled (the default).

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FolderAnonymousLinkType

> Applicable: SharePoint Online

Users can configure folder anonymous access links that allow recipients to view, view and upload, or view, edit, and upload files.

The valid values are:

- View
- ViewUpload
- Edit

```yaml
Type: Microsoft.SharePoint.Client.AnonymousLinkType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HideSyncButtonOnTeamSite
{{ Fill HideSyncButtonOnTeamSite Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IBImplicitGroupBased
{{ Fill IBImplicitGroupBased Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeAtAGlanceInShareEmails

> Applicable: SharePoint Online

Enable or disable the At A Glance feature in sharing e-mails. This provides the key points and time to read for the shared item if available.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationBarriersSuspension
{{ Fill InformationBarriersSuspension Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressAllowList

> Applicable: SharePoint Online

Configures multiple IP addresses or IP address ranges (IPv4 or IPv6), that are recognized as trusted.

Use commas to separate multiple IP addresses or IP address ranges. Verify there are no overlapping IP addresses and ensure IP ranges use Classless Inter-Domain Routing (CIDR) notation. For example, 172.16.0.0, 192.168.1.0/27.

> [!NOTE]
> The IPAddressAllowList parameter only lets administrators set IP addresses or ranges that are recognized as trusted. To only grant access from these IP addresses or ranges, set the IPAddressEnforcement parameter to $true.

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

### -IPAddressEnforcement

> Applicable: SharePoint Online

Allows access from network locations that are defined by an administrator.

The values are $true and $false. The default value is $false which means the setting is disabled.

Before the IPAddressEnforcement parameter is set, make sure you add a valid IPv4 or IPv6 address to the IPAddressAllowList parameter.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressWACTokenLifetime

> Applicable: SharePoint Online

Allows to set the session timeout. If you are a tenant administrator and you begin IP address enforcement for OneDrive for Business in Office 365, this enforcement automatically activates a tenant parameter IPAddressWACTokenLifetime. The default value is 15 minutes, when IP Address Enforcement is True.

PARAMVALUE: Int32

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsCollabMeetingNotesFluidEnabled
{{ Fill IsCollabMeetingNotesFluidEnabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsDataAccessInCardDesignerEnabled
{{ Fill IsDataAccessInCardDesignerEnabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsEnableAppAuthPopUpEnabled
{{ Fill IsEnableAppAuthPopUpEnabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsFluidEnabled
{{ Fill IsFluidEnabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsLoopEnabled
{{ Fill IsLoopEnabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsSharePointAddInsBlocked

> Applicable: SharePoint Online

When this feature is enabled, all functionalities of the add-ins will be restricted, preventing them from running or installing.

The valid values are:

- False (default) - All the add-ins features are supported.
- True - All the add-ins features will be blocked.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsSharePointAddInsDisabled

> Applicable: SharePoint Online

When the feature is enabled, all the add-ins features will be disabled.

The valid values are:

- False (default) - All the add-ins features are supported.
- True - All the add-ins features will be disabled.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsWBFluidEnabled

> Applicable: SharePoint Online

Sets whether Whiteboard is enabled or disabled for OneDrive for Business users. Whiteboard on OneDrive for Business is automatically enabled for applicable Microsoft 365 tenants but can be disabled.

The valid values are:

- $true - Administrator enabled Whiteboard for user with OneDrive for Business Users.
- $false - Administrator disable Whiteboard for user with OneDrive for Business Users.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LabelMismatchEmailHelpLink

> Applicable: SharePoint Online

This parameter allows tenant admins to customize the "Help Link" in email with the subject "Incompatible sensitivity label detected." When a sensitivity label mismatch occurs between the label on the document uploaded and the label on the site, SharePoint Online captures an audit record and sends an Incompatible sensitivity label detected email notification to the person who uploaded the document and the site owner. The notification contains details of the document which caused the problem and the label assigned to the document and to the site. The comparison happens between the priority of these two labels.

The value can be any valid URL.

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

### -LegacyAuthProtocolsEnabled

> Applicable: SharePoint Online

By default this value is set to $True, which means that authentication using legacy protocols is enabled.

Setting this parameter to $False prevents Office clients using non-modern authentication protocols from accessing SharePoint Online resources.

- True - Enables Office clients using non-modern authentication protocols (such as, Forms-Based Authentication (FBA) or Identity Client Runtime Library (IDCRL)) to access SharePoint resources.
- False - Prevents Office clients using non-modern authentication protocols from accessing SharePoint Online resources.

> [!NOTE]
> • This may also prevent third-party apps from accessing SharePoint Online resources. <br/> Also, this will also block apps using the SharePointOnlineCredentials class to access SharePoint Online resources. For additional information about SharePointOnlineCredentials, see SharePointOnlineCredentials class. <br/><br/>• The change is not instant. It might take up to 24 hours to be applied.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyBrowserAuthProtocolsEnabled
{{ Fill LegacyBrowserAuthProtocolsEnabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitedAccessFileType

> Applicable: SharePoint Online

Allows users to preview only Office files in the browser. This option increases security, but may be a barrier to user productivity.

The following parameters can be used with `-ConditionalAccessPolicy AllowLimitedAccess` for both the organization-wide setting and the site-level setting.

- OfficeOnlineFilesOnly: Allows users to preview only Office files in the browser. This option increases security but may be a barrier to user productivity.
- LimitedAccessFileType WebPreviewableFiles (default): Allows users to preview Office files in the browser. This option optimizes for user productivity but offers less security for files that aren't Office files. **Warning:** This option is known to cause problems with PDF and image file types because they can be required to be downloaded to the end user's machine to render in the browser. Plan the use of this control carefully. Otherwise, your users could be faced with unexpected "Access Denied" errors.
- LimitedAccessFileType OtherFiles: Allows users to download files that can't be previewed, such as .zip and .exe. This option offers less security.

PARAMVALUE: OfficeOnlineFilesOnly | WebPreviewableFiles | OtherFiles

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SPOLimitedAccessFileType
Parameter Sets: ParamSetMultipleSites
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorVersionLimit
{{ Fill MajorVersionLimit Description }}

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MarkNewFilesSensitiveByDefault

> Applicable: SharePoint Online

If external sharing is turned on, sensitive content could be shared and accessed by guests before the Office DLP rule finishes processing, you can address this issue by configuring this parameter.

Possible values are

- BlockExternalSharing: Prevents guests from accessing newly added files until at least one Office DLP policy scans the content of the file.
- AllowExternalSharing: Disables this feature.

For more information see [Mark new files as sensitive by default](/sharepoint/sensitive-by-default).

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SensitiveByDefaultState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MassDeleteNotificationDisabled
{{ Fill MassDeleteNotificationDisabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCompatibilityLevel

> Applicable: SharePoint Online

The only valid value is "15".

```yaml
Type: System.Int32
Parameter Sets: (All)
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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaTranscriptionAutomaticFeatures

> Applicable: SharePoint Online

When the feature is enabled, videos can have transcripts generated automatically on upload. The policy is default on. If a tenant admin decides to disable the feature, he can do so by disabling the policy at tenant level. This feature can not be enabled or disabled at site level.
Possible values:

- Enabled
- Disabled

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.MediaTranscriptionAutomaticFeaturesPolicyType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinCompatibilityLevel

> Applicable: SharePoint Online

The only valid value is "15".

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoAccessRedirectUrl

> Applicable: SharePoint Online

Specifies the URL of the redirected site for those site collections which have the locked state "NoAccess."

The valid values are:

- "" (default) - Blank by default, this will also remove or clear any value that has been set.
- Full URL - Example: <https://contoso.sharepoint.com/Pages/Locked.aspx>

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

### -NotificationsInOneDriveForBusinessEnabled

> Applicable: SharePoint Online

Enables or disables notifications in OneDrive for Business.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotificationsInSharePointEnabled

> Applicable: SharePoint Online

Enables or disables notifications in SharePoint.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotifyOwnersWhenInvitationsAccepted

This parameter has been deprecated since SharePoint Online legacy invitation flow switched to Entra B2B invitation flow.

### -NotifyOwnersWhenItemsReshared

> Applicable: SharePoint Online

When this parameter is set to $true and another user re-shares a document from a user's OneDrive for Business, the OneDrive for Business owner is notified by e-mail.

For additional information about how to configure notifications for external sharing, see Configure notifications for external sharing for OneDrive for Business.

The valid values are $true and $false.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODBAccessRequests

> Applicable: SharePoint Online

Lets administrators set policy on access requests and requests to share in OneDrive for Business.

The valid values are:

- On - Users without permission to share can trigger sharing requests to the OneDrive for Business owner when they attempt to share. Also, users without permission to a file or folder can trigger access requests to the OneDrive for Business owner when they attempt to access an item they do not have permissions to.
- Off - Prevent access requests and requests to share on OneDrive for Business.
- Unspecified - Let each OneDrive for Business owner enable or disable access requests and requests to share on their OneDrive.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODBMembersCanShare

> Applicable: SharePoint Online

Lets administrators set policy on re-sharing behavior in OneDrive for Business.

The valid values are:

- On - Users with edit permissions can re-share.
- Off - Only OneDrive for Business owner can share. The value of ODBAccessRequests defines whether a request to share gets sent to the owner.
- Unspecified - Let each OneDrive for Business owner enable or disable re-sharing behavior on their OneDrive.

```yaml
Type: Microsoft.SharePoint.Client.SharingState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODBMembersCanShare
{{ Fill ODBMembersCanShare Description }}

```yaml
Type: Microsoft.SharePoint.Client.SharingState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OfficeClientADALDisabled

> Applicable: SharePoint Online

When set to true this will disable the ability to use Modern Authentication that leverages ADAL across the tenant.

The valid values are:

- False (default) - Modern Authentication is enabled/allowed.
- True - Modern Authentication via ADAL is disabled.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveBlockGuestsAsSiteAdmin
{{ Fill OneDriveBlockGuestsAsSiteAdmin Description }}

```yaml
Type: Microsoft.SharePoint.Client.SharingState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveDefaultLinkToExistingAccess
{{ Fill OneDriveDefaultLinkToExistingAccess Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveDefaultShareLinkRole
{{ Fill OneDriveDefaultShareLinkRole Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveDefaultShareLinkScope
{{ Fill OneDriveDefaultShareLinkScope Description }}

```yaml
Type: Microsoft.SharePoint.Client.Sharing.SharingScope
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveForGuestsEnabled

> Applicable: SharePoint Online

Lets OneDrive for Business creation for administrator managed guest users. Administrator managed Guest users use credentials in the resource tenant to access the resources.

The valid values are:

- $true - Administrator managed Guest users can be given OneDrives, provided needed licenses are assigned.
- $false - Administrator managed Guest users can't be given OneDrives as functionality is turned off.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveLoopDefaultSharingLinkRole

> Applicable: SharePoint Online

This parameter sets the default share link role for Loop and Whiteboard files on OneDrive sites.

The valid values are:

- Edit
- View
- None
- Review
- RestrictedView

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveLoopDefaultSharingLinkScope

> Applicable: SharePoint Online

Gets or sets default share link scope for Loop and Whiteboard files on OneDrive sites.

The valid values are:

- Anyone
- Organization
- SpecificPeople
- Uninitialized

```yaml
Type: Microsoft.SharePoint.Client.Sharing.SharingScope
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveRequestFilesLinkEnabled
{{ Fill OneDriveRequestFilesLinkEnabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveRequestFilesLinkExpirationInDays
{{ Fill OneDriveRequestFilesLinkExpirationInDays Description }}

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveSharingCapability
{{ Fill OneDriveSharingCapability Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingCapabilities
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveStorageQuota

> Applicable: SharePoint Online

Sets a default OneDrive for Business storage quota for the tenant. It will be used for new OneDrive for Business sites created.

A typical use will be to reduce the amount of storage associated with OneDrive for Business to a level below what the License entitles the users. For example, it could be used to set the quota to 10 gigabytes (GB) by default.

If value is set to 0, the parameter will have no effect.

If the value is set larger than the Maximum allowed OneDrive for Business quota, it will have no effect.

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrphanedPersonalSitesRetentionPeriod

> Applicable: SharePoint Online

Specifies the number of days after a user's Active Directory account is deleted that their OneDrive for Business content will be deleted.

The value range is in days, between 30 and 3650. The default value is 30.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SyntexFeatureScopeValue
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OwnerAnonymousNotification

> Applicable: SharePoint Online

Enables or disables owner anonymous notification. If enabled, an email notification will be sent to the OneDrive for Business owners when anonymous links are created or changed.

PARAMVALUE: True | False

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissiveBrowserFileHandlingOverride

> Applicable: SharePoint Online

Enables the Permissive browser file handling. By default, the browser file handling is set to Strict. The Strict setting adds headers that force the browser to download certain types of files. The forced download improves security by disallowing the automatic execution of Web content. When the setting is set to Permissive, no headers are added and certain types of files can be executed in the browser instead of download.

The valid values are:

- True - Enable the Permissive browser file handling setting.
- False - Keep the default Strict browser file handling setting.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SelectedSitesListOperations
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreventExternalUsersFromResharing

> Applicable: SharePoint Online

Prevents external users from resharing files, folders, and sites that they do not own.

PARAMVALUE: True | False

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProvisionSharedWithEveryoneFolder

> Applicable: SharePoint Online

Creates a Shared with Everyone folder in every user's new OneDrive for Business document library.

The valid values are:

- True (default) - The Shared with Everyone folder is created.
- False - No folder is created when the site and OneDrive for Business document library is created.

The default behavior of the Shared with Everyone folder changed in August 2015.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCdnAllowedFileTypes

> Applicable: SharePoint Online

Sets public CDN allowed file types, if the public CDN is enabled.

PARAMVALUE: String

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCdnEnabled

> Applicable: SharePoint Online

Enables or disables the public CDN.

PARAMVALUE: True | False

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SyntexFeatureScopeValue
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireAcceptingAccountMatchInvitedAccount

This parameter has been deprecated since SharePoint Online legacy invitation flow switched to Entra B2B invitation flow.

### -RequireAnonymousLinksExpireInDays

> Applicable: SharePoint Online

Specifies the upper bound for user-created anonymous link expiration periods. All links created after setting this policy will expire by the end of a period spanning the set number of days.

The value can be from 0 to 730 days.

To remove the expiration requirement, set the value to zero (0).

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireOrganizationLinksExpireInDays

> Applicable: SharePoint Online

Specifies the upper bound for user-created organization link expiration periods. All links created after setting this policy will expire by the end of a period spanning the set number of days.

The value can be from 7 to 730 days.

To remove the expiration requirement, set the value to zero (0).

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SelectedSitesListOperations
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReSyncTenantPrivacyProfile

> Applicable: SharePoint Online

The 'SyncPrivacyProfileProperties' parameter is obsolete and renamed ReSyncTenantPrivacyProfile.

This parameter enables the synchronization of privacy profile properties.

ReSyncTenantPrivacyProfile sets whether or not the synced tenant properties will be updated on the next request. The request will cause Microsoft Entra ID to grab the tenant's current display name (TenantDisplayName) and privacy profile URL (PrivacyProfileUrl).

Running 'Set-SPOTenant - ReSyncTenantPrivacyProfile' will force a sync from the Microsoft Entra privacy profile URL to SharePoint Online. The sync may take up to 24 hours to complete. Whenever SharePoint Online gets the privacy profile URL, it checks whether the last sync time is out of the sync time window. If it is, it syncs from Microsoft Entra ID to SharePoint Online.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchResolveExactEmailOrUPN

> Applicable: SharePoint Online

Removes the search capability from People Picker. Note, recently resolved names will still appear in the list until browser cache is cleared or expired. This also does not allow SharePoint users to search for security groups or SharePoint groups.

SharePoint Administrators will still be able to use starts with or partial name matching when enabled.

The valid values are:

- False (default) - Starts with / partial name search functionality is available.
- True - Disables starts with for all users/partial name search functionality for all SharePoint users, except SharePoint Admins.

```yaml
Type: System.Boolean
Parameter Sets: (All)
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

For additional information about how to restrict a domain sharing, see [Restricted Domains Sharing in Office 365 SharePoint Online and OneDrive for Business](https://support.office.com/en-US/article/Restricted-Domains-Sharing-in-Office-365-SharePoint-Online-and-OneDrive-for-Business-5d7589cd-0997-4a00-a2ba-2320ec49c4e9).

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

### -SharingBlockedDomainList

> Applicable: SharePoint Online

Specifies a list of email domains that are blocked or prohibited for sharing with the external collaborators. Use space character as the delimiter for entering multiple values. For example, "contoso.com fabrikam.com".

For additional information about how to restrict a domain sharing, see [Restricted Domains Sharing in Office 365 SharePoint Online and OneDrive for Business](https://support.office.com/en-US/article/Restricted-Domains-Sharing-in-Office-365-SharePoint-Online-and-OneDrive-for-Business-5d7589cd-0997-4a00-a2ba-2320ec49c4e9).

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecycleBinRetentionPeriod
{{ Fill RecycleBinRetentionPeriod Description }}

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReduceTempTokenLifetimeEnabled
{{ Fill ReduceTempTokenLifetimeEnabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReduceTempTokenLifetimeValue
{{ Fill ReduceTempTokenLifetimeValue Description }}

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireAcceptingAccountMatchInvitedAccount
Ensures that an external user can only accept an external sharing invitation with an account matching the invited email address.

The parameter accepts two values: True or False.

True-User must accept this invitation with bob@contoso.com.

False- When a document is shared with an external user, bob@contoso.com, it can be accepted by any user with access to the invitation link in the original e-mail.

Administrators who desire increased control over external collaborators should consider enabling this feature.

This only applies to new external users accepting new sharing invitations.

The resource owner must share with an organizational or Microsoft account or the external user will be unable to access the resource.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireAnonymousLinksExpireInDays
{{ Fill RequireAnonymousLinksExpireInDays Description }}

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictedAccessControlForOneDriveErrorHelpLink
{{ Fill RestrictedAccessControlForOneDriveErrorHelpLink Description }}

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

### -RestrictedAccessControlforSitesErrorHelpLink
{{ Fill RestrictedAccessControlforSitesErrorHelpLink Description }}

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

### -ResyncContentSecurityPolicyConfigurationEntries
{{ Fill ResyncContentSecurityPolicyConfigurationEntries Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReSyncTenantPrivacyProfile
{{ Fill ReSyncTenantPrivacyProfile Description }}

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchResolveExactEmailOrUPN
Removes the search capability from People Picker.

The valid values are:

* Recently resolved names will still appear in the list.
* False- Restores default search functionality.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SelfServiceSiteCreationDisabled
{{ Fill SelfServiceSiteCreationDisabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SensitivityLabel
{{ Fill SensitivityLabel Description }}

```yaml
Type: System.String
Parameter Sets: ParamSetMultipleSites
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
Type: System.String
Parameter Sets: (All)
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingCapability

> Applicable: SharePoint Online

Determines what level of sharing is available for OneDrive and SharePoint sites.

The valid values are:

- ExternalUserAndGuestSharing (default) - External user sharing (share by email) and guest link sharing are both enabled.
- Disabled - External user sharing (share by email) and guest link sharing are both disabled.
- ExternalUserSharingOnly - External user sharing (share by email) is enabled, but guest link sharing is disabled.
- ExistingExternalUserSharingOnly - Only guests already in your organization's directory.

For more information about sharing, see [Manage sharing settings](/sharepoint/turn-external-sharing-on-or-off) for your SharePoint online environment.

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingCapabilities
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingDomainRestrictionMode

> Applicable: SharePoint Online

Specifies the external sharing mode for domains.

The valid values are:

- None
- AllowList - Users will be able to share with external collaborators coming only from that email domain.
- BlockList - Users will be able to share with all external collaborators apart from the ones on the BlockedDomainList.

For additional information about how to restrict a domain sharing, see [Restricted Domains Sharing in Office 365 SharePoint Online and OneDrive for Business](https://support.office.com/en-US/article/Restricted-Domains-Sharing-in-Office-365-SharePoint-Online-and-OneDrive-for-Business-5d7589cd-0997-4a00-a2ba-2320ec49c4e9).

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingDomainRestrictionModes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowAllUsersClaim

> Applicable: SharePoint Online

Enables the administrator to hide the All Users claim groups in People Picker.

When users share an item with "All Users (x)", it is accessible to all organization members in the tenant's Microsoft Entra ID who have authenticated with via this method. When users share an item with "All Users (x)" it is accessible to all organization members in the tenant that used NTLM to authentication with SharePoint.

Note, the All Users (authenticated) group is equivalent to the Everyone claim, and shows as Everyone.
To change this, see -ShowEveryoneClaim.

The valid values are:

- True (default) - The All Users claim groups are displayed in People Picker.
- False - The All Users claim groups are hidden in People Picker.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowEveryoneClaim

> Applicable: SharePoint Online

Enables the administrator to hide the Everyone claim in the People Picker.
When users share an item with Everyone, it is accessible to all authenticated users in the tenant's Microsoft Entra ID, including any active external users who have previously accepted invitations.

Note, that some SharePoint system resources such as templates and pages are required to be shared to Everyone and this type of sharing does not expose any user data or metadata.

The valid values are:

- True - The Everyone claim group is displayed in People Picker. This has been the default for tenants older than March 2018
- False (default) - The Everyone claim group is hidden from the People Picker. This has become the new default for new tenants.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowEveryoneExceptExternalUsersClaim

> Applicable: SharePoint Online

Enables the administrator to hide the "Everyone except external users" claim in the People Picker.
When users share an item with "Everyone except external users", it is accessible to all organization members in the tenant's Microsoft Entra ID, but not to any users who have previously accepted invitations.

The valid values are:

- True (default) - The Everyone except external users is displayed in People Picker.
- False - The Everyone except external users claim is not visible in People Picker.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowOpenInDesktopOptionForSyncedFiles
{{ Fill ShowOpenInDesktopOptionForSyncedFiles Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowPeoplePickerGroupSuggestionsForIB
{{ Fill ShowPeoplePickerGroupSuggestionsForIB Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowPeoplePickerSuggestionsForGuestUsers

> Applicable: SharePoint Online

Shows people picker suggestions for guest users. To enable the option to search for existing guest users at Tenant Level, set this parameter to $true.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignInAccelerationDomain

> Applicable: SharePoint Online

Specifies the home realm discovery value to be sent to Microsoft Entra ID during the user sign-in process.

When the organization uses a third-party identity provider, this prevents the user from seeing the Microsoft Entra Home Realm Discovery web page and ensures the user only sees their company's Identity Provider's portal.
This value can also be used with Microsoft Entra ID P1 or P2 to customize the Microsoft Entra sign-in page.

Acceleration will not occur on site collections that are shared externally.

This value should be configured with the login domain that is used by your company (that is, example@contoso.com).

If your company has multiple third-party identity providers, configuring the sign-in acceleration value will break sign-in for your organization.

The valid values are:

- "" (default) - Blank by default, this will also remove or clear any value that has been set.
- Login Domain - For example: "contoso.com"

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

### -SiteOwnerManageLegacyServicePrincipalEnabled

> Applicable: SharePoint Online

Allows or disallows the site collection admins to manage the Azure Access Control (ACS) service principal.

When the value is set to false, the service principal can only be created or updated by the SharePoint tenant admin. If the value is set to true, both the SharePoint tenant admin and site collection admin will be able to create or update the service principal through SharePoint.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sites
{{ Fill Sites Description }}

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind[]
Parameter Sets: ParamSetMultipleSites
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SocialBarOnSitePagesDisabled

> Applicable: SharePoint Online

Disables or enables the Social Bar.

The Social Bar will appear on all modern SharePoint pages with the exception of the home page of a site. It will give users the ability to like a page, see the number of views, likes, and comments on a page, and see the people who have liked a page.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SpecialCharactersStateInFileFolderNames

> Applicable: SharePoint Online

Permits the use of special characters in file and folder names in SharePoint Online and OneDrive for Business document libraries.

> [!NOTE]
> The only two characters that can be managed at this time are the # and % characters.

The valid values are:

- NoPreference - Support for feature will be enabled by Microsoft on your Office 365 tenant.
- Allowed - Lets the # and % characters in file and folder names in SharePoint Online and OneDrive for Business document libraries.
- Disallowed - Disallows the # and % characters in file and folder names in SharePoint Online and OneDrive for Business document libraries.

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SpecialCharactersState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartASiteFormUrl

> Applicable: SharePoint Online

Specifies URL of the form to load in the Start a Site dialog.

The valid values are:

- "" (default) - Blank by default, this will also remove or clear any value that has been set.
- Full URL - Example: "<https://contoso.sharepoint.com/path/to/form">

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

### -StopNew2010Workflows

Prevents creation of new SharePoint 2010 classic workflows.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StopNew2013Workflows

Prevents creation of new SharePoint 2013 classic workflows.

PARAMVALUE: True | False

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StreamLaunchConfig
{{ Fill StreamLaunchConfig Description }}

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncAadB2BManagementPolicy
{{ Fill SyncAadB2BManagementPolicy Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncPrivacyProfileProperties
{{ Fill SyncPrivacyProfileProperties Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TlsTokenBindingPolicyValue
{{ Fill TlsTokenBindingPolicyValue Description }}

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SPOTlsTokenBindingPolicyValue
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseFindPeopleInPeoplePicker

> Applicable: SharePoint Online

This feature enables tenant admins to enable ODB and SPO to respect Exchange supports Address Book Policy (ABP) policies in the people picker.

PARAMVALUE: True | False

> [!NOTE]
> When set to $true, users aren't able to share with security groups or SharePoint groups.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -UsePersistentCookiesForExplorerView

> Applicable: SharePoint Online
> [!NOTE]
> This setting is not used anymore with Internet Explorer (IE) retired and the parameter would be removed soon. Users need to select "Yes" when prompted for "Stay signed in?" at the time of sign-in for "View in File Explorer" to work with Microsoft Edge.

Lets SharePoint issue a special cookie that will allow this feature to work even when "Keep Me Signed In" is not selected.

"Open with Explorer" requires persisted cookies to operate correctly.
When the user does not select "Keep Me Signed in" at the time of sign-in, "Open with Explorer" will fail.

This special cookie expires after 30 minutes and cannot be cleared by closing the browser or signing out of SharePoint Online.
To clear this cookie, the user must log out of their Windows session.

The valid values are:

- False (default) - No special cookie is generated and the normal Office 365 sign-in length/timing applies.
- True - Generates a special cookie that will allow "Open with Explorer" to function if the "Keep Me Signed In" box is not checked at sign-in.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ViewersCanCommentOnMediaDisabled
{{ Fill ViewersCanCommentOnMediaDisabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ViewInFileExplorerEnabled

Enables or disables the ability to use View in Explorer in Microsoft Edge (93) or above.

> [!NOTE]
> When the value is set the View In Explorer command will become visible in UX for all users using Edge browser version 93 or above however those users still need [ConfigureViewInFileExplorer](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) Edge policy enabled for the functionality to work.
>
> Minimum Module Version Required: 16.0.21610.12000

The valid values are:

- False (default) - Disables View In Explorer command to become visible in Edge.
- True - Enables View In Explorer command to become visible in Edge.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhoCanShareAnonymousAllowList
{{ Fill WhoCanShareAnonymousAllowList Description }}

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhoCanShareAuthenticatedGuestAllowList
{{ Fill WhoCanShareAuthenticatedGuestAllowList Description }}

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Workflows2013Enabled
{{ Fill Workflows2013Enabled Description }}

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

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

[Get-SPOSite](Get-SPOSite.md)

[Set-SPOSite](Set-SPOSite.md)
