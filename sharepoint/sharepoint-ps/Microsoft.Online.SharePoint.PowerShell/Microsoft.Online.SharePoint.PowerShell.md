Frestrie---
Module Name: Microsoft.Online.SharePoint.PowerShell
Module Guid: adedde5f-e77b-4682-ab3d-a4cb4ff79b83
title: Microsoft.Online.SharePoint.PowerShell Module
Locale: en-US
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Microsoft.Online.SharePoint.PowerShell Module
## Description

The following cmdlet references are for SharePoint Online.

## Microsoft.Online.SharePoint.PowerShell Cmdlets

### [Add-SPOContainerTypeBilling](Add-SPOContainerTypeBilling.md)
Adds the mentioned billing profile details to a standard container type.

### [Add-SPOContainerUser](Add-SPOContainerUser.md)
Adds a user to a SharePoint Embedded container with a specified role.

### [Add-SPOContentSecurityPolicy](Add-SPOContentSecurityPolicy.md)
Adds a source to the **Content Security Policy** configuration.

### [Add-SPOFileRequestBrandingProfile](Add-SPOFileRequestBrandingProfile.md)
Adds a branding profile for the file request feature by specifying logo and background assets from an existing organization asset library.

### [Add-SPOFontPackage](Add-SPOFontPackage.md)
Creates a new custom font package with fonts in the brand fonts library.

### [Add-SPOGeoAdministrator](Add-SPOGeoAdministrator.md)
Adds a new SharePoint user or security group as GeoAdministrator to a multi-geo tenant.

### [Add-SPOHubSiteAssociation](Add-SPOHubSiteAssociation.md)
Associates a site with a hub site.

### [Add-SPOHubToHubAssociation](Add-SPOHubToHubAssociation.md)
Associates a hub site to a hub site. Note: This feature is currently in preview and may not be available in your tenant.

### [Add-SPOListDesign](Add-SPOListDesign.md)
Creates a new list or document library design available to users when they create a new list or document library from site contents, certain site home pages, the SharePoint home page, the Microsoft Lists app, Microsoft Teams, or Office.com.

### [Add-SPOOrgAssetsLibrary](Add-SPOOrgAssetsLibrary.md)
Designates a library to be used as a central location for organization assets across the tenant.

### [Add-SPOServicePrioritizationAppRegistration](Add-SPOServicePrioritizationAppRegistration.md)
Adds a new app registration for service prioritization in SharePoint Online. > [!NOTE] > This functionality is rolling out and might not be fully enabled in your environment yet.

### [Add-SPOSiteCollectionAppCatalog](Add-SPOSiteCollectionAppCatalog.md)
Adds a Site Collection scoped App Catalog to a site.

### [Add-SPOSiteDesign](Add-SPOSiteDesign.md)
Creates a new site design available to users when they create a new site from the SharePoint home page.

### [Add-SPOSiteDesignTask](Add-SPOSiteDesignTask.md)
Similar to Invoke-SPOSiteDesign, this command is used to apply a published site design to a specified site collection target. It schedules the operation, allowing for the application of larger site scripts (Invoke-SPOSiteDesign is limited to 30 actions and subactions).  The supported site templates you can apply a site design to include: "modern" team site (with O365 group), "modern" team site (without an O365 group); communication site; classic team site; and classic publishing site.

### [Add-SPOSiteScript](Add-SPOSiteScript.md)
Uploads a new site script for use either directly or in a site design.

### [Add-SPOSiteScriptPackage](Add-SPOSiteScriptPackage.md)
Uploads a new site script package for use either directly or in a site design.

### [Add-SPOTenantCdnOrigin](Add-SPOTenantCdnOrigin.md)
Configures a new origin to public or private content delivery network (CDN). Requires Tenant administrator permissions.

### [Add-SPOTheme](Add-SPOTheme.md)
Creates a new custom theme, or overwrites an existing theme to modify its settings.

### [Add-SPOUser](Add-SPOUser.md)
Adds an existing Office 365 user or an Office 365 security group to a SharePoint group.

### [Approve-SPOTenantServicePrincipalPermissionGrant](Approve-SPOTenantServicePrincipalPermissionGrant.md)
Approves a permission request for the current tenant's "SharePoint Online Client" service principal.

### [Approve-SPOTenantServicePrincipalPermissionRequest](Approve-SPOTenantServicePrincipalPermissionRequest.md)
Approves a permission request for the current tenant's "SharePoint Online Client" service principal

### [Clear-SPOTenantPreAuthSettings](Clear-SPOTenantPreAuthSettings.md)
Clears the pre-authentication settings for either the allow or deny list.

### [Connect-SPOService](Connect-SPOService.md)
Connects the SharePoint Online Administrator or the SharePoint Embedded Administrator to a SharePoint Online connection (the SharePoint Online Administration Center). This cmdlet must be run before any other SharePoint Online cmdlets can run.

### [ConvertTo-SPOMigrationEncryptedPackage](ConvertTo-SPOMigrationEncryptedPackage.md)
Use this Cmdlet to convert your XML files into a new encrypted migration package.

### [ConvertTo-SPOMigrationTargetedPackage](ConvertTo-SPOMigrationTargetedPackage.md)
Use this cmdlet to convert your XML files into a new migration package.

### [Copy-SPOPersonalSitePage](Copy-SPOPersonalSitePage.md)
This cmdlet command allows you to relocate existing SharePoint pages by utilizing an existing copy operation. We will also copy any assets associated with the SharePoint pages to the new destination. We offer two methods for relocating pages: - Copy: This method keeps the original page intact while creating a duplicate at the new location. - Move: This method creates a new copy at the new location and deletes the original page from the source.

### [Deny-SPOTenantServicePrincipalPermissionRequest](Deny-SPOTenantServicePrincipalPermissionRequest.md)
Denies a permission request for the current tenant's "SharePoint Online Client" service principal

### [Disconnect-SPOService](Disconnect-SPOService.md)
Disconnects from a SharePoint Online service.

### [Enable-SPOCommSite](Enable-SPOCommSite.md)
Enables the  communication site experience on an existing classic team site. Please read instructions in [modernize classic team site](/sharepoint/modernize-classic-team-site) before attempting to execute this cmdlet.

### [Enable-SPOTenantServicePrincipal](Enable-SPOTenantServicePrincipal.md)
Enables the current tenant's "SharePoint Online Client" service principal.

### [Export-SPODataAccessGovernanceInsight](Export-SPODataAccessGovernanceInsight.md)
This cmdlet downloads the Data Access Governance (DAG) reports to the specified path. The default is the "Downloads" folder.

### [Export-SPOQueryLogs](Export-SPOQueryLogs.md)
Export query logs for a user in an Office 365 tenant.  > [!NOTE] > Beginning February 2022, we'll be removing the Export-SPOQueryLogs command from SharePoint in Microsoft 365. We encourage users to instead download their Microsoft Search query history logs from the [My Account privacy portal](https://myaccount.microsoft.com/settingsandprivacy/privacy).

### [Export-SPOUserInfo](Export-SPOUserInfo.md)
Export user information from site user information list.

### [Export-SPOUserProfile](Export-SPOUserProfile.md)
Export user profile data to csv file.

### [Find-SPOCrossTenantLongFilePathsForSiteRename](Find-SPOCrossTenantLongFilePathsForSiteRename.md)
Identify sites with file paths over 400 characters for cross-tenant user migration.

### [Get-FileSensitivityLabelInfo](Get-FileSensitivityLabelInfo.md)
Extracts and displays the sensitivity label related information attached to an office file stored in SharePoint.

### [Get-SPOAppBillingPolicies](Get-SPOAppBillingPolicies.md)
Returns billing policies that are owned by the tenant.

### [Get-SPOAppErrors](Get-SPOAppErrors.md)
Returns application errors.

### [Get-SPOAppInfo](Get-SPOAppInfo.md)
Returns all installed applications.

### [Get-SPOApplication](Get-SPOApplication.md)
Returns a list of SharePoint Embedded applications in the specified tenant.

### [Get-SPOAuditDataCollectionStatusForActivityInsights](Get-SPOAuditDataCollectionStatusForActivityInsights.md)
Lists the current status of audit data collection for reports on activities from the last 28 days in the SharePoint admin center.

### [Get-SPOBrowserIdleSignOut](Get-SPOBrowserIdleSignOut.md)
Used to retrieve the current configuration values for Idle session sign-out policy.

### [Get-SPOBuiltInDesignPackageVisibility](Get-SPOBuiltInDesignPackageVisibility.md)
Gets the visibility of the available built-in Design Packages.

### [Get-SPOBuiltInFontPackageSettings](Get-SPOBuiltInFontPackageSettings.md)
Use this cmdlet to get settings of [built-in font packages](/sharepoint/brand-center-font-packages).

### [Get-SPOBuiltInSiteTemplateSettings](Get-SPOBuiltInSiteTemplateSettings.md)
Get the current state of Microsoft-provided SharePoint site templates displayed or hidden in the site template gallery in your tenant.

### [Get-SPOContainer](Get-SPOContainer.md)
Returns one or more containers in a SharePoint Embedded application.

### [Get-SPOContainerType](Get-SPOContainerType.md)
Returns one or more container types created in the tenant.

### [Get-SPOContainerTypeConfiguration](Get-SPOContainerTypeConfiguration.md)
Use this cmdlet to read the configuration values set on the container type.

### [Get-SPOContentEventEmailAddresses](Get-SPOContentEventEmailAddresses.md)
Retrieves email addresses associated with a specific content event category. If no category is specified by the user, email addresses for all categories of content events will be provided.

### [Get-SPOContentSecurityPolicy](Get-SPOContentSecurityPolicy.md)
Returns all sources in the current **Content Security Policy** configuration.

### [Get-SPOCopilotAgentInsightsReport](Get-SPOCopilotAgentInsightsReport.md)
This cmdlet enables the administrator to check status of all active and available reports when no report ID is present and to view or download a report if report ID is present.  > [!NOTE] > The feature associated with this cmdlet will be rolling out soon.

### [Get-SPOCrossGeoMovedUsers](Get-SPOCrossGeoMovedUsers.md)
In a multi-geo tenant returns the SharePoint Online user (or users) that had been moved.

### [Get-SPOCrossGeoMoveReport](Get-SPOCrossGeoMoveReport.md)
Provides a report of objects moved between geo locations.

### [Get-SPOCrossGeoUsers](Get-SPOCrossGeoUsers.md)
Returns the SharePoint Online users in a multi-geo tenant that match the criteria.

### [Get-SPOCrossTenantCompatibilityStatus](Get-SPOCrossTenantCompatibilityStatus.md)
Determines the compatibility with the partner tenant.

### [Get-SPOCrossTenantHostUrl](Get-SPOCrossTenantHostUrl.md)
Returns the cross-tenant host URL.

### [Get-SPODataAccessGovernanceInsight](Get-SPODataAccessGovernanceInsight.md)
Lists various 'Data Access Governance' (DAG) reports in SharePoint admin center.

### [Get-SPODataEncryptionPolicy](Get-SPODataEncryptionPolicy.md)
.

### [Get-SPODeletedContainer](Get-SPODeletedContainer.md)
Returns all deleted Containers in the Recycle Bin.

### [Get-SPODeletedSite](Get-SPODeletedSite.md)
Returns all deleted site collections from the Recycle Bin.

### [Get-SPOEnterpriseAppInsightsReport](Get-SPOEnterpriseAppInsightsReport.md)
This cmdlet enables the administrator to check status of all active and available reports when no report ID is present and to view or download a report if report ID is present.

### [Get-SPOExternalUser](Get-SPOExternalUser.md)
Returns external users in the tenant.

### [Get-SPOFileRequestBrandingProfiles](Get-SPOFileRequestBrandingProfiles.md)
Retrieves branding profiles configured for the file request feature, including details about logo and background assets.

### [Get-SPOFontPackage](Get-SPOFontPackage.md)
Returns one or all custom font packages in the tenant.

### [Get-SPOGeoAdministrator](Get-SPOGeoAdministrator.md)
This cmdlet returns the SharePoint Online user or security group accounts with Global Admin privileges in the current multi-geo tenant.

### [Get-SPOGeoMoveCrossCompatibilityStatus](Get-SPOGeoMoveCrossCompatibilityStatus.md)
This cmdlet returns the compatibility status between geographic locations.

### [Get-SPOGeoStorageQuota](Get-SPOGeoStorageQuota.md)
This cmdlet gets the storage quota on a multi-geo tenant.

### [Get-SPOHideDefaultThemes](Get-SPOHideDefaultThemes.md)
Queries the current SPOHideDefaultThemes setting. SPO stands for SharePoint Online.

### [Get-SPOHomeSite](Get-SPOHomeSite.md)
Returns the home site url for your tenant.

### [Get-SPOHubSite](Get-SPOHubSite.md)
Lists hub sites or hub site information.

### [Get-SPOInformationBarriersInsightsReport](Get-SPOInformationBarriersInsightsReport.md)
Enables the SharePoint Administrator to check status of all active and completed reports of insights on Information Barriers (IB).

### [Get-SPOListDesign](Get-SPOListDesign.md)
Gets details about list designs that are on the SharePoint tenant. You can specify an ID of a specific list design to retrieve. If there are no parameters listed, details about all list designs are listed.

### [Get-SPOListFileVersionBatchDeleteJobProgress](Get-SPOListFileVersionBatchDeleteJobProgress.md)
Gets the progress of a trim job for a site collection.

### [Get-SPOListFileVersionExpirationReportJobProgress](Get-SPOListFileVersionExpirationReportJobProgress.md)
Gets the status for a file version expiration report generation job for a document library.

### [Get-SPOListVersionPolicy](Get-SPOListVersionPolicy.md)
Gets the version policy setting on the document library.

### [Get-SPOM365AgentAccessInsightsReport](Get-SPOM365AgentAccessInsightsReport.md)
This cmdlet enables the administrator to check status of all active and available Microsoft 365 Agent Insights reports when no report ID is present and to view or download a report if report ID is present.  > [!NOTE] > The feature associated with this cmdlet will be rolling out soon.

### [Get-SPOMalwareFile](Get-SPOMalwareFile.md)
Extracts and displays the malware-related information of an infected file stored in SharePoint.

### [Get-SPOMalwareFileContent](Get-SPOMalwareFileContent.md)
Gets the file stream associated with the malware-infected file stored in SharePoint.

### [Get-SPOMigrationJobProgress](Get-SPOMigrationJobProgress.md)
**Note**: This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).  This cmdlet lets you report on SPO migration jobs that are in progress.

### [Get-SPOMigrationJobStatus](Get-SPOMigrationJobStatus.md)
**Note**: This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).  Use this cmdlet to monitor the status of a submitted SharePoint Online migration job.

### [Get-SPOMultiGeoCompanyAllowedDataLocation](Get-SPOMultiGeoCompanyAllowedDataLocation.md)
Returns the SharePoint Online Multi geo allowed data locations.

### [Get-SPOMultiGeoExperience](Get-SPOMultiGeoExperience.md)
Use this cmdlet to get the multi geo experience mode.

### [Get-SPOOrgAssetsLibrary](Get-SPOOrgAssetsLibrary.md)
Displays information about all libraries designated as locations for organization assets.

### [Get-SPOOrgNewsSite](Get-SPOOrgNewsSite.md)
Lists URLs of all the configured organizational news sites. Requires Tenant administrator permissions.

### [Get-SPOPersonalSitePageCopyProgress](Get-SPOPersonalSitePageCopyProgress.md)
This cmdlet enables you to track the progress of a SharePoint page's copy operation.

### [Get-SPOPublicCdnOrigins](Get-SPOPublicCdnOrigins.md)
This cmdlet returns a list of CDN Origins in your SharePoint Online Tenant

### [Get-SPORestrictedAccessForSitesInsights](Get-SPORestrictedAccessForSitesInsights.md)
This cmdlet enables the administrator to check status of all active and available reports about insights on sites protected and access denials by restricted access control.

### [Get-SPORestrictedSiteCreation](Get-SPORestrictedSiteCreation.md)
This cmdlet allows SharePoint administrators to check the current configuration of the restricted site creation feature.

### [Get-SPORestrictedSiteCreationForApps](Get-SPORestrictedSiteCreationForApps.md)
This cmdlet allows SharePoint administrators to check the current configuration of the restricted site creation for apps feature.

### [Get-SPOServicePrioritizationAppRegistrations](Get-SPOServicePrioritizationAppRegistrations.md)
Retrieves the list of app registrations configured for service prioritization in SharePoint Online.

### [Get-SPOServicePrioritizationBillingPolicies](Get-SPOServicePrioritizationBillingPolicies.md)
Retrieves the list of billing policies configured for service prioritization in SharePoint Online. 

### [Get-SPOSite](Get-SPOSite.md)
Returns one or more site collections.

### [Get-SPOSiteCollectionAppCatalogs](Get-SPOSiteCollectionAppCatalogs.md)
Use this cmdlet to get the Site Collection App Catalog.

### [Get-SPOSiteContentMoveState](Get-SPOSiteContentMoveState.md)
This Cmdlet allows a SharePoint administrators to check the status of a site or group move.

### [Get-SPOSiteDataEncryptionPolicy](Get-SPOSiteDataEncryptionPolicy.md)
Validates the encryption of a Group Site, Team Site, or OneDrive for Business site if a Customer Key has been registered for the site.

### [Get-SPOSiteDesign](Get-SPOSiteDesign.md)
Gets details about site designs that are on the SharePoint tenant. You can specify an ID of a specific site design to retrieve. If there are no parameters listed, details about all site designs are listed.

### [Get-SPOSiteDesignRights](Get-SPOSiteDesignRights.md)
Displays a list of principals and their rights for usage of the site design. This can be used to determine the scope that your site design has with users on the tenant.

### [Get-SPOSiteDesignRun](Get-SPOSiteDesignRun.md)
Retrieves a list of site designs applied to a specified site collection.

### [Get-SPOSiteDesignRunStatus](Get-SPOSiteDesignRunStatus.md)
Retrieves and displays a list of all site script actions executed for a specified site design applied to a site.

### [Get-SPOSiteDesignTask](Get-SPOSiteDesignTask.md)
Cmdlet to get a scheduled site design script.

### [Get-SPOSiteFileVersionBatchDeleteJobProgress](Get-SPOSiteFileVersionBatchDeleteJobProgress.md)
Gets the progress of a trim job for a site collection.

### [Get-SPOSiteFileVersionExpirationReportJobProgress](Get-SPOSiteFileVersionExpirationReportJobProgress.md)
Gets the status for a file version expiration report generation job for a site collection.

### [Get-SPOSiteGroup](Get-SPOSiteGroup.md)
Gets all the groups on the specified site collection.

### [Get-SPOSiteManageVersionPolicyJobProgress](Get-SPOSiteManageVersionPolicyJobProgress.md)
Gets the status and progress for site manage version policy jobs.

### [Get-SPOSitePages](Get-SPOSitePages.md)
This cmdlet allows you to retrieve all SharePoint pages under a specific SharePoint site.

### [Get-SPOSiteRenameState](Get-SPOSiteRenameState.md)
Returns the current rename job state of a SharePoint Online Site.

### [Get-SPOSiteReview](Get-SPOSiteReview.md)
Track all site access reviews initiated from Data Access Governance (DAG) reports.

### [Get-SPOSiteScript](Get-SPOSiteScript.md)
Displays information about existing site scripts.

### [Get-SPOSiteScriptFromList](Get-SPOSiteScriptFromList.md)
Creates site script syntax from an existing SharePoint list.

### [Get-SPOSiteScriptFromWeb](Get-SPOSiteScriptFromWeb.md)
Creates site script syntax from an existing SharePoint site.

### [Get-SPOSiteUserInvitations](Get-SPOSiteUserInvitations.md)
Searches against all stored sharing links and retrieves the email invites.

### [Get-SPOSiteVersionPolicyJobProgress](Get-SPOSiteVersionPolicyJobProgress.md)
Gets the progress of setting version policy for existing document libraries on the site collection.

### [Get-SPOStorageEntity](Get-SPOStorageEntity.md)
Tenant properties allow tenant administrators to add properties in the app catalog that can be read by various SharePoint Framework components. Because tenant properties are stored in the tenant app catalog, you must provide the tenant app catalog site collection URL or the site collection app catalog URL in the following cmdlets. This cmdlet is used to get a value in the property bag.

### [Get-SPOStructuralNavigationCacheSiteState](Get-SPOStructuralNavigationCacheSiteState.md)
Get the structural navigation caching state for a site collection.

### [Get-SPOStructuralNavigationCacheWebState](Get-SPOStructuralNavigationCacheWebState.md)
Get the structural navigation caching state for a web.

### [Get-SPOTenant](Get-SPOTenant.md)
Returns SharePoint Online organization properties.

### [Get-SPOTenantCdnEnabled](Get-SPOTenantCdnEnabled.md)
Returns whether Public content delivery network (CDN) or Private CDN is enabled on the tenant level. Requires Tenant administrator permissions.

### [Get-SPOTenantCdnOrigins](Get-SPOTenantCdnOrigins.md)
Lists all the configured origins under the tenancy or under a given site. You must be a SharePoint Online administrator to run this cmdlet.

### [Get-SPOTenantCdnPolicies](Get-SPOTenantCdnPolicies.md)
Get the public or private Policies applied on your SharePoint Online Tenant. Requires Tenant administrator permissions.

### [Get-SPOTenantContentTypeReplicationParameters](Get-SPOTenantContentTypeReplicationParameters.md)
Gets content types for replication parameters

### [Get-SPOTenantLogEntry](Get-SPOTenantLogEntry.md)
Retrieves SharePoint Online company logs. This cmdlet is reserved for internal Microsoft use.

### [Get-SPOTenantLogLastAvailableTimeInUtc](Get-SPOTenantLogLastAvailableTimeInUtc.md)
Returns the most recent time when the SharePoint Online organization logs were collected.

### [Get-SPOTenantPreAuthSettings](Get-SPOTenantPreAuthSettings.md)
Gets the configuration of pre-authentication.

### [Get-SPOTenantRenameSitePrioritization](Get-SPOTenantRenameSitePrioritization.md)
Returns the list of sites that are prioritized for early execution, as part of [Advanced Tenant Rename](/sharepoint/change-your-sharepoint-domain-name#advanced-tenant-rename-preview).

### [Get-SPOTenantRenameStatus](Get-SPOTenantRenameStatus.md)
> [!IMPORTANT] > This feature is currently available to organizations that have no more than 10,000 total SharePoint sites and OneDrive accounts combined.  Get the status of the job to change the SharePoint domain name for your organization in Microsoft 365.

### [Get-SPOTenantServicePrincipalPermissionGrants](Get-SPOTenantServicePrincipalPermissionGrants.md)
Gets the collection of permission grants for the "SharePoint Online Client" service principal

### [Get-SPOTenantServicePrincipalPermissionRequests](Get-SPOTenantServicePrincipalPermissionRequests.md)
Gets the collection of permission requests for the "SharePoint Online Client" service principal

### [Get-SPOTenantSyncClientRestriction](Get-SPOTenantSyncClientRestriction.md)
Returns the current configuration status.

### [Get-SPOTenantTaxonomyReplicationParameters](Get-SPOTenantTaxonomyReplicationParameters.md)
Get the replication parameters to manage Multi-Geo taxonomy replication.

### [Get-SPOTheme](Get-SPOTheme.md)
Returns one or all theme settings from the tenant.

### [Get-SPOUnifiedGroup](Get-SPOUnifiedGroup.md)
Retrieves the Preferred Data Location for the specified Office 365 Group.

### [Get-SPOUnifiedGroupMoveState](Get-SPOUnifiedGroupMoveState.md)
Returns the state of an Office 365 Group move between Preferred Data Locations.

### [Get-SPOUser](Get-SPOUser.md)
Returns the SharePoint Online user or security group accounts that match a given search criteria.

### [Get-SPOUserAndContentMoveState](Get-SPOUserAndContentMoveState.md)
This cmdlet allows SharePoint administrators to check the status of a user or site move across geo locations.

### [Get-SPOUserOneDriveLocation](Get-SPOUserOneDriveLocation.md)
This cmdlet will return the user principal name, current location, and corresponding OneDrive for Business url, and the site ID. This cmdlet only supports Multi-Geo OneDrive sites.

### [Get-SPOWebTemplate](Get-SPOWebTemplate.md)
Displays all site templates that match the given identity.

### [Grant-SPOHubSiteRights](Grant-SPOHubSiteRights.md)
Grants rights to users or mail-enabled security groups to associate their site with a hub site.

### [Grant-SPOSiteDesignRights](Grant-SPOSiteDesignRights.md)
Used to apply permissions to a set of users or a security group, effectively scoping the visibility of the site design in the UX. They start off public, but after you set permissions, only those groups or users with permissions can access the site design.

### [Invoke-SPOMigrationEncryptUploadSubmit](Invoke-SPOMigrationEncryptUploadSubmit.md)
**Note**: This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).  Creates a new migration job in the target site collection.

### [Invoke-SPOSiteDesign](Invoke-SPOSiteDesign.md)
Applies a published site design to a specified site collection target. This allows a site design to be applied to an existing site collection. The supported site templates you can apply a site design to include: "modern" team site (with O365 group), "modern" team site (without an O365 group); communication site; classic team site; and classic publishing site.

### [Invoke-SPOSiteSwap](Invoke-SPOSiteSwap.md)
Invokes a job to swap the location of a site with another site while archiving the original site.

### [New-SPOAppBillingPolicy](New-SPOAppBillingPolicy.md)
Creates a new billing policy for an application owned by the tenant.

### [New-SPOContainerType](New-SPOContainerType.md)
This cmdlet creates a new container type of standard or trial status. The standard container type can be created with the regular billing structure or direct to customer billing structure.

### [New-SPOListFileVersionBatchDeleteJob](New-SPOListFileVersionBatchDeleteJob.md)
Queues a job to trim versions from a document library.

### [New-SPOListFileVersionExpirationReportJob](New-SPOListFileVersionExpirationReportJob.md)
Starts generating file version expiration report for a document library.

### [New-SPOMigrationEncryptionParameters](New-SPOMigrationEncryptionParameters.md)
**Note**: This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).  Creates a new random encryption key for a migration job or package.

### [New-SPOMigrationPackage](New-SPOMigrationPackage.md)
Cmdlet to create a new migration package based on source files in a local or network shared folder.  > [!NOTE] > This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see > [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).

### [New-SPOPublicCdnOrigin](New-SPOPublicCdnOrigin.md)
Creates a new public CDN on a document library in your SharePoint Online Tenant

### [New-SPOSdnProvider](New-SPOSdnProvider.md)
Adds a new Software-Defined Networking (SDN) provider

### [New-SPOServicePrioritizationBillingPolicy](New-SPOServicePrioritizationBillingPolicy.md)
Creates a new billing policy for service prioritization in SharePoint Online.

### [New-SPOSite](New-SPOSite.md)
Creates a new SharePoint Online site collection for the current company.

### [New-SPOSiteFileVersionBatchDeleteJob](New-SPOSiteFileVersionBatchDeleteJob.md)
Queues a job to trim versions for all document libraries in a site collection.

### [New-SPOSiteFileVersionExpirationReportJob](New-SPOSiteFileVersionExpirationReportJob.md)
Generates a version storage usage report for a site collection. This report can be used to understand current version storage footprint of the site.

### [New-SPOSiteGroup](New-SPOSiteGroup.md)
Creates a new group in a SharePoint Online site collection.

### [New-SPOSiteManageVersionPolicyJob](New-SPOSiteManageVersionPolicyJob.md)
Starts a background job to manage file versions and version history limits for all document libraries in the given site.

### [New-SPOSiteSharingReportJob](New-SPOSiteSharingReportJob.md)
Creates a new sharing report job.

### [Register-SPODataEncryptionPolicy](Register-SPODataEncryptionPolicy.md)
Cmdlet to register customer encryption status for your geo tenant. For more information, see [Controlling your data in Office 365 using Customer Key](/microsoft-365/compliance/controlling-your-data-using-customer-key)

### [Register-SPOHubSite](Register-SPOHubSite.md)
Enables the hub site feature on a site to make it a hub site. For more information visit [SharePoint hub sites overview](/sharepoint/dev/features/hub-site/hub-site-overview).

### [Remove-SPOAppBillingPolicy](Remove-SPOAppBillingPolicy.md)
Removes billing policy associated with the application.

### [Remove-SPOContainer](Remove-SPOContainer.md)
Sends a Container to the Recycle Bin.

### [Remove-SPOContainerType](Remove-SPOContainerType.md)
This cmdlet removes the container type specified from the tenant.

### [Remove-SPOContainerUser](Remove-SPOContainerUser.md)
This cmdlet removes the container type specified from the tenant.

### [Remove-SPOContentEventEmailAddresses](Remove-SPOContentEventEmailAddresses.md)
Removes the email addresses associated with the specified category of content event if they exist. Consequently, notification emails will no longer be sent to these addresses.

### [Remove-SPOContentSecurityPolicy](Remove-SPOContentSecurityPolicy.md)
Removes a source from the **Content Security Policy** configuration.

### [Remove-SPODataAccessGovernanceInsight](Remove-SPODataAccessGovernanceInsight.md)
This cmdlet deletes the given Data Access Governance (DAG) report.

### [Remove-SPODeletedContainer](Remove-SPODeletedContainer.md)
Permanently deletes the specified Container from the Recycle Bin. This action cannot be undone.

### [Remove-SPODeletedSite](Remove-SPODeletedSite.md)
Removes a SharePoint Online deleted site collection from the Recycle Bin.

### [Remove-SPOExternalUser](Remove-SPOExternalUser.md)
Removes a collection of external users from the tenancy's folder.

### [Remove-SPOFileRequestBrandingProfile](Remove-SPOFileRequestBrandingProfile.md)
Removes a branding profile (either primary or secondary) configured for the file request feature across the tenant.

### [Remove-SPOFontPackage](Remove-SPOFontPackage.md)
Removes a brand font package from the tenant.

### [Remove-SPOGeoAdministrator](Remove-SPOGeoAdministrator.md)
Removes a new SharePoint user or security Group in the current Multi-Geo Tenant.

### [Remove-SPOHomeSite](Remove-SPOHomeSite.md)
Removes the current SharePoint Online Home site setting.

### [Remove-SPOHubSiteAssociation](Remove-SPOHubSiteAssociation.md)
Removes a site from its associated hub site.

### [Remove-SPOHubToHubAssociation](Remove-SPOHubToHubAssociation.md)
Removes the selected hub site from its parent hub.

### [Remove-SPOListDesign](Remove-SPOListDesign.md)
Removes a list design. It no longer appears in the UI for creating a new list.

### [Remove-SPOListFileVersionBatchDeleteJob](Remove-SPOListFileVersionBatchDeleteJob.md)
Cancels further processing of a trim job for a document library.

### [Remove-SPOMigrationJob](Remove-SPOMigrationJob.md)
Cmdlet to remove a previously created migration job from the specified site collection.

### [Remove-SPOMultiGeoCompanyAllowedDataLocation](Remove-SPOMultiGeoCompanyAllowedDataLocation.md)
Use this cmdlet to remove a multi geo allowed location.

### [Remove-SPOOrgAssetsLibrary](Remove-SPOOrgAssetsLibrary.md)
Removes a library that was designated as a central location for organization assets across the tenant.

### [Remove-SPOOrgNewsSite](Remove-SPOOrgNewsSite.md)
Removes a given site from the list of organizational news sites based on its URL in your SharePoint Online Tenant

### [Remove-SPOPublicCdnOrigin](Remove-SPOPublicCdnOrigin.md)
Removes a given public CDN origin based on its identity (id) in your SharePoint Online Tenant

### [Remove-SPOSdnProvider](Remove-SPOSdnProvider.md)
Removes Software-Defined Networking (SDN) Support in your SharePoint Online tenant

### [Remove-SPOServicePrioritizationAppRegistration](Remove-SPOServicePrioritizationAppRegistration.md)
Removes an app registration from service prioritization in SharePoint Online. 

### [Remove-SPOSite](Remove-SPOSite.md)
Sends a SharePoint Online site collection to the SharePoint Online Recycle Bin.

### [Remove-SPOSiteCollectionAppCatalog](Remove-SPOSiteCollectionAppCatalog.md)
Removes the site collection app catalog.

### [Remove-SPOSiteCollectionAppCatalogById](Remove-SPOSiteCollectionAppCatalogById.md)
Removes the site collection app catalog by the id of the site collection.

### [Remove-SPOSiteDesign](Remove-SPOSiteDesign.md)
Removes a site design. It no longer appears in the UI for creating a new site.

### [Remove-SPOSiteDesignTask](Remove-SPOSiteDesignTask.md)
Command to remove a scheduled site design script.

### [Remove-SPOSiteFileVersionBatchDeleteJob](Remove-SPOSiteFileVersionBatchDeleteJob.md)
Stops further processing of site level trim job that is in-progress.

### [Remove-SPOSiteGroup](Remove-SPOSiteGroup.md)
Removes a SharePoint Online group from a site collection.

### [Remove-SPOSiteManageVersionPolicyJob](Remove-SPOSiteManageVersionPolicyJob.md)
Stops processing of the in-progress manage version policy job for the given site.

### [Remove-SPOSiteScript](Remove-SPOSiteScript.md)
Removes a site script.

### [Remove-SPOSiteUserInvitations](Remove-SPOSiteUserInvitations.md)
.

### [Remove-SPOSiteVersionPolicyJob](Remove-SPOSiteVersionPolicyJob.md)
Cancels further processing of version settings update on existing document libraries on the site collection.

### [Remove-SPOStorageEntity](Remove-SPOStorageEntity.md)
Tenant properties allow tenant administrators to add properties in the app catalog that can be read by various SharePoint Framework components. Because tenant properties are stored in the tenant app catalog, you must provide the tenant app catalog site collection URL or the site collection app catalog URL in the following cmdlets. This cmdlet is used to remove a value in the property bag.

### [Remove-SPOTenantCdnOrigin](Remove-SPOTenantCdnOrigin.md)
Removes a new origin from the Public or Private content delivery network (CDN). Requires Tenant administrator permissions.

### [Remove-SPOTenantRenameSitePrioritization](Remove-SPOTenantRenameSitePrioritization.md)
Allows removal of the prioritization previously assigned to a site for early execution, as part of [Advanced Tenant Rename](/sharepoint/change-your-sharepoint-domain-name#advanced-tenant-rename-preview).

### [Remove-SPOTenantSyncClientRestriction](Remove-SPOTenantSyncClientRestriction.md)
Disables the feature for the tenancy.

### [Remove-SPOTheme](Remove-SPOTheme.md)
Removes a theme from the theme gallery.

### [Remove-SPOUser](Remove-SPOUser.md)
Removes a user or a security group from a site collection or a group.

### [Remove-SPOUserInfo](Remove-SPOUserInfo.md)
Do not use.

### [Remove-SPOUserProfile](Remove-SPOUserProfile.md)
Remove user profile from the tenant.

### [Repair-SPOSite](Repair-SPOSite.md)
Checks and repairs the site collection and its contents.

### [Request-SPOPersonalSite](Request-SPOPersonalSite.md)
Requests that one or more users be enqueued for a Personal Site to be created.

### [Request-SPOUpgradeEvaluationSite](Request-SPOUpgradeEvaluationSite.md)
Requests to create a copy of an existing site collection for the purposes of validating the effects of upgrade without affecting the original site.

### [Restore-SPODataEncryptionPolicy](Restore-SPODataEncryptionPolicy.md)
Cmdlet to restore customer encryption status for your geo tenant when in recovery mode. For more information, see [Controlling your data in Office 365 using Customer Key](/microsoft-365/compliance/controlling-your-data-using-customer-key)

### [Restore-SPODeletedContainer](Restore-SPODeletedContainer.md)
Recovers a deleted Container from the Recycle Bin.

### [Restore-SPODeletedSite](Restore-SPODeletedSite.md)
Restores a SharePoint Online deleted site collection from the Recycle Bin.

### [Revoke-SPOHubSiteRights](Revoke-SPOHubSiteRights.md)
Revokes rights for specified principals to a hub.

### [Revoke-SPOSiteDesignRights](Revoke-SPOSiteDesignRights.md)
Revokes rights for specified principals from a site design.

### [Revoke-SPOTenantServicePrincipalPermission](Revoke-SPOTenantServicePrincipalPermission.md)
Revokes a permission that was previously granted to the "SharePoint Online Client" service principal

### [Revoke-SPOUserSession](Revoke-SPOUserSession.md)
Provides IT administrators the ability to invalidate a particular users' O365 sessions across all their devices.

### [Set-SPOApplication](Set-SPOApplication.md)
Sets or updates one or more configuration of a SharePoint Embedded application.

### [Set-SPOApplicationPermission](Set-SPOApplicationPermission.md)
Manages permissions for a guest application to access a SharePoint Embedded application.

### [Set-SPOBrowserIdleSignOut](Set-SPOBrowserIdleSignOut.md)
Sets the current configuration values for Idle session sign-out.

### [Set-SPOBuiltInDesignPackageVisibility](Set-SPOBuiltInDesignPackageVisibility.md)
Sets the visibility of the available built-in Design Packages at moment of site creation.

### [Set-SPOBuiltInFontPackageSettings](Set-SPOBuiltInFontPackageSettings.md)
Use this cmdlet to set settings of [built-in font packages](/sharepoint/brand-center-font-packages).

### [Set-SPOBuiltInSiteTemplateSettings](Set-SPOBuiltInSiteTemplateSettings.md)
Sets all or specific Microsoft-provided SharePoint site templates to be displayed or hidden in the site template gallery in your tenant. All site templates are displayed by default.

### [Set-SPOContainer](Set-SPOContainer.md)
Sets or updates one or more property values for a container in SharePoint Embedded.

### [Set-SPOContainerType](Set-SPOContainerType.md)
Sets or updates one or more property values of a trial, standard or a direct to customer billed container type.

### [Set-SPOContainerTypeConfiguration](Set-SPOContainerTypeConfiguration.md)
Sets or updates the configuration settings of a container type in SharePoint Embedded.

### [Set-SPOContainerUser](Set-SPOContainerUser.md)
Reassigns a user from their current role to a new role within a SharePoint Embedded container.

### [Set-SPOContentEventEmailAddresses](Set-SPOContentEventEmailAddresses.md)
Adds the email addresses to the specified category of content event. Consequently, notification emails will be sent to these addresses.

### [Set-SPOCopilotPromoOptInStatus](Set-SPOCopilotPromoOptInStatus.md)
Sets the Opt-In Copilot promo status for the tenant.

### [Set-SPOCrossTenantRelationship](Set-SPOCrossTenantRelationship.md)
This cmdlet sends a trust request to the tenant with whom you want to establish trust.

### [Set-SPODisableSpacesActivation](Set-SPODisableSpacesActivation.md)
Disables the SharePoint Spaces activation.

### [Set-SPOFontPackage](Set-SPOFontPackage.md)
Applies a brand font package to a SharePoint site or Viva Connections.

### [Set-SPOGeoStorageQuota](Set-SPOGeoStorageQuota.md)
This cmdlet sets the storage quota on a multi-geo tenant.

### [Set-SPOHideDefaultThemes](Set-SPOHideDefaultThemes.md)
Specifies whether the default themes should be available.

### [Set-SPOHomeSite](Set-SPOHomeSite.md)
Sets a SharePoint Site as a Home Site.

### [Set-SPOHubSite](Set-SPOHubSite.md)
Sets the hub site information such as name, logo, and description.

### [Set-SPOListVersionPolicy](Set-SPOListVersionPolicy.md)
Sets the version policy setting on the document library.

### [Set-SPOMigrationPackageAzureSource](Set-SPOMigrationPackageAzureSource.md)
Cmdlet to create Azure containers, upload migration package files into the appropriate containers and snapshot the uploaded content.

### [Set-SPOMultiGeoCompanyAllowedDataLocation](Set-SPOMultiGeoCompanyAllowedDataLocation.md)
Adds a multi-geo allowed location.

### [Set-SPOMultiGeoExperience](Set-SPOMultiGeoExperience.md)
Used to set a geo location into SPO mode.

### [Set-SPOOrgAssetsLibrary](Set-SPOOrgAssetsLibrary.md)
Updates information for a library that is designated as a location for organization assets.

### [Set-SPOOrgNewsSite](Set-SPOOrgNewsSite.md)
Marks a site as one of multiple possible tenant's organizational news sites. Requires at least SharePoint administrator permissions.

### [Set-SPORestrictedSiteCreation](Set-SPORestrictedSiteCreation.md)
Sets or updates one or more group configurations for restricting site creation.

### [Set-SPORestrictedSiteCreationForApps](Set-SPORestrictedSiteCreationForApps.md)
Sets or updates one or more group configurations for restricting site creation for apps.

### [Set-SPOServicePrioritizationAppRegistration](Set-SPOServicePrioritizationAppRegistration.md)
Updates an existing app registration for service prioritization in SharePoint Online. 

### [Set-SPOSite](Set-SPOSite.md)
Sets or updates one or more properties' values for a site collection.

### [Set-SPOSiteArchiveState](Set-SPOSiteArchiveState.md)
Sets the archived state of the site. Can be used to archive and reactivate sites.

### [Set-SPOSiteDesign](Set-SPOSiteDesign.md)
Updates a previously uploaded site design.

### [Set-SPOSiteGroup](Set-SPOSiteGroup.md)
Updates the SharePoint Online owner and permission levels on a group inside a site collection.

### [Set-SPOSiteOffice365Group](Set-SPOSiteOffice365Group.md)
Connects a top-level SPO site collection to a new Microsoft 365 Group.

### [Set-SPOSiteScript](Set-SPOSiteScript.md)
Updates a previously uploaded site script.

### [Set-SPOSiteScriptPackage](Set-SPOSiteScriptPackage.md)
Updates a previously uploaded site script package. The package file must be a zip archive containing all the files necessary for the site script. A file called "manifest.json" with script actions must be present in this zip file.

### [Set-SPOStorageEntity](Set-SPOStorageEntity.md)
Tenant properties allow tenant administrators to add properties in the app catalog that can be read by various SharePoint Framework components. Because tenant properties are stored in the tenant app catalog, you must provide the tenant app catalog site collection URL or the site collection app catalog URL in the following cmdlets.

### [Set-SPOStructuralNavigationCacheSiteState](Set-SPOStructuralNavigationCacheSiteState.md)
Enable or disable caching for all webs in a site collection.

### [Set-SPOStructuralNavigationCacheWebState](Set-SPOStructuralNavigationCacheWebState.md)
Enable or disable caching for a web in a site collection.

### [Set-SPOTenant](Set-SPOTenant.md)
Sets properties on the SharePoint Online organization.

### [Set-SPOTenantCdnEnabled](Set-SPOTenantCdnEnabled.md)
Enables or disables Public content delivery network (CDN) or Private CDN on the tenant level. Requires Tenant administrator permissions.

### [Set-SPOTenantCdnPolicy](Set-SPOTenantCdnPolicy.md)
Sets the content delivery network (CDN) policies at the tenant level.

### [Set-SPOTenantContentTypeReplicationParameters](Set-SPOTenantContentTypeReplicationParameters.md)
Select content types for replication

### [Set-SPOTenantPreAuthSettings](Set-SPOTenantPreAuthSettings.md)
Sets the configuration of pre-authentication.

### [Set-SPOTenantRenameSitePrioritization](Set-SPOTenantRenameSitePrioritization.md)
Allows prioritization of a site for early execution, as part of [Advanced Tenant Rename](/sharepoint/change-your-sharepoint-domain-name#advanced-tenant-rename-preview).

### [Set-SPOTenantSyncClientRestriction](Set-SPOTenantSyncClientRestriction.md)
Controls tenant-wide options and restrictions specific to syncing files.

### [Set-SPOTenantTaxonomyReplicationParameters](Set-SPOTenantTaxonomyReplicationParameters.md)
Select groups for replication

### [Set-SPOUnifiedGroup](Set-SPOUnifiedGroup.md)
Sets the Preferred Data Location (PDL) for the specified Office 365 Group. The customer tenant must be multi-geo enabled.

### [Set-SPOUser](Set-SPOUser.md)
Configures properties on an existing user.

### [Set-SPOWebTheme](Set-SPOWebTheme.md)
Sets the theme for a SharePoint site.

### [Start-SPOAuditDataCollectionForActivityInsights](Start-SPOAuditDataCollectionForActivityInsights.md)
This cmdlet starts collecting audit data for reports on activities from the last 28 days, such as sharing link reports and content shared with everyone except external users, from the SharePoint admin center.

### [Start-SPOCopilotAgentInsightsReport](Start-SPOCopilotAgentInsightsReport.md)
Using this cmdlet, administrators may trigger the build of a new Copilot agent insight report for the specified number of days.  > [!NOTE] > The feature associated with this cmdlet will be rolling out soon.

### [Start-SPODataAccessGovernanceInsight](Start-SPODataAccessGovernanceInsight.md)
This cmdlet generates Data Access Governance (DAG) reports meant to provide insights into potential oversharing of sensitive data in SharePoint and/or OneDrive for Business. SharePoint Advanced Management (SAM) license is required to run these reports.

### [Start-SPOEnterpriseAppInsightsReport](Start-SPOEnterpriseAppInsightsReport.md)
This cmdlet enables administrator to trigger the build of a new enterprise application insights report for the last N days.

### [Start-SPOInformationBarriersInsightsReport](Start-SPOInformationBarriersInsightsReport.md)
Generates a new report to identify and discover the usage patterns of Information Barriers (IB) across SharePoint sites and OneDrive accounts in the organization.

### [Start-SPOM365AgentAccessInsightsReport](Start-SPOM365AgentAccessInsightsReport.md)
Using this cmdlet, administrators may trigger the build of a new Microsoft 365 agent insight report for the specified number of days.  > [!NOTE] > The feature associated with this cmdlet will be rolling out soon.

### [Start-SPORestrictedAccessForSitesInsights](Start-SPORestrictedAccessForSitesInsights.md)
This cmdlet enables administrator to trigger the build of a new restricted access control insights report for the data from last 28 days.

### [Start-SPOSiteContentMove](Start-SPOSiteContentMove.md)
Start a job to move a particular user or group of users to be moved across geo locations relative to the one that executes the command

### [Start-SPOSiteOpticalCharacterRecognitionBackfill](Start-SPOSiteOpticalCharacterRecognitionBackfill.md)
> [!important] > Optical Character Recognition (OCR) is a pay-as-you-go feature. Running this cmdlet will incur cost for your organization.  Initiates a job to trigger the OCR process for all files for the selected site.

### [Start-SPOSiteRename](Start-SPOSiteRename.md)
> [!NOTE] > This Feature is part of the Admin Center Preview. If your tenant is not part of the Admin Center Preview, you will get an error when trying to run this cmdlet.  Starts a job to rename a site. You can change the URL, and optionally the site title along with changing the URL, of a site on a SharePoint Online collection.

### [Start-SPOSiteReview](Start-SPOSiteReview.md)
SharePoint Administrators can delegate access governance of sites to corresponding site owners through 'site access review'. The 'access review' is under the context of oversharing as specified in the Data Access Governance (DAG) reports. Read all about site access review [here](/sharepoint/site-access-review).

### [Start-SPOTenantRename](Start-SPOTenantRename.md)
> [!IMPORTANT] > This feature is currently available to organizations that have no more than 10,000 total SharePoint sites and OneDrive accounts combined.  Additionally, tenant renaming capability is not available for GCC, GCC High, and DoD.  Starts a job to change the SharePoint domain name for your organization in Microsoft 365. For example, if the name of your organization changes from "Contoso" to "Fabrikam," you can change contoso.sharepoint.com to fabrikam.sharepoint.com.  > [!WARNING] > Changing your SharePoint domain name might take several hours to days depending on the number of sites and OneDrive users that you have. We strongly recommend that you make this change during a period of low usage (like a weekend) and tell users to avoid accessing SharePoint and OneDrive content during the change. In addition, any actions that create new OneDrives and sites (such as creating a new team or private channel in Microsoft Teams) will be temporarily blocked during the rename.

### [Start-SPOUnifiedGroupMove](Start-SPOUnifiedGroupMove.md)
Initiates the move of an Office 365 Group to a new geo location

### [Start-SPOUserAndContentMove](Start-SPOUserAndContentMove.md)
Starts the ability to move a user closer to their sites.

### [Stop-SPOAuditDataCollectionForActivityInsights](Stop-SPOAuditDataCollectionForActivityInsights.md)
This cmdlet stops collecting audit data for reports on activities from the last 28 days, such as sharing link reports and content shared with everyone except external users, from the SharePoint admin center.

### [Stop-SPOSiteContentMove](Stop-SPOSiteContentMove.md)
Stops a job to move a particular user or group of users to be moved across geo locations relative to the one that executes the command.

### [Stop-SPOTenantRename](Stop-SPOTenantRename.md)
> [!IMPORTANT] > This feature is currently available to organizations that have no more than 10,000 total SharePoint sites and OneDrive accounts combined.  Cancels the scheduled job to change the SharePoint domain name for your organization in Microsoft 365.  > [!NOTE] > If the job to change the SharePoint domain name is already in progress, then it cannot be canceled or stopped.

### [Stop-SPOUserAndContentMove](Stop-SPOUserAndContentMove.md)
In a Multi-Geo company, stops the ability to move a user's content related objects in a SharePoint Online Tenant

### [Submit-SPOMigrationJob](Submit-SPOMigrationJob.md)
**Note**: This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).  Cmdlet to submit a new migration job referenced to a previously uploaded package in Azure Blob storage into to a site collection.

### [Switch-SPOFileRequestBrandingProfiles](Switch-SPOFileRequestBrandingProfiles.md)
Switches the primary and secondary file request branding profiles configured for the tenant.

### [Test-SPOSite](Test-SPOSite.md)
Tests a SharePoint Online site collection.

### [Unlock-SPOSensitivityLabelEncryptedFile](Unlock-SPOSensitivityLabelEncryptedFile.md)
It removes encryption on a Sensitivity label encrypted file in SharePoint Online. No need to download the file.

### [Unregister-SPOHubSite](Unregister-SPOHubSite.md)
Disables the hub site feature on a site.

### [Update-SPODataEncryptionPolicy](Update-SPODataEncryptionPolicy.md)
Updates customer encryption status for a geo tenant.

### [Update-UserType](Update-UserType.md)
Updates the specified user's UserType value from Microsoft Entra ID.
