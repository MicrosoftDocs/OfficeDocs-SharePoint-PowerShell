---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/Set-SPOApplication
title: Set-SPOApplication
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Set-SPOApplication

## SYNOPSIS

Sets or updates one or more configuration of a SharePoint Embedded application.

## SYNTAX

```
Set-SPOApplication [-OwningApplicationId] <Guid> [[-SharingCapability] <SharingCapabilities>]
 [[-OverrideTenantSharingCapability] <Boolean>]
 [[-CopilotEmbeddedChatHosts] <System.Collections.Generic.List`1[System.String]>]
 [[-ItemMajorVersionLimit] <Int>]
 [[-EnableAutoExpirationVersionTrim] <Boolean>] [[-ExpireVersionsAfterDays] <Int>]
 [[-FileTypesForVersionExpiration] <String[]>]
 [[-RemoveVersionExpirationFileTypeOverride] <String[]>]
 [<CommonParameters>]
```

## DESCRIPTION

`Set-SPOApplication` cmdlet is used to set the configuration properties of a specific application, determined by the `OwningApplicationId`.

You must be a SharePoint Embedded Administrator to run this cmdlet.

> [!NOTE]
> The OwningApplicationId for Microsoft Loop is `a187e399-0c36-4b98-8f04-1edc167a0996`.
> The OwningApplicationId for Microsoft Designer is `5e2795e3-ce8c-4cfb-b302-35fe5cd01597`.

To invite people outside your organization, please make sure [Microsoft Entra B2B](/sharepoint/sharepoint-azureb2b-integration) is enabled.

## EXAMPLES

### Example 1

```powershell
Set-SPOApplication -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 -OverrideTenantSharingCapability $false
```

This example disables the override sharing capability, aligning this SharePoint Embedded application's sharing settings with sharing capability of the SharePoint Online.

### Example 2

```powershell
Set-SPOApplication -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 -OverrideTenantSharingCapability $true -SharingCapability Disabled
```

This example enables the override, restricting file sharing within the SharePoint Embedded application to internal company users only, regardless of the broader SharePoint Online tenant settings.

### Example 3

```powershell
Set-SPOTenant -EnableAzureADB2BIntegration $true
Set-SPOApplication -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 -OverrideTenantSharingCapability $true -SharingCapability ExternalUserandGuestSharing
```
This example demonstrates how to enable file sharing within the SharePoint Embedded application for external users. Note that B2B integration must be enabled to allow guest invitations to SharePoint Embedded apps.

### Example 4

```powershell
Set-SPOApplication -OwningApplicationId 423poi45 -CopilotEmbeddedChatHosts "https://localhost:3000 https://contoso.sharepoint.com https://fabrikam.com"
```
This example sets the host URLs for the application with Id 423poi45.

### Example 5

```powershell
Set-SPOApplication -OwningApplicationId 423poi45 -ItemMajorVersionLimit 1000
```
This example sets the ItemMajorVersionLimit to 1000.

### Example 6

```powershell
Set-SPOApplication -OwningApplicationId 423poi45 -EnableAutoExpirationVersionTrim $true
```
This example enables automatic version history trimming for the application's containers. When automatic trimming is enabled, `ExpireVersionsAfterDays` and `ItemMajorVersionLimit` are managed automatically and cannot be set at the same time.

### Example 7

```powershell
Set-SPOApplication -OwningApplicationId 423poi45 -EnableAutoExpirationVersionTrim $false -ItemMajorVersionLimit 500 -ExpireVersionsAfterDays 180
```
This example disables automatic trimming and sets a manual version policy. When `EnableAutoExpirationVersionTrim` is `$false`, both `ItemMajorVersionLimit` and `ExpireVersionsAfterDays` must be specified.

### Example 8

```powershell
Set-SPOApplication -OwningApplicationId 423poi45 -ExpireVersionsAfterDays 365 -FileTypesForVersionExpiration "docx","xlsx"
```
This example applies the version-expiration policy to the specified file types.

### Example 9

```powershell
Set-SPOApplication -OwningApplicationId 423poi45 -RemoveVersionExpirationFileTypeOverride "docx","xlsx"
```
This example removes the file-type version-expiration overrides for the specified file types. `RemoveVersionExpirationFileTypeOverride` cannot be combined with any other version policy parameter.

## PARAMETERS

### -CopilotEmbeddedChatHosts

This parameter is used to add host URLs allowed to use the SharePoint Embedded application's declarative agent experience. This will always be a subset of permissible URLs set by the application's developer. To check the list of permissible URLs, use the `Get-SPOApplication` cmdlet.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideTenantSharingCapability

This setting allows the application to independently set its sharing capabilities, overriding the tenant-level settings of SharePoint Online. Options:

- False (default) - The application follows the tenant-level sharing capability
- True - The application's sharing settings are independent of the tenant level sharing capability

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OwningApplicationId

This parameter specifies the ID of the SharePoint Embedded application.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ItemMajorVersionLimit

This parameter is used to override ItemMajorVersionLimit for container types. Valid values are between 1 and 50000.

```yaml
Type: Int
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoExpirationVersionTrim

Enables or disables automatic file version history trimming for the SharePoint Embedded application's containers.

- `$true` - Version history limits are managed automatically. `ExpireVersionsAfterDays` and `ItemMajorVersionLimit` cannot be specified at the same time.
- `$false` - A manual version policy is used. Both `ItemMajorVersionLimit` and `ExpireVersionsAfterDays` must be specified.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpireVersionsAfterDays

The number of days after which file versions expire. A value of 0 means versions never expire. Otherwise the value must be between 30 and 36500. This parameter cannot be used when `EnableAutoExpirationVersionTrim` is `$true`.

```yaml
Type: Int
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileTypesForVersionExpiration

The file types whose version-expiration policy should be updated. The array cannot be empty, and at least one of `EnableAutoExpirationVersionTrim`, `ItemMajorVersionLimit`, or `ExpireVersionsAfterDays` must also be specified.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveVersionExpirationFileTypeOverride

The file-type version-expiration overrides to remove. The array cannot be empty. This parameter is exclusive and cannot be combined with `FileTypesForVersionExpiration`, `EnableAutoExpirationVersionTrim`, `ItemMajorVersionLimit`, or `ExpireVersionsAfterDays`.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingCapability

Determines what level of sharing is available for the SharePoint Embedded Application.

The valid values are:

- ExternalUserAndGuestSharing (default) - External user sharing (share by email) and guest link sharing are both enabled.
- Disabled - External user sharing (share by email) and guest link sharing are both disabled.
- ExternalUserSharingOnly - External user sharing (share by email) is enabled, but guest link sharing is disabled.
- ExistingExternalUserSharingOnly - Only guests already in your organization's directory.

The default setting is None, meaning the application follows the SharePoint Online tenant-level sharing settings. Use the `Get-SPOTenant` cmdlet to view these settings.

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SharingCapabilities
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, ExternalUserSharingOnly, ExternalUserAndGuestSharing, ExistingExternalUserSharingOnly

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOApplication](Get-SPOApplication.md)

[Set-SPOTenant](set-spotenant.md)
