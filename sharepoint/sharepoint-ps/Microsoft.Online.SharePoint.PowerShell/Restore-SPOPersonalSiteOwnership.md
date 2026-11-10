---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/restore-spopersonalsiteownership
applicable: SharePoint Online
title: Restore-SPOPersonalSiteOwnership
schema: 2.0.0
author: bgbggoogol-a11y
ms.author: burrag
ms.reviewer:
---

# Restore-SPOPersonalSiteOwnership

## SYNOPSIS

Restores ownership of an existing OneDrive site and reconnects the owner's SharePoint user profile without deleting the previously associated OneDrive.

## SYNTAX

```
Restore-SPOPersonalSiteOwnership [[-Identity] <SpoSitePipeBind>] [-IgnoreArchive] [-IgnoreSiteLock]
 [-MySiteId <Guid>] [-OldOwnerUPN <String>] [-OwnerObjectId <Guid>] [-OwnerUPN <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

> [!IMPORTANT]
> This reference describes an unreleased cmdlet. The cmdlet isn't registered in the published SharePoint Online Management Shell. Release availability and end-to-end validation are pending.

The `Restore-SPOPersonalSiteOwnership` cmdlet restores ownership and profile association for an existing OneDrive site in the connected tenant. It sets the specified user as the primary site owner and a site collection administrator, grants Full Control on the root web when needed, and reconnects the user's SharePoint user profile to that site.

Use this cmdlet to repair an existing OneDrive's ownership and profile association. It doesn't create a OneDrive, restore a deleted site from the recycle bin, restore a deleted Microsoft Entra user, or copy content between sites. It isn't a secondary-contact or manager access-delegation command.

Connect to the tenant's SharePoint admin service by using `Connect-SPOService`. Your account must have permission to update the selected site. The new owner must exist in the same tenant and have an existing SharePoint user profile that the service can retrieve by the user's account claim. The selected site must be an existing OneDrive site.

The service resolves the new owner's current directory identity before repairing ownership and the site's cached user identity. The profile's stored directory object ID and binary user identifier aren't used as prerequisites for recovery: differences can reflect delayed synchronization. The cmdlet doesn't create a missing profile or repair these profile identity properties.

The profile update is limited to its personal-site association (`PersonalSpace`). The cmdlet also updates the selected site's reciprocal profile identifier. It preserves unrelated profile properties, including feed association, personal-site capabilities, and personal-site creation state.

For Multi-Geo tenants, the cmdlet checks the site's host against the new owner's preferred data location and the available tenant location configuration. If either is absent or the location configuration is empty, the check uses the selected site's current host. When no configuration entry matches the preferred location, it uses the single configured location or the tenant's unambiguous default location. If a location can't be selected unambiguously or its host is invalid, the checks fail. The cmdlet doesn't move sites between locations.

Specify the target by using `-Identity` or `-MySiteId`, and the new owner by using `-OwnerUPN` or `-OwnerObjectId`. A target and an owner are required even though the individual parameters are optional. If you supply both forms of an identity, `-MySiteId` takes precedence over `-Identity`, and `-OwnerObjectId` takes precedence over `-OwnerUPN`. The ignored URL or UPN isn't used to cross-check the supplied ID.

If the new owner's profile already references another OneDrive, the cmdlet returns that URL in `PreviousPersonalSiteUrl` and changes the profile association to the selected site. It doesn't open, recycle, or delete the previously associated site, and it doesn't move that site's content. The returned URL doesn't establish the previous site's current availability or access permissions.

The cmdlet also cancels pending personal-site deletion scheduling for the selected site, repairs the owner's cached site identity when needed, and submits license reevaluation and directory URL updates as applicable. It doesn't assign a Microsoft 365 license.

The operation applies repeatable corrections across multiple stages, but isn't a single transaction. If a stage fails, earlier changes can remain. Review the returned progress before deciding whether to retry. The cmdlet stops if its safety checks detect an unexpected change to the owner identity, site ownership, or profile association during the operation.

Run `-WhatIf` first to perform authorized read-only checks and inspect the previous association. These checks don't reserve the site or guarantee that a later recovery attempt will succeed. See **OUTPUTS** for the result fields and stage order.

## EXAMPLES

### Example 1: Check recovery without making changes

```powershell
Connect-SPOService -Url "https://contoso-admin.sharepoint.com"

$result = Restore-SPOPersonalSiteOwnership `
    -Identity "https://contoso-my.sharepoint.com/personal/user_contoso_com" `
    -OwnerUPN "user@contoso.com" `
    -WhatIf

$result | Format-List State, Stage, PreviousPersonalSiteUrl, CompletedStages, PendingStages, FailedStage, ErrorCode, ErrorMessage
```

This example checks the site and owner and reads the owner's current OneDrive association. It doesn't apply recovery changes. Successful checks return `State = WhatIf`, with `Validation` and `ReadOnlyChecks` completed and the eight recovery stages pending.

Unlike a preview that only displays a local message, `-WhatIf` contacts the service and returns a result object. It requires a working connection and the same site-update authorization as recovery.

### Example 2: Restore ownership by using IDs

```powershell
$result = Restore-SPOPersonalSiteOwnership `
    -MySiteId "11111111-1111-4111-8111-111111111111" `
    -OwnerObjectId "22222222-2222-4222-8222-222222222222"

$result | Format-List *
```

This example restores the selected OneDrive's ownership to the user identified by their Microsoft Entra object ID. Replace both example IDs with the actual IDs. Review the confirmation prompt before continuing.

The result includes the previous profile association and recovery progress. A successful result doesn't mean that background license processing or directory changes have finished propagating.

### Example 3: Disconnect a specified old profile

```powershell
$result = Restore-SPOPersonalSiteOwnership `
    -Identity "https://contoso-my.sharepoint.com/personal/former_user_contoso_com" `
    -OwnerUPN "restored.user@contoso.com" `
    -OldOwnerUPN "former.user@contoso.com"
```

This example also disconnects the specified old profile if it still references the selected OneDrive. If that profile doesn't exist or references a different site, the disconnection stage makes no changes. The old and new profiles must be different.

This parameter doesn't delete the old user, the old profile, or either user's OneDrive content.

### Example 4: Handle a reported recovery failure

```powershell
$result = Restore-SPOPersonalSiteOwnership `
    -Identity "https://contoso-my.sharepoint.com/personal/user_contoso_com" `
    -OwnerUPN "user@contoso.com" `
    -ErrorAction Stop

if ($result.State -eq "Failed") {
    $result | Format-List CompletedStages, FailedStage, PendingStages, ErrorCode, ErrorMessage, PreviousPersonalSiteUrl
    throw ("Ownership recovery failed at stage '{0}': {1}" -f $result.FailedStage, $result.ErrorMessage)
}
```

This example checks the returned state instead of relying only on PowerShell error handling. A recovery result with `State = Failed` isn't automatically converted into a terminating PowerShell error. Connection, authorization, request-validation, and other exceptions can still raise PowerShell errors.

Resolve the reported problem and run read-only checks again before retrying. Don't assume that a failed stage made no changes or that earlier completed stages were rolled back.

## PARAMETERS

### -Confirm

> Applicable: SharePoint Online

Prompts for confirmation before applying recovery. This is a high-impact operation, so PowerShell can prompt even when you don't specify `-Confirm`, depending on your confirmation preference.

If you decline confirmation, the cmdlet sends no recovery or read-only-check request and returns no result object.

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

### -Identity

> Applicable: SharePoint Online

Specifies the HTTPS URL of the existing OneDrive site to repair. Use `-Identity` or `-MySiteId` to select the target. The URL must not contain embedded credentials, a query string, or a fragment.

If you also supply a nonempty `-MySiteId`, the cmdlet uses that ID and ignores `-Identity`.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases: MySiteUrl

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreArchive

> Applicable: SharePoint Online

Allows recovery to access the selected site despite its archive lock. This switch doesn't bypass tenant security restrictions or replace an unarchive operation.

Use this switch only when you've determined that bypassing the archive lock is appropriate for the recovery.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: IgnoreSiteArchiveLock

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSiteLock

> Applicable: SharePoint Online

Allows recovery to access the selected site despite its ordinary site lock. This switch doesn't bypass tenant security restrictions or change the site's configured lock state.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MySiteId

> Applicable: SharePoint Online

Specifies the ID of the existing OneDrive site to repair. Use `-MySiteId` or `-Identity` to select the target.

A nonempty ID takes precedence over `-Identity`. The selected site must belong to the connected tenant.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: SiteId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OldOwnerUPN

> Applicable: SharePoint Online

Specifies an old owner's user principal name (UPN). The cmdlet disconnects this profile only if it exists and still references the selected OneDrive.

If the profile is absent or references another site, this stage makes no changes. Specifying the new owner's profile as the old profile causes the request to fail.

Disconnection clears only the old profile's personal-site association (`PersonalSpace`). It preserves the profile's other properties and doesn't delete the user profile, user account, or site content.

Omit this parameter when you don't need to disconnect a specific old profile.

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

### -OwnerObjectId

> Applicable: SharePoint Online

Specifies the new owner's Microsoft Entra user object ID. Use `-OwnerObjectId` or `-OwnerUPN` to select the new owner.

A nonempty object ID takes precedence over `-OwnerUPN`. The service resolves the user's current UPN and site identity from this object ID. The user must belong to the connected tenant and have an existing SharePoint user profile retrievable by the resolved account claim.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OwnerUPN

> Applicable: SharePoint Online

Specifies the new owner's UPN, such as `user@contoso.com`.

If you also supply a nonempty `-OwnerObjectId`, the cmdlet uses that object ID and ignores `-OwnerUPN`.

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

### -WhatIf

> Applicable: SharePoint Online

Performs authorized read-only checks and returns the previous OneDrive association and progress without applying recovery changes.

The cmdlet sends a read-only request to the service. It doesn't change ownership, grant permissions, disconnect profiles, cancel deletion scheduling, or submit recovery updates.

Successful checks return `State = WhatIf` and leave the recovery stages in `PendingStages`. If the checks fail, inspect the error or returned failure result. A successful check doesn't guarantee that conditions will remain unchanged before a later recovery request.

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

This cmdlet supports PowerShell common parameters. See [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

This cmdlet doesn't accept pipeline input.

## OUTPUTS

### Microsoft.Online.SharePoint.TenantAdministration.SPOPersonalSiteOwnershipRestoreResult

Returns one result object when the service returns a recovery or read-only-check result.

| Property | Type | Description |
| --- | --- | --- |
| `State` | String | `Succeeded`, `Failed`, or `WhatIf`. A successful read-only check isn't a completed recovery. |
| `Stage` | String | The last stage reached, whether it completed or failed. |
| `CompletedStages` | String[] | Stages that returned successfully, including stages that required no changes. |
| `FailedStage` | String | The stage that failed, or null when no stage failed. A failed stage can have partial effects. |
| `PendingStages` | String[] | Stages not attempted, in execution order. Excludes the failed stage. Successful `-WhatIf` leaves all recovery stages pending. |
| `ErrorCode` | Int32 | The failure's HResult, or zero when recovery or read-only checks succeed. |
| `ErrorMessage` | String | The returned error message, or null when no recovery failure occurred. Some failures provide an exception type instead of detailed service information. |
| `PreviousPersonalSiteUrl` | String | The new owner's profile-associated OneDrive URL captured before recovery, or null for a successfully read absent association. If checks failed before capture, null doesn't establish that no association exists. |

The customer-visible stages run in this order:

| Stage | Behavior |
| --- | --- |
| `Validation` | Checks the supplied target and owner selection. |
| `ReadOnlyChecks` | Checks site, directory, profile, location, and identity requirements; captures the previous OneDrive association. |
| `OldProfile` | Disconnects the specified old profile when it still references the target. Otherwise, makes no changes. |
| `DeletionSchedule` | Cancels pending personal-site deletion scheduling for the target. |
| `Ownership` | Sets the primary site owner and site collection administrator, grants root-web Full Control when needed, and updates the root web's author. |
| `OwnerIdentity` | Repairs the owner's cached site identity in place when needed, retaining the site-user ID and its role assignments. Fails if another site user already has the intended identity. |
| `ProfileReconnection` | Repairs the new owner's profile's personal-site association and records the profile identifier on the selected site. Doesn't repair profile identity or other profile properties. |
| `LicenseReevaluation` | Queues license reevaluation when required. Doesn't assign a license or wait for reevaluation to finish. |
| `DirectoryUrlPublication` | Submits the owner's OneDrive URL update to Microsoft Entra ID. |
| `CompletionVerification` | Verifies ownership, the target profile association, and removal from the personal-site deletion queue. |

Completed submission stages don't guarantee that background processing has finished or that directory changes have propagated. Use the returned progress rather than inferring success from a command completing without an exception.

Recovery also attempts to refresh service-side site registration on a best-effort basis. A refresh failure doesn't necessarily fail recovery, and a successful result doesn't guarantee that all site registration has converged. This refresh isn't reported as a separate stage.

## NOTES

This operation changes ownership of one existing OneDrive. Changing the primary owner can remove the previous owner's site collection administrator status when that user isn't the secondary contact. The cmdlet doesn't explicitly remove that user's other role assignments or group memberships. Review the previous owner's effective access after recovery.

Repeating recovery reapplies the required corrections toward the same ownership and profile state; an already-correct profile association doesn't skip all subsequent work. A retry can submit directory updates again. License reevaluation uses a stable work-item identity to avoid duplicate pending requests. Fresh safety checks still apply, and a repeated request can fail if its prerequisites changed.

For a storage-quota-related failure during the ownership stage, the cmdlet can retry once with a bounded temporary quota increase. It attempts to restore and verify the original quota settings, including when the retry fails. A conflicting quota change or a restoration failure causes the stage to fail; recovery doesn't promise that all changes were rolled back.

The cmdlet doesn't accept bulk input. Review each target and its returned result separately.

## RELATED LINKS

[Connect-SPOService](Connect-SPOService.md)

[Get-SPOSite](Get-SPOSite.md)

[Restore-SPODeletedSite](Restore-SPODeletedSite.md)

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
