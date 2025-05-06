---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Set-SPOContainerTypeConfiguration
applicable: SharePoint Online
title: Set-SPOContainerTypeConfiguration
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Set-SPOContainerTypeConfiguration

## SYNOPSIS

Sets or updates the configuration settings of a container type in SharePoint Embedded.

## SYNTAX
```powershell
Set-SPOContainerTypeConfiguration -ContainerTypeId <Guid> [-DiscoverabilityDisabled <Boolean>]
 [-SharingRestricted <Boolean>] [-ApplicationRedirectUrl <String>] [-WhoCanShareAnonymousAllowList <Guid[]>]
 [-WhoCanShareAuthenticatedGuestAllowList <Guid[]>] [-OverrideTenantWhoCanShareAnonymousAllowList <Boolean>]
 [-OverrideTenantWhoCanShareAuthenticatedGuestAllowList <Boolean>]
```

## DESCRIPTION

For any parameters passed in, the `Set-SPOContainerTypeConfiguration` cmdlet sets or updates the settings for a container type created under a SharePoint Embedded application.

You must be a SharePoint Embedded Administrator to run this cmdlet. 

## EXAMPLES

### Example 1

```powershell
Set-SPOContainerTypeConfiguration -ContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604e4 -DiscoverabilityDisabled $false
```

Example 1 turns on discoverability for this container type. All content created within this container type will be discoverable in the Microsoft 365 experience, including on office.com, onedrive.com, recommended files, and other intelligent discovery experiences.

### Example 2

```powershell
Set-SPOContainerTypeConfiguration -ContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604e4 -SharingRestricted $false
```

Example 2 turns on an open sharing model for this container type. Any container members and guest users with edit permissions can share files created within the container type.

### Example 3

```powershell
Set-SPOContainerTypeConfiguration -ContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604e4 -OverrideTenantWhoCanShareAnonymousAllowList $true -WhoCanShareAnonymousAllowList <guids> 
```

Example 3 overrides the tenant-level `WhoCanShareAnonymousAllowList`.

### Example 4

```powershell
Set-SPOContainerTypeConfiguration -ContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604e4 -OverrideTenantWhoCanShareAnonymousAllowList $true –WhoCanShareAnonymousAllowList $null -OverrideTenantWhoCanShareAuthenticatedGuestAllowList $true –WhoCanShareAuthenticatedGuestAllowList $null
```

Example 4 overrides the tenant-level `WhoCanShareAnonymousAllowList` and `WhoCanShareAuthenticatedGuestAllowList` with null values, which bypass the check. This has the effect of no longer restricting external sharing privileges to members of specific security groups.

### Example 5

```powershell
Set-SPOContainerTypeConfiguration -ContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604e4 -OverrideTenantWhoCanShareAuthenticatedGuestAllowList $true –WhoCanShareAuthenticatedGuestAllowList $null 
```

Example 5 overrides the tenant-level `WhoCanShareAuthenticatedGuestAllowList` with a null value, while leaving the `WhoCanShareAnonymousAllowList` untouched. This has the effect of no longer restricting the privilege of sharing to authenticated guests to members of specific security groups.
>>>>>>> main

## PARAMETERS

### -DiscoverabilityDisabled

As a SharePoint Administrator or Global Administrator in Microsoft 365, you can control how your content appears in the Microsoft 365 experience. The default value for this parameter is True, which hides the SharePoint Embedded application content throughout the Microsoft 365 environment, including on office.com, onedrive.com, in recommended sections, or through other Microsoft intelligent file discovery features.
If you opt into the Microsoft 365 experience, your files will be integrated into Microsoft 365 environment, participating in intelligent file discovery.

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Applicable: SharePoint Embedded
Position: Named
Required: False
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharingRestricted

SharePoint Embedded offers a role-based sharing model that allows developers to configure file-sharing permissions based on container permission roles, offering a choice between a restrictive and an open sharing model. The open sharing model allows any container members and guest users with edit permissions to share files. The restrictive sharing model allows only container members who are either Owners or Managers to share files.
 
PARAMVALUE: $true | $false

```yaml
Type: Boolean
Applicable: SharePoint Embedded
Position: Named
Required: False
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```
### -ApplicationRedirectUrl

This parameter specifies the url of that the application should be redirected to. 

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

### -ContainerTypeId

This parameter specifies the ID of the container type corresponding to the SharePoint Embedded application.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### -OverrideTenantWhoCanShareAnonymousAllowList

This setting determines if the container type `WhoCanShareAnonymousAllowList` overrides the tenant-level `WhoCanShareAnonymousAllowList`. The default value for this parameter is false.

PARAMVALUE: True | False

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

### -OverrideTenantWhoCanShareAuthenticatedGuestAllowList

This setting determines if the container type `WhoCanShareAuthenticatedGuestAllowList` overrides the tenant-level `WhoCanShareAuthenticatedGuestAllowList`. The default value for this parameter is false.

PARAMVALUE: True | False

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

### -WhoCanShareAnonymousAllowList

Sets a container type-specific list of security groups who are allowed to share with anonymous (non-authenticated) users as well as authenticated guest users. This must be set in conjunction with `OverrideTenantWhoCanShareAnonymousAllowList`.

> [!NOTE]
> This allow list only accepts security groups, and not Microsoft 365 Groups.

Each security group is denoted by its GUID object ID. To set this list to be a specific security group, you need to enter its GUID as the parameter. You can enter multiple GUIDs by using a comma to separate them. To skip the check and allow all security groups to share to anyone, set this allow list and the `WhoCanShareAuthenticatedGuestAllowList` to null arrays. 

```yaml
Type: Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhoCanShareAuthenticatedGuestAllowList

Sets a container type-specific list of security groups who are allowed to share with authenticated guest users at the container level. This must be set in conjunction with `OverrideTenantWhoCanShareAuthenticatedGuestAllowList`.

> [!NOTE]
> This allow list only accepts security groups, and not Microsoft 365 Groups.

Each security group is denoted by its GUID object ID. To set this list to be a specific security group, you need to enter its GUID as the parameter. You can enter multiple GUIDs by using a comma to separate them. To skip the check and allow all security groups to share to authenticated guests, set this allow list to a null array.


```yaml
Type: Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


## RELATED LINKS

[Get-SPOContainerTypeConfiguration](Get-SPOContainerTypeConfiguration.md)
