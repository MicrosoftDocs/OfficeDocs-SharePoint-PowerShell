---
external help file: sharepointonline.xml
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

```powershell
Set-SPOTenant [-ApplyAppEnforcedRestrictionsToAdHocRecipients <Boolean>]
 [-BccExternalSharingInvitations <Boolean>]
 [-BccExternalSharingInvitationsList <String>]
 [-BlockDownloadLinksFileType <BlockDownloadLinksFileTypes>]
 [-BusinessConnectivityServiceDisabled <Boolean>]
 [-DisplayStartASiteOption <Boolean>]
 [-EnableAIPIntegration <Boolean>]
 [-EnableAutoNewsDigest <Boolean>]
 [-EnableMinimumVersionRequirement <Boolean>]
 [-EnablePromotedFileHandlers <Boolean>]
 [-ExternalServicesEnabled <Boolean>]
 [-MarkNewFilesSensitiveByDefault <SensitiveByDefaultState>]
 [-MaxCompatibilityLevel <Int32>]
 [-MinCompatibilityLevel <Int32>]
 [-NoAccessRedirectUrl <String>]
 [-OfficeClientADALDisabled <Boolean>]
 [-ProvisionSharedWithEveryoneFolder <Boolean>]
 [-RequireAcceptingAccountMatchInvitedAccount <Boolean>]
 [-SearchResolveExactEmailOrUPN <Boolean>]
 [-SharingCapability <SharingCapabilities>]
 [-ShowAllUsersClaim <Boolean>]
 [-ShowEveryoneClaim <Boolean>]
 [-ShowEveryoneExceptExternalUsersClaim <Boolean>]
 [-SignInAccelerationDomain <String>]
 [-StartASiteFormUrl <String>]
 [-UsePersistentCookiesForExplorerView <Boolean>]
 [-CommentsOnSitePagesDisabled <Boolean>]
 [-CommentsOnFilesDisabled <Boolean>]
 [-CommentsOnListItemsDisabled <Boolean>]
 [-SocialBarOnSitePagesDisabled <Boolean>]
 [-DefaultLinkPermission <SharingPermissionType>]
 [-DefaultSharingLinkType <SharingLinkType>]
 [-DisabledWebPartIds <Guid>]
 [-DisallowInfectedFileDownload <Boolean>]
 [-DisableAddShortcutsToOneDrive <Boolean>]
 [-EnableGuestSignInAcceleration <Boolean>]
 [-FileAnonymousLinkType <AnonymousLinkType>]
 [-FilePickerExternalImageSearchEnabled <Boolean>]
 [-FolderAnonymousLinkType <AnonymousLinkType>]
 [-IPAddressAllowList <String>]
 [-IPAddressEnforcement <Boolean>]
 [-IPAddressWACTokenLifetime <Int32>]
 [-LegacyAuthProtocolsEnabled <Boolean>]
 [-MediaTranscriptionAutomaticFeatures <MediaTranscriptionAutomaticFeaturesPolicyType>]
 [-MediaTranscription <MediaTranscriptionPolicyType>]
 [-NotificationsInOneDriveForBusinessEnabled <Boolean>]
 [-NotificationsInSharePointEnabled <Boolean>]
 [-NotifyOwnersWhenInvitationsAccepted <Boolean>]
 [-NotifyOwnersWhenItemsReshared <Boolean>]
 [-ODBAccessRequests <SharingState>]
 [-ODBMembersCanShare <SharingState>]
 [-OneDriveForGuestsEnabled <Boolean>]
 [-OneDriveStorageQuota <Int64>]
 [-IsWBFluidEnabled <Boolean>]
 [-OrphanedPersonalSitesRetentionPeriod <Int32>]
 [-OwnerAnonymousNotification <Boolean>]
 [-PermissiveBrowserFileHandlingOverride <Boolean>]
 [-PreventExternalUsersFromResharing <Boolean>]
 [-PublicCdnAllowedFileTypes <String>]
 [-PublicCdnEnabled <Boolean>]
 [-RequireAnonymousLinksExpireInDays <Int32>]
 [-SharingAllowedDomainList <String>]
 [-SharingBlockedDomainList <String>]
 [-SharingDomainRestrictionMode <SharingDomainRestrictionModes>]
 [-ShowPeoplePickerSuggestionsForGuestUsers <Boolean>]
 [-SpecialCharactersStateInFileFolderNames <SpecialCharactersState>]
 [-ReSyncTenantPrivacyProfile]
 [-UseFindPeopleInPeoplePicker <Boolean>]
 [-UserVoiceForFeedbackEnabled <Boolean>]
 [-ContentTypeSyncSiteTemplatesList [String[]]]
 [-ExcludeSiteTemplate]
 [-CustomizedExternalSharingServiceUrl <String>]
 [-ConditionalAccessPolicy <SPOConditionalAccessPolicyType>]
 [-ConditionalAccessPolicyErrorHelpLink <String>]
 [-LimitedAccessFileType <SPOLimitedAccessFileType>]
 [-AllowDownloadingNonWebViewableFiles <Boolean>]
 [-AllowCommentsTextOnEmailEnabled <Boolean>]
 [-AllowEditing <Boolean>]
 [-EnableAzureADB2BIntegration <Boolean>]
 [-ExternalUserExpirationRequired <Boolean>]
 [-ExternalUserExpireInDays <Int32>]
 [-EmailAttestationRequired <Boolean>]
 [-EmailAttestationReAuthDays <Int32>]
 [-BlockUserInfoVisibility]
 [-BlockUserInfoVisibilityInOneDrive]
 [-BlockUserInfoVisibilityInSharePoint]
 [-AllowOverrideForBlockUserInfoVisibility]
 [-IncludeAtAGlanceInShareEmails]
 [-StopNew2010Workflows <Boolean>]
 [-StopNew2013Workflows <Boolean>]
 [-BlockSendLabelMismatchEmail <Boolean>]
 [-DisableOutlookPSTVersionTrimming <Boolean>]
 [-ViewInFileExplorerEnabled <Boolean>]
 [-AllowGuestUserShareToUsersNotInSiteCollection <Boolean>]
 [-DisableCustomAppAuthentication <Boolean>]
 [-SiteOwnerManageLegacyServicePrincipalEnabled <Boolean>]
 [-ReduceTempTokenLifetimeEnabled <Boolean>]
 [-ReduceTempTokenLifetimeValue <Int32>]
 [-ShowPeoplePickerGroupSuggestionsForIB <Boolean>]
 [-InformationBarriersSuspension <Boolean>]
 [-IBImplicitGroupBased <Boolean>]
 [-DefaultOneDriveInformationBarrierMode <String>]
 [-ViewersCanCommentOnMediaDisabled <Boolean>]
 [-CoreSharingCapability <SharingCapabilities>]
 [-OneDriveRequestFilesLinkEnabled <Boolean>]
 [-CoreRequestFilesLinkEnabled <Boolean>]
 [-OneDriveRequestFilesLinkExpirationInDays <Int32>]
 [-CoreRequestFilesLinkExpirationInDays <Int32>]
 [-OneDriveLoopDefaultSharingLinkScope <String>]
 [-OneDriveLoopDefaultSharingLinkRole <String>]
 [-CoreLoopDefaultSharingLinkScope <String>]
 [-CoreLoopDefaultSharingLinkRole <String>]
 [-AllowAnonymousMeetingParticipantsToAccessWhiteboards <SharingState>]
 [-LabelMismatchEmailHelpLink <String>]
 [-DisableBackToClassic <Boolean>]
 [-IsEnableAppAuthPopUpEnabled <Boolean>]
 [-BlockDownloadFileTypePolicy <Boolean>]
 [-EnableAutoExpirationVersionTrim <Boolean>]
 [-MajorVersionLimit <int>]
 [-ExpireVersionsAfterDays <int>]
 [-MassDeleteNotificationDisabled <Boolean>]
 [-DisableDocumentLibraryDefaultLabeling <Boolean>]
 [-EnableSensitivityLabelforPDF <Boolean>]
 [<CommonParameters>]
```

## DESCRIPTION

You can use the `Set-SPOTenant` cmdlet to enable external services and to specify the versions in which site collections can be created.
You can also use the `Set-SPOSite` cmdlet together with the `Set-SPOTenant` cmdlet to block access to a site in your organization and redirect traffic to another site.

You must be a SharePoint Online administrator or Global Administrator to run the cmdlet.

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

This example sets Automatic Version Storage Limits on all new document libraries at Tenant Level.

### EXAMPLE 12

```powershell
Set-SPOTenant -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -ExpireVersionsAfterDays 30
```

This example sets Manual Version Storage Limits on all new document libraries at Tenant Level by limiting the number of major versions and the time (in days) versions are kept. 

### EXAMPLE 13

```powershell
Set-SPOTenant -EnableAutoExpirationVersionTrim $false -MajorVersionLimit 500 -ExpireVersionsAfterDays 0
```

This example sets Manual Version Storage Limits on all new document libraries at Tenant Level by limiting the number of major versions with no time limits.

### EXAMPLE 14

```powershell
PS > Set-SPOTenant -SharingDomainRestrictionMode "AllowList" -SharingAllowedDomainList "contoso.com fabrikam.com"
```

This example enables users to share with external collaborators from those domains only.

### EXAMPLE 15

```powershell
PS > Set-SPOTenant -SharingDomainRestrictionMode "BlockList" -SharingBlockedDomainList "contoso.com"
```

This example enables users to share with all external collaborators except for those on the BlockedDomainList.

## PARAMETERS

### -ApplyAppEnforcedRestrictionsToAdHocRecipients

When the feature is enabled, all guest users are subject to conditional access policy. By default guest users who are accessing SharePoint Online files with pass code are exempt from the conditional access policy.

The valid values are:  

- False (default) - Guest access users are exempt from conditional access policy.  
- True - Conditional access policy is also applied to guest users.

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

### -BccExternalSharingInvitations

When the feature is enabled, all external sharing invitations that are sent will blind copy the e-mail messages listed in the BccExternalSharingsInvitationList.

The valid values are:  

- False (default) - BCC for external sharing is disabled.  
- True - All external sharing invitations that are sent will blind copy the e-mail messages listed in the BccExternalSharingsInvitationList.

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

### -BccExternalSharingInvitationsList

Specifies a list of e-mail addresses to be BCC'd when the BCC for External Sharing feature is enabled.  
Multiple addresses can be specified by creating a comma separated list with no spaces.

The valid values are:  

- "" (default) - Blank by default, this will also clear any value that has been set.  
- Single or Multiple e-mail addresses - joe@contoso.com or joe@contoso.com,bob@contoso.com

```yaml
Type: String
Parameter Sets: (All)
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

### -BusinessConnectivityServiceDisabled
Prevents access to features that depend on the Business Connectivity Service (BCS), including external lists, external columns, and external content types.

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

### -DisplayStartASiteOption

Determines whether tenant users see the Start a Site menu option.

The valid values are:  

- True (default) - Tenant users will see the Start a Site menu option.  
- False - Start a Site is hidden from the menu.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAIPIntegration

This parameter enables SharePoint to process the content of files stored in SharePoint and OneDrive with sensitivity labels that include encryption. For more information, see [Enable sensitivity labels for Office files in SharePoint and OneDrive](/microsoft-365/compliance/sensitivity-labels-sharepoint-onedrive-files).

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

### -EnableMinimumVersionRequirement

This parameter was used to opt-out of the versioning setting update. It has no effect as of today as versioning setting has already been rolled out.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnablePromotedFileHandlers

This parameter is reserved for Microsoft internal use.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MarkNewFilesSensitiveByDefault

If external sharing is turned on, sensitive content could be shared and accessed by guests before the Office DLP rule finishes processing, you can address this issue by configuring this parameter.
Possible values are
- BlockExternalSharing: Prevents guests from accessing newly added files until at least one Office DLP policy scans the content of the file.
- AllowExternalSharing: Disables this feature.

For more information see [Mark new files as sensitive by default](https://learn.microsoft.com/sharepoint/sensitive-by-default).

```yaml
Type: SensitiveByDefaultState
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: AllowExternalSharing
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalServicesEnabled

Enables external services for a tenant.  
External services are defined as services that are not in the Office 365 datacenters.

The valid values are:  

- True (default) - External services are enabled for the tenant.  
- False - External services that are outside of the Office 365 datacenters cannot interact with SharePoint.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCompatibilityLevel

The only valid value is "15".

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

### -MinCompatibilityLevel

The only valid value is "15".

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

### -NoAccessRedirectUrl

Specifies the URL of the redirected site for those site collections which have the locked state "NoAccess."

The valid values are:  

- "" (default) - Blank by default, this will also remove or clear any value that has been set.  
- Full URL - Example: <https://contoso.sharepoint.com/Pages/Locked.aspx>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OfficeClientADALDisabled

When set to true this will disable the ability to use Modern Authentication that leverages ADAL across the tenant.

The valid values are:  

- False (default) - Modern Authentication is enabled/allowed.  
- True - Modern Authentication via ADAL is disabled.

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

### -ProvisionSharedWithEveryoneFolder

Creates a Shared with Everyone folder in every user's new OneDrive for Business document library.

The valid values are:  

- True (default) - The Shared with Everyone folder is created.  
- False - No folder is created when the site and OneDrive for Business document library is created.

The default behavior of the Shared with Everyone folder changed in August 2015.  
For additional information about the change, see [Provision the Shared with Everyone folder in OneDrive for Business](https://support.office.com/article/Provision-the-Shared-with-Everyone-folder-in-OneDrive-for-Business-6bb02c91-fd0b-42ba-9457-3921cb6dc5b2).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireAcceptingAccountMatchInvitedAccount

Ensures that an external user can only accept an external sharing invitation with an account matching the invited email address.

Administrators who desire increased control over external collaborators should consider enabling this feature.

Note, this only applies to new external users accepting new sharing invitations. Also, the resource owner must share with an organizational or Microsoft account or the external user will be unable to access the resource.

The valid values are:  

- False (default) - When a document is shared with an external user, bob@contoso.com, it can be accepted by any user with access to the invitation link in the original e-mail.  
- True - User must accept this invitation with bob@contoso.com.

> [!NOTE]
> If this functionality is turned off (value is False), it is possible for the external/guest users you invite to your Azure AD, to log in using their personal, non-work accounts either on purpose, or by accident (they might have a pre-existing, signed in session already active in the browser window they use to accept your invitation).
> [!NOTE]
> Even though setting the value is instant (if you first run **Set-SPOTenant -RequireAcceptingAccountMatchInvitedAccount $True**, and then **Get-SPOTenant -RequireAcceptingAccountMatchInvitedAccount**, True should be returned), the functionality isn't turned on immediately. It may take up to 24 hours to take effect.

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

### -SearchResolveExactEmailOrUPN

Removes the search capability from People Picker. Note, recently resolved names will still appear in the list until browser cache is cleared or expired. This also does not allow SharePoint users to search for security groups or SharePoint groups.

SharePoint Administrators will still be able to use starts with or partial name matching when enabled.

The valid values are:  

- False (default) - Starts with / partial name search functionality is available.  
- True - Disables starts with for all users/partial name search functionality for all SharePoint users, except SharePoint Admins.

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

### -SharingCapability

Determines what level of sharing is available for the site.

The valid values are:  

- ExternalUserAndGuestSharing (default) - External user sharing (share by email) and guest link sharing are both enabled.
- Disabled - External user sharing (share by email) and guest link sharing are both disabled.
- ExternalUserSharingOnly - External user sharing (share by email) is enabled, but guest link sharing is disabled.
- ExistingExternalUserSharingOnly - Only guests already in your organization's directory.

For more information about sharing, see [Manage sharing settings](/sharepoint/turn-external-sharing-on-or-off) for your SharePoint online environment.

```yaml
Type: SharingCapabilities
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: ExternalUserAndGuestSharing
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowAllUsersClaim

Enables the administrator to hide the All Users claim groups in People Picker.

When users share an item with "All Users (x)", it is accessible to all organization members in the tenant's Azure Active Directory who have authenticated with via this method. When users share an item with "All Users (x)" it is accessible to all organization members in the tenant that used NTLM to authentication with SharePoint.

Note, the All Users (authenticated) group is equivalent to the Everyone claim, and shows as Everyone.
To change this, see -ShowEveryoneClaim.

The valid values are:  

- True (default) - The All Users claim groups are displayed in People Picker.  
- False - The All Users claim groups are hidden in People Picker.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowEveryoneClaim

Enables the administrator to hide the Everyone claim in the People Picker.  
When users share an item with Everyone, it is accessible to all authenticated users in the tenant's Azure Active Directory, including any active external users who have previously accepted invitations.

Note, that some SharePoint system resources such as templates and pages are required to be shared to Everyone and this type of sharing does not expose any user data or metadata.

The valid values are:  

- True - The Everyone claim group is displayed in People Picker. This has been the default for tenants older than March 2018  
- False (default) - The Everyone claim group is hidden from the People Picker. This has become the new default for new tenants.

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

### -ShowEveryoneExceptExternalUsersClaim

Enables the administrator to hide the "Everyone except external users" claim in the People Picker.  
When users share an item with "Everyone except external users", it is accessible to all organization members in the tenant's Azure Active Directory, but not to any users who have previously accepted invitations.

The valid values are:  

- True (default) - The Everyone except external users is displayed in People Picker.  
- False - The Everyone except external users claim is not visible in People Picker.

```yaml
Type: Boolean

Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignInAccelerationDomain

Specifies the home realm discovery value to be sent to Azure Active Directory (AAD) during the user sign-in process.

When the organization uses a third-party identity provider, this prevents the user from seeing the Azure Active Directory Home Realm Discovery web page and ensures the user only sees their company's Identity Provider's portal.
This value can also be used with Azure Active Directory Premium to customize the Azure Active Directory login page.

Acceleration will not occur on site collections that are shared externally.

This value should be configured with the login domain that is used by your company (that is, example@contoso.com).

If your company has multiple third-party identity providers, configuring the sign-in acceleration value will break sign-in for your organization.

The valid values are:  

- "" (default) - Blank by default, this will also remove or clear any value that has been set.  
- Login Domain - For example: "contoso.com"

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartASiteFormUrl

Specifies URL of the form to load in the Start a Site dialog.

The valid values are:  

- "" (default) - Blank by default, this will also remove or clear any value that has been set.  
- Full URL - Example: "<https://contoso.sharepoint.com/path/to/form">

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePersistentCookiesForExplorerView
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

### -CommentsOnSitePagesDisabled

Disables or enables commenting functionality on the site pages.
PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommentsOnFilesDisabled

Disables or enables commenting functionality on the files.
PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommentsOnListItemsDisabled

Disables or enables commenting functionality on list items.
PARAMVALUE: $true | $false

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

### -SocialBarOnSitePagesDisabled

Disables or enables the Social Bar.

The Social Bar will appear on all modern SharePoint pages with the exception of the home page of a site. It will give users the ability to like a page, see the number of views, likes, and comments on a page, and see the people who have liked a page.

PARAMVALUE: $true | $false

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

### -DefaultLinkPermission

Lets administrators choose the default permission of the link in the sharing dialog box in OneDrive for Business and SharePoint Online. This applies to anonymous access, internal and direct links.

The valid values are View and Edit (default).

```yaml
Type: SharingPermissionType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: Edit
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultSharingLinkType

Lets administrators choose what type of link appears is selected in the "Get a link" sharing dialog box in OneDrive for Business and SharePoint Online.

For additional information about how to change the default link type, see Change the default link type when users get links for sharing.

> [!NOTE]
> Setting this value to "none" will default "get a link" to the most permissive link available (that is, if anonymous links are enabled, the default link will be anonymous access; if they are disabled then the default link will be internal.  

The valid values are:

- None - Respect the organization default sharing link type
- Direct - Sets the default sharing link for this site to the Specific people link
- Internal - Sets the default sharing link for this site to the organization link or company shareable link
- AnonymousAccess - Sets the default sharing link for this site to an Anonymous Access or Anyone link

```yaml
Type: SharingLinkType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisabledWebPartIds

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

### -DisallowInfectedFileDownload

Prevents the Download button from being displayed on the Virus Found warning page.

Accepts a value of true (enabled) to hide the Download button or false (disabled) to display the Download button. By default this feature is set to false.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableCustomAppAuthentication

Prevents apps using an Azure Access Control (ACS) app-only access token to access SharePoint. ACS, a service of Azure Active Directory (Azure AD), has been retired on November 7, 2018. This retirement does not impact the SharePoint add-in model, which uses the https://accounts.accesscontrol.windows.net hostname (which is not impacted by this retirement). For new tenants, apps using an ACS app-only access token are disabled by default. We recommend using the Azure AD app-only model which is modern and more secure. Note that marking this property to $true doesn't prevent creating apps in SharePoint that use an Azure Access Control (ACS) app-only access token. Marking this property to $true only ensures that such apps can't access SharePoint anymore.

Accepts a value of true or false. By default this feature is set to true.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteOwnerManageLegacyServicePrincipalEnabled

Allows or disallows the site collection admins to manage the Azure Access Control (ACS) service principal.

When the value is set to false, the service principal can only be created or updated by the SharePoint tenant admin. If the value is set to true, both the SharePoint tenant admin and site collection admin will be able to create or update the service principal through SharePoint.

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

### -EnableGuestSignInAcceleration

Accelerates guest-enabled site collections as well as member-only site collections when the SignInAccelerationDomain parameter is set.

> [!NOTE]
> If enabled, your identity provider must be capable of authenticating guest users. If it is not, guest users will be unable to log in and access content that was shared with them.  

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileAnonymousLinkType

Anonymous access links can allow recipients to only view or view and edit. The value can be set separately for folders and separately for files.

The valid values are:

- View
- Edit

```yaml
Type: AnonymousLinkType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePickerExternalImageSearchEnabled

For Webparts that support inserting images, like for example Image or Hero webpart, the Web search (Powered by Bing) option will be available if enabled (the default).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -FolderAnonymousLinkType

Anonymous access links can allow recipients to only view or view and edit.

The valid values are:

- View
- Edit

```yaml
Type: AnonymousLinkType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressAllowList

Configures multiple IP addresses or IP address ranges (IPv4 or IPv6), that are recognized as trusted.

Use commas to separate multiple IP addresses or IP address ranges. Verify there are no overlapping IP addresses and ensure IP ranges use Classless Inter-Domain Routing (CIDR) notation. For example, 172.16.0.0, 192.168.1.0/27.

> [!NOTE]
> The IPAddressAllowList parameter only lets administrators set IP addresses or ranges that are recognized as trusted. To only grant access from these IP addresses or ranges, set the IPAddressEnforcement parameter to $true.  

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressEnforcement

Allows access from network locations that are defined by an administrator.

The values are $true and $false. The default value is $false which means the setting is disabled.

Before the IPAddressEnforcement parameter is set, make sure you add a valid IPv4 or IPv6 address to the IPAddressAllowList parameter.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressWACTokenLifetime

Allows to set the session timeout. If you are a tenant administrator and you begin IP address enforcement for OneDrive for Business in Office 365, this enforcement automatically activates a tenant parameter IPAddressWACTokenLifetime. The default value is 15 minutes, when IP Address Enforcement is True.

PARAMVALUE: Int32

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

### -LegacyAuthProtocolsEnabled

By default this value is set to $True, which means that authentication using legacy protocols is enabled.

Setting this parameter to $False prevents Office clients using non-modern authentication protocols from accessing SharePoint Online resources.

- True - Enables Office clients using non-modern authentication protocols (such as, Forms-Based Authentication (FBA) or Identity Client Runtime Library (IDCRL)) to access SharePoint resources.
- False - Prevents Office clients using non-modern authentication protocols from accessing SharePoint Online resources.

> [!NOTE]
> • This may also prevent third-party apps from accessing SharePoint Online resources. <br/> Also, this will also block apps using the SharePointOnlineCredentials class to access SharePoint Online resources. For additional information about SharePointOnlineCredentials, see SharePointOnlineCredentials class. <br/><br/>• The change is not instant. It might take up to 24 hours to be applied.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaTranscription

When the feature is enabled, videos can have transcripts generated on demand or generated automatically in certain scenarios. This is the default because the policy is default on. If a video owner decides they don’t want the transcript, they can always hide or delete it from that video. 
Possible values:

- Enabled
- Disabled

```yaml
Type: MediaTranscriptionPolicyType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaTranscriptionAutomaticFeatures

When the feature is enabled, videos can have transcripts generated automatically on upload. The policy is default on. If a tenant admin decides to disable the feature, he can do so by disabling the policy at tenant level. This feature can not be enabled or disabled at site level.
Possible values:

- Enabled
- Disabled

```yaml
Type: MediaTranscriptionAutomaticFeaturesPolicyType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotificationsInOneDriveForBusinessEnabled

Enables or disables notifications in OneDrive for Business.

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotificationsInSharePointEnabled

Enables or disables notifications in SharePoint.

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotifyOwnersWhenInvitationsAccepted

When this parameter is set to $true and when an external user accepts an invitation to a resource in a user's OneDrive for Business, the OneDrive for Business owner is notified by e-mail.

For additional information about how to configure notifications for external sharing, see Configure notifications for external sharing for OneDrive for Business.

The valid values are $true and $false.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotifyOwnersWhenItemsReshared

When this parameter is set to $true and another user re-shares a document from a user's OneDrive for Business, the OneDrive for Business owner is notified by e-mail.

For additional information about how to configure notifications for external sharing, see Configure notifications for external sharing for OneDrive for Business.

The valid values are $true and $false.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODBAccessRequests

Lets administrators set policy on access requests and requests to share in OneDrive for Business.

The valid values are:

- On - Users without permission to share can trigger sharing requests to the OneDrive for Business owner when they attempt to share. Also, users without permission to a file or folder can trigger access requests to the OneDrive for Business owner when they attempt to access an item they do not have permissions to.
- Off - Prevent access requests and requests to share on OneDrive for Business.
- Unspecified - Let each OneDrive for Business owner enable or disable access requests and requests to share on their OneDrive.

```yaml
Type: SharingState
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODBMembersCanShare

Lets administrators set policy on re-sharing behavior in OneDrive for Business.

The valid values are:

- On - Users with edit permissions can re-share.
- Off - Only OneDrive for Business owner can share. The value of ODBAccessRequests defines whether a request to share gets sent to the owner.
- Unspecified - Let each OneDrive for Business owner enable or disable re-sharing behavior on their OneDrive.

```yaml
Type: SharingState
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveForGuestsEnabled

Lets OneDrive for Business creation for administrator managed guest users. Administrator managed Guest users use credentials in the resource tenant to access the resources.

The valid values are:

- $true - Administrator managed Guest users can be given OneDrives, provided needed licenses are assigned.
- $false - Administrator managed Guest users can't be given OneDrives as functionality is turned off.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveStorageQuota

Sets a default OneDrive for Business storage quota for the tenant. It will be used for new OneDrive for Business sites created.

A typical use will be to reduce the amount of storage associated with OneDrive for Business to a level below what the License entitles the users. For example, it could be used to set the quota to 10 gigabytes (GB) by default.

If value is set to 0, the parameter will have no effect.

If the value is set larger than the Maximum allowed OneDrive for Business quota, it will have no effect.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -IsWBFluidEnabled

Sets whether Whiteboard is enabled or disabled for OneDrive for Business users. Whiteboard on OneDrive for Business is automatically enabled for applicable Microsoft 365 tenants but can be disabled.

The valid values are:

- $true - Administrator enabled Whiteboard for user with OneDrive for Business Users.
- $false - Administrator disable Whiteboard for user with OneDrive for Business Users.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrphanedPersonalSitesRetentionPeriod

Specifies the number of days after a user's Active Directory account is deleted that their OneDrive for Business content will be deleted.

The value range is in days, between 30 and 3650. The default value is 30.

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

### -OwnerAnonymousNotification

Enables or disables owner anonymous notification. If enabled, an email notification will be sent to the OneDrive for Business owners when an anonymous links are created or changed.

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissiveBrowserFileHandlingOverride

Enables the Permissive browser file handling. By default, the browser file handling is set to Strict. The Strict setting adds headers that force the browser to download certain types of files. The forced download improves security by disallowing the automatic execution of Web content. When the setting is set to Permissive, no headers are added and certain types of files can be executed in the browser instead of download.

The valid values are:

- True - Enable the Permissive browser file handling setting.
- False - Keep the default Strict browser file handling setting.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreventExternalUsersFromResharing

Prevents external users from resharing files, folders, and sites that they do not own.

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCdnAllowedFileTypes

Sets public CDN allowed file types, if the public CDN is enabled.

PARAMVALUE: String

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCdnEnabled

Enables or disables the public CDN.

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireAnonymousLinksExpireInDays

Specifies all anonymous links that have been created (or will be created) will expire after the set number of days.

The value can be from 0 to 730 days.

To remove the expiration requirement, set the value to zero (0).

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

### -SharingAllowedDomainList

Specifies a list of email domains that is allowed for sharing with the external collaborators. Use the space character as the delimiter for entering multiple values. For example, "contoso.com fabrikam.com".

For additional information about how to restrict a domain sharing, see [Restricted Domains Sharing in Office 365 SharePoint Online and OneDrive for Business](https://support.office.com/en-US/article/Restricted-Domains-Sharing-in-Office-365-SharePoint-Online-and-OneDrive-for-Business-5d7589cd-0997-4a00-a2ba-2320ec49c4e9).

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingBlockedDomainList

Specifies a list of email domains that is blocked or prohibited for sharing with the external collaborators. Use space character as the delimiter for entering multiple values. For example, "contoso.com fabrikam.com".

For additional information about how to restrict a domain sharing, see [Restricted Domains Sharing in Office 365 SharePoint Online and OneDrive for Business](https://support.office.com/en-US/article/Restricted-Domains-Sharing-in-Office-365-SharePoint-Online-and-OneDrive-for-Business-5d7589cd-0997-4a00-a2ba-2320ec49c4e9).

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingDomainRestrictionMode

Specifies the external sharing mode for domains.

The valid values are:

- None
- AllowList - Users will be able to share with external collaborators coming only from that email domain.
- BlockList - Users will be able to share with all external collaborators apart from the ones on the BlockedDomainList.

For additional information about how to restrict a domain sharing, see [Restricted Domains Sharing in Office 365 SharePoint Online and OneDrive for Business](https://support.office.com/en-US/article/Restricted-Domains-Sharing-in-Office-365-SharePoint-Online-and-OneDrive-for-Business-5d7589cd-0997-4a00-a2ba-2320ec49c4e9).

```yaml
Type: SharingDomainRestrictionModes
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowPeoplePickerSuggestionsForGuestUsers

Shows people picker suggestions for guest users. To enable the option to search for existing guest users at Tenant Level, set this parameter to $true.

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

### -SpecialCharactersStateInFileFolderNames

Permits the use of special characters in file and folder names in SharePoint Online and OneDrive for Business document libraries.

> [!NOTE]
> The only two characters that can be managed at this time are the # and % characters.  

The valid values are:

- NoPreference - Support for feature will be enabled by Microsoft on your Office 365 tenant.
- Allowed - Lets the # and % characters in file and folder names in SharePoint Online and OneDrive for Business document libraries.
- Disallowed - Disallows the # and % characters in file and folder names in SharePoint Online and OneDrive for Business document libraries.

```yaml
Type: SpecialCharactersState
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReSyncTenantPrivacyProfile 
The 'SyncPrivacyProfileProperties' parameter is obsolete and renamed ReSyncTenantPrivacyProfile.

This parameter enables the synchronization of privacy profile properties.

ReSyncTenantPrivacyProfile sets whether or not the synced tenant properties will be updated on the next request. The request will cause Azure Active Directory to grab the tenant's current display name (TenantDisplayName) and privacy profile URL (PrivacyProfileUrl). 

Running 'Set-SPOTenant - ReSyncTenantPrivacyProfile' will force a sync from the Azure Active Directory privacy profile URL to SharePoint Online. The sync may take up to 24 hours to complete. Whenever SharePoint Online gets the privacy profile URL, it checks whether the last sync time is out of the sync time window. If it is, it syncs from Azure Active Directory to SharePoint Online.

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

### -UseFindPeopleInPeoplePicker

This feature enables tenant admins to enable ODB and SPO to respect Exchange supports Address Book Policy (ABP) policies in the people picker.

> [!NOTE]
> When set to $true, users aren't able to share with security groups or SharePoint groups.  

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -DisableDocumentLibraryDefaultLabeling

This switch allows tenant admins to disable the capability of configuring a default sensitivity label for a document library.

> [!NOTE]
> When set to $true, users aren't able to apply a default sensitivity label for a document library. The default value is false.  

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: false
Accept pipeline input: False
Accept wildcard characters: False
```


### -UserVoiceForFeedbackEnabled

Enables or disables the User Voice Feedback button.

PARAMVALUE: $true | $false

When set to $true, the "Feedback" link will be shown at the bottom of all modern SharePoint Online pages. The "Feedback" link will allow the end user to fill out a feedback form inside SharePoint Online which will then create an entry in the public SharePoint UserVoice topic.

When set to $false, feedback link will not be shown anymore. It may take up to an hour for a change of this property to be reflected consistently throughout your tenant.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: $true
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomizedExternalSharingServiceUrl

Specifies a URL that will be appended to the error message that is surfaced when a user is blocked from sharing externally by policy. This URL can be used to direct users to internal portals to request help or to inform them about your organization's policies. An example value is "<https://www.contoso.com/sharingpolicies".>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentTypeSyncSiteTemplatesList [String[]] [-ExcludeSiteTemplate]

By default Content Type Hub will no longer push content types to OneDrive for Business sites (formerly known as MySites).

In case you want the Content Type Hub to push content types to OneDrive for Business sites, use: `Set-SPOTenant -ContentTypeSyncSiteTemplatesList MySites`.

When the feature is enabled, the Content Type Hub will push content types to OneDrive for Business sites.

Once you have enabled Content Type publishing to OneDrive for Business sites, you can disable it later using: `Set-SPOTenant -ContentTypeSyncSiteTemplatesList MySites -ExcludeSiteTemplate`.

```yaml
Type: String[]
Parameter Sets: ParameterSetContentTypeSyncSiteTemplatesList
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeSiteTemplate
Excludes the specified template from Content Type hub content type synchronization. Must be used with `-ContentTypeSyncSiteTemplatesList [String[]]`.
 

```yaml
Type: SwitchParameter
Parameter Sets: ParameterSetContentTypeSyncSiteTemplatesList
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionalAccessPolicy

Please read [Control access from unmanaged devices](https://learn.microsoft.com/sharepoint/control-access-from-unmanaged-devices ) documentation here to understand Conditional Access Policy usage in SharePoint Online.

PARAMVALUE: AllowFullAccess | AllowLimitedAccess | BlockAccess

```yaml
Type: SPOConditionalAccessPolicyType
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: AllowFullAccess
Accept pipeline input: True
Accept wildcard characters: False
```

### -ConditionalAccessPolicyErrorHelpLink

A Link for help when Conditional Access Policy blocks a user. This should be in a valid URL format. A valid URL format that begins with http:// or https://.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowDownloadingNonWebViewableFiles  

This paramater has been deprecated.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowCommentsTextOnEmailEnabled  

When this parameter is true, the email notification that a user receives when is mentioned, includes the surrounding document context. Set it to false to disable this feature.

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

### -AllowEditing  

Prevents users from editing Office files in the browser and copying and pasting Office file contents out of the browser window.

PARAMVALUE: $true | $false

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

### -EnableAzureADB2BIntegration  

Enables OneDrive and SharePoint integration with Azure AD B2B. For more information, see [SharePoint and OneDrive integration with Azure AD B2B](/sharepoint/sharepoint-azureb2b-integration).

PARAMVALUE: $true | $false

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

### -LimitedAccessFileType

Allows users to preview only Office files in the browser. This option increases security, but may be a barrier to user productivity.

The following parameters can be used with `-ConditionalAccessPolicy AllowLimitedAccess` for both the organization-wide setting and the site-level setting.

- OfficeOnlineFilesOnly: Allows users to preview only Office files in the browser. This option increases security but may be a barrier to user productivity.
- LimitedAccessFileType WebPreviewableFiles (default): Allows users to preview Office files in the browser. This option optimizes for user productivity but offers less security for files that aren't Office files. **Warning:** This option is known to cause problems with PDF and image file types because they can be required to be downloaded to the end user's machine to render in the browser. Plan the use of this control carefully. Otherwise, your users could be faced with unexpected "Access Denied" errors.
- LimitedAccessFileType OtherFiles: Allows users to download files that can't be previewed, such as .zip and .exe. This option offers less security.

PARAMVALUE: OfficeOnlineFilesOnly | WebPreviewableFiles | OtherFiles

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

### -ExternalUserExpirationRequired

Specifies whether to enable the external user expiration policy, where external users will be expired and removed from the site collection in a given number of days.

Note: Once the policy is enabled, expiration values will be set on external users as they join a site collection (via sharing links or via direct access). When the policy is disabled, it will no longer set expiration values on users, but it will not automatically clear expiration values set on existing users. The users can then have their expiration value cleared by a site collection administrator if required.

The valid values are:
True - Enables the Policy.
False (default) - Disables the policy.

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
### -EnableSensitivityLabelforPDF

Allows tenant admins to turn on support for PDFs with sensitivity labels for the following scenarios:

- Applying a sensitivity label in Office for the web.
- Uploading a labeled document, and then extracting and displaying that sensitivity label.
- Search, eDiscovery, and data loss prevention.
- Auto-labeling policies and default sensitivity labels for SharePoint document libraries.

The valid values are:

- True - Enables support for PDFs.
- False (default) - Disables support for PDFs.

```yaml
Type: Boolean

Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: false
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalUserExpireInDays

Specifies the number of days before an external user will expire and be removed from the site collection if the policy is enabled. Value can be from 30 to 730 days.

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

### -EmailAttestationRequired

Sets email attestation to required.

If people who use a verification code select to "stay signed in" in the browser, they must prove that they can access the same account that they used to redeem the sharing invitation. You can set the number of days for email attestation with **-EmailAttestationReAuthDays**. This setting affects only ad-hoc external recipients.

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

### -EmailAttestationReAuthDays

Sets the number of days for email attestation re-authentication. Value can be from 1 to 365 days.

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

### -BlockUserInfoVisibility

This feature has not yet been rolled out to Production. Attempting to set this parameter before rollout is complete will result in an error message. More details on this feature will be available on release.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockUserInfoVisibilityInOneDrive

Blocks users from accessing User Info if they have Limited Access permission only to the OneDrive. The policy applies to all OneDrives in the tenant. 

The valid values are: 

- ApplyToNoUsers (default) – No users are prevented from accessing User Info when they have Limited Access permission only 

- ApplyToAllUsers – All users (internal or external) are prevented from accessing User Info if they have Limited Access permission only 

- ApplyToGuestAndExternalUsers – Only external or guest users are prevented from accessing User Info if they have Limited Access permission only 

- ApplyToInternalUsers – Only internal users are prevented from accessing User Info if they have Limited Access permission only 

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: ApplyToNoUsers
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockUserInfoVisibilityInSharePoint

Blocks users from accessing User Info if they have Limited Access permission only to a SharePoint site. Policy applies to all SharePoint sites in the tenant. 

The valid values are: 

- ApplyToNoUsers (default) – No users are prevented from accessing User Info when they have Limited Access permission only to a SharePoint site 

- ApplyToAllUsers – All users (internal or external) are prevented from accessing User Info if they have Limited Access permission only to a SharePoint site 

- ApplyToGuestAndExternalUsers – Only external or guest users are prevented from accessing User Info if they have Limited Access permission only to a SharePoint site 

- ApplyToInternalUsers – Only internal users are prevented from accessing User Info if they have Limited Access permission only to a SharePoint site 

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: ApplyToNoUsers
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowOverrideForBlockUserInfoVisibility

Allow organization level policy for Block User Info Visibility to be overridden for a SharePoint site or OneDrive. Use Set-SPOSite to override the policy for a SharePoint site or OneDrive. 

The valid values are:

- False (default) – Do not allow the Block User Info Visibility policy to be overridden for a SharePoint site or OneDrive 

- True – Allow the Block User Info Visibility policy to be overridden for a SharePoint site or OneDrive 

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

### -EnableAutoNewsDigest

Enable or disable auto news digest. [Documentation](https://aka.ms/autonewsdigest) for auto news digest.

```yaml
Type: Boolean

Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeAtAGlanceInShareEmails

Enable or disable the At A Glance feature in sharing e-mails. This provides the key points and time to read for the shared item if available.

```yaml
Type: Boolean

Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -StopNew2010Workflows
Prevents creation of new SharePoint 2010 classic workflows.

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

### -StopNew2013Workflows
Prevents creation of new SharePoint 2013 classic workflows.

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

### -BlockSendLabelMismatchEmail

When a sensitivity label mismatch occurs between the label on the document uploaded and the label on the site, SharePoint Online captures an audit record, and sends an Incompatible sensitivity label detected email notification to the person who uploaded the document and the site owner. The notification contains details of the document which caused the problem and the label assigned to the document and to the site. The comparison happens between the priority of these two labels. 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: false
Accept pipeline input: False
Accept wildcard characters: False
```

### -LabelMismatchEmailHelpLink
This parameter allows tenant admins to customize the "Help Link" in email with the subject "Incompatible sensitivity label detected." When a sensitivity label mismatch occurs between the label on the document uploaded and the label on the site, SharePoint Online captures an audit record and sends an Incompatible sensitivity label detected email notification to the person who uploaded the document and the site owner. The notification contains details of the document which caused the problem and the label assigned to the document and to the site. The comparison happens between the priority of these two labels. 

The value can be any valid URL.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableOutlookPSTVersionTrimming

This parameter has no effect and it was used to opt-out of PST files retention policy changes as communicated in MC256835 (May 2021).
Starting August 16, 2021, the service started retaining 30 days worth of versions for any PST files stored in OneDrive for Business and SharePoint Online team site document libraries. This change was introduced to prevent cases of previous versions of PST files quickly consuming available storage. The change only impacts previous versions of PST files stored in your document library storage. As a best practice, PST files should not be uploaded on OneDrive for Business and SharePoint Online team site document libraries due to the impact on storage and network bandwidth.

PARAMVALUE: $true | $false

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

### -DisableAddShortcutsToOneDrive 

When the feature is disabled ($true), the option [Add shortcut to My files](https://support.microsoft.com/office/add-shortcuts-to-shared-folders-in-onedrive-for-work-or-school-d66b1347-99b7-4470-9360-ffc048d35a33) will be removed; any folders that have already been added will remain on the user's computer.

PARAMVALUE: $true | $false

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

### -ViewInFileExplorerEnabled
Enables or disables the ability to use View in Explorer in Microsoft Edge (93) or above. 

> [!NOTE]
> When the value is set the View In Explorer command will become visible in UX for all users using Edge browser version 93 or above however those users still need [ConfigureViewInFileExplorer](https://learn.microsoft.com/deployedge/microsoft-edge-policies#configureviewinfileexplorer) Edge policy enabled for the functionality to work.
> 
> Minimum Module Version Required: 16.0.21610.12000 

The valid values are:  

- False (default) - Disables View In Explorer command to become visible in Edge.
- True - Enables View In Explorer command to become visible in Edge.

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

### -AllowGuestUserShareToUsersNotInSiteCollection 

The AllowGuestUserShareToUsersNotInSiteCollection settings (defaulted to false) will allow guests to share to users not in the site.

The valid values are:  

- False (default) – Guest users will only be able to share to users that exist within the current site. 
- True – Guest users will be able to find user accounts in the directory by typing in the exact email address match. 

Note: When the value is set to True, you will also need to enable [SharePoint and OneDrive integration with Azure AD B2B](/sharepoint/sharepoint-azureb2b-integration) for the functionality to work.

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

### -ShowOpenInDesktopOptionForSyncedFiles

The ShowOpenInDesktopOptionForSyncedFiles setting (set to false by default) displays the "Open in desktop" option when users go to SharePoint or OneDrive on the web and open the shortcut menu for a file that they're syncing with the OneDrive sync app.

The valid values are:

- False (default) – "Open in desktop" is disabled and not shown on the shortcut menu.
- True – "Open in desktop" is enabled and the option to open synced files locally appears on the shortcut menu.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveLoopDefaultSharingLinkScope

Gets or sets default share link scope for fluid on OneDrive sites. 

The valid values are:  

- Anyone
- Organization
- SpecificPeople
- Uninitialized

```yaml
Type: SharingCapabilities
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: Uninitialized
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveLoopDefaultSharingLinkRole

Gets or sets default share link role for fluid on OneDrive sites.

Note: Although the values below may be viewable in Powershell, only View OR Edit may be set at this time. 

The valid values are:  

- Edit
- View
- LimitedEdit
- LimitedView
- ManageList
- None
- Owner
- RestrictedView
- Review
- Submit

```yaml
Type: SharingCapabilities
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreLoopDefaultSharingLinkScope

Gets or sets default share link scope for fluid on SharePoint sites. 

The valid values are:  

- Anyone
- Organization
- SpecificPeople
- Uninitialized

```yaml
Type: SharingCapabilities
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: Uninitialized
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreLoopDefaultSharingLinkRole

Gets or sets default share link role for fluid on SharePoint sites.

Note: Although the values below may be viewable in Powershell, only View OR Edit may be set at this time. 

The valid values are:  

- Edit
- View
- LimitedEdit
- LimitedView
- ManageList
- None
- Owner
- RestrictedView
- Review
- Submit

```yaml
Type: SharingCapabilities
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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.

For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

### -ReduceTempTokenLifetimeEnabled 
Enables reduced session timeout for temporary URLs used by apps for document download scenarios. Reduction occurs when an app redeeming an IP address does not match the original requesting IP. The default value is 15 minutes if ReduceTempTokenLifetimeValue is not set.

**Note**: Reducing this value may bring degradation in end-user experience by requiring frequent authentication prompts to users. 


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
### -ReduceTempTokenLifetimeValue

Optional parameter to set the session timeout value for temporary URLs. The value can be set between 5 and 15 minutes and the default value is 15 minutes.
 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: 15
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowPeoplePickerGroupSuggestionsForIB

The ShowPeoplePickerGroupSuggestionsForIB setting (defaulted to false) allows showing group suggestions for information barriers (IBs) in the People Picker.

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

### -InformationBarriersSuspension

When InformationBarriersSuspension parameter is set to $false, information barriers in SharePoint and OneDrive is enabled, when set to $true, it is disabled.

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

### -IBImplicitGroupBased

The IBImplicitGroupBased setting enables Microsoft 365 Groups membership-based access and sharing control for all Implicit mode sites.

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

### -DefaultOneDriveInformationBarrierMode

The DefaultOneDriveInformationBarrierMode sets the information barrier mode for all OneDrive sites.

The valid values are:

- Open
- Explicit
- Implicit
- OwnerModerated
- Mixed

For more information about information barriers, see [Use information barriers with SharePoint](/purview/information-barriers-sharepoint) for your SharePoint Online environment.
  
```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ViewersCanCommentOnMediaDisabled

Controls whether viewers commenting on media items is disabled or not.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreSharingCapability

Determines what level of sharing is available for SharePoint sites (not including OneDrive sites).

The valid values are:  

- ExternalUserAndGuestSharing (default) - External user sharing (share by email) and guest link sharing are both enabled.
- Disabled - External user sharing (share by email) and guest link sharing are both disabled.
- ExternalUserSharingOnly - External user sharing (share by email) is enabled, but guest link sharing is disabled.
- ExistingExternalUserSharingOnly - Only guests already in your organization's directory.

For more information about sharing, see [Manage sharing settings](/sharepoint/turn-external-sharing-on-or-off) for your SharePoint online environment.

```yaml
Type: SharingCapabilities
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: ExternalUserAndGuestSharing
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveRequestFilesLinkEnabled

Enable or disable the Request files link on the OneDrive partition for all OneDrive sites. If this value is not set, the Request files link will only show for OneDrives with Anyone links enabled. 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoreRequestFilesLinkEnabled

Enable or disable the Request files link on the core partition for all SharePoint sites (not including OneDrive sites). If this value is not set, Request files will only show for OneDrives with Anyone links enabled. 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OneDriveRequestFilesLinkExpirationInDays

Specifies the number of days before a Request files link expires for all OneDrive sites. 

The value can be from 0 to 730 days.

To remove the expiration requirement, set the value to zero (0).

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

### -CoreRequestFilesLinkExpirationInDays

Specifies the number of days before a Request files link expires for all SharePoint sites (not including OneDrive sites).

The value can be from 0 to 730 days.

To remove the expiration requirement, set the value to zero (0).

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

### -AllowAnonymousMeetingParticipantsToAccessWhiteboards
When you share a whiteboard in a Teams meeting, Whiteboard creates a sharing link. This link is accessible by anyone within the organization. The whiteboard is also shared with any in-tenant users in the meeting. Whiteboards are shared using company-shareable links, regardless of the default setting. Support for the default sharing link type is planned.

There's more capability for temporary collaboration by external and shared device accounts during a Teams meeting. Users can temporarily view and collaborate on whiteboards that are shared in a meeting, in a similar way to PowerPoint Live sharing.

In this case, Whiteboard provides temporary viewing and collaboration on the whiteboard during the Teams meeting only. A share link isn't created and Whiteboard doesn't grant access to the file.

If you have external sharing enabled for OneDrive for Business, no further action is required.

If you restrict external sharing for OneDrive for Business, you can keep it restricted, and just enable this new setting in order for external and shared device accounts to work. For more information, see [Manage sharing for Microsoft Whiteboard](/microsoft-365/whiteboard/manage-sharing-organizations).

```yaml
Type: SharingState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableBackToClassic

Enables or disables the link "Return to classic SharePoint" on modern SharePoint list and library pages.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsEnableAppAuthPopUpEnabled

Enables or disables users in the organization to authenticate SharePoint applications using popups. 

This parameter affects the way code in SharePoint interacts with Azure AD to get tokens to access APIs. In scenarios where third-party cookies are disabled (such as Safari browsers with ITP feature enabled), any code that requires a token to access an API automatically triggers a full page refresh. When IsEnableAppAuthPopUpEnabled is set to $true, SharePoint will instead surface a popup in this scenario.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockDownloadFileTypePolicy 

You can block the download of Teams meeting recording files from SharePoint or OneDrive. This allows users to remain productive while addressing the risk of accidental data loss. Users have browser-only access to play the meeting recordings with no ability to download or sync files or access them through apps.

This policy applies to new meeting recordings across the entire organization. You can exempt people who are members of specified security groups from the policy. This allows you to specify governance or compliance specialists who should have download access to meeting recordings.

After the policy is turned on, any new Teams meeting recording files created by the Teams service and saved in SharePoint and OneDrive are blocked from download.

Because this policy affects meeting recordings stored in OneDrive and SharePoint, you must be a SharePoint administrator to configure it.

Note that this policy doesn't apply to manually uploaded meeting recording files. For more details, see [Block the download of Teams meeting recording files from SharePoint or OneDrive](/microsoftteams/block-download-meeting-recording).

```yaml
Type: Boolean 
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoExpirationVersionTrim
Global and SharePoint admins in Microsoft 365 can set Organization-level Version History Limit settings that universally apply to new versions created on all new Document Libraries created in your organization. 

When Version History Limits are managed Automatically, SharePoint employs an algorithm behind the scenes that deletes (thins out) intermittent older versions that are least likely to be needed, while preserving sufficient high-value versions - more versions in the recent past and fewer farther back in time - in case restores are required.

The valid values are: 

- True – Version History Limits for new versions created on all new Document Libraries in your organization will be managed Automatically.  
- False – Version History Limits for new Versions created on all new Document Libraries in your organization will be managed Manually by setting limits to the number of major versions (MajorVersionLimit) and time set (ExpireVersionsAfterDays).  Review the documentation of both parameters to manage your organization's version limits Manually.  

> [!NOTE]
> When Version History Limits are managed Manually (EnableAutoExpirationVersionTrim $false), MajorVersionLimit and ExpireVersionsAfterDays are both required parameters with the following acceptable values:
> a. MajorVersionLimit accepts values from 1 through 50,000 (inclusive).
> b. ExpireVersionsAfterDays accepts values of 0 to Never Expire or values >= 30 to delete versions that exceed that time period.
> When Version History Limits are managed Automatically (EnableAutoExpirationVersionTrim $true), setting MajorVersionLimit or ExpireVersionsAfterDays will result in an error as the count limits are set by the service.
>
> This parameter is currently under private preview.

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MajorVersionLimit
When Version History Limits are managed Manually (EnableAutoExpirationVersionTrim $false), admins will need to set the limits to the number of major versions (MajorVersionLimit) and the time period the versions are stored (ExpireVersionsAfterDays). Please check the description of EnableAutoExpirationVersionTrim for more details.

PARAMVALUE: Int32

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

### -ExpireVersionsAfterDays
When Version History Limits are managed Manually (EnableAutoExpirationVersionTrim $false), admins will need to set the limits to the number of major versions (MajorVersionLimit) and the time period the versions are stored (ExpireVersionsAfterDays). Please check the description of EnableAutoExpirationVersionTrim for more details.

PARAMVALUE: Int32

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

### -MassDeleteNotificationDisabled
Enables or disables the mass delete detection feature. When MassDeleteNotificationDisabled is set to $true, tenant admins can perform mass deletion operations without triggering notifications.

PARAMVALUE: $true | $false

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

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Upgrade-SPOSite](Upgrade-SPOSite.md)

[Set-SPOSite](Set-SPOSite.md)
