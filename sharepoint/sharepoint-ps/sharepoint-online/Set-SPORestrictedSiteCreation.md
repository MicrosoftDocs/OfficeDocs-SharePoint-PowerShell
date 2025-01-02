---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-sporestrictedsitecreation
applicable: SharePoint Online
title: Set-SPORestrictedSiteCreation
schema: 2.0.0
author: vgaddam-pm
ms.author: vgaddam
ms.reviewer: jmcdowe
---

# Set-SPORestrictedSiteCreation

## SYNOPSIS

Sets or updates one or more group configurations for restricting site creation.

## SYNTAX

### ParamSet1

```powershell
Set-SPORestrictedSiteCreation
   [-Enabled <Boolean>]
   [-Mode <RestrictedSiteCreationMode>]
   [-SiteType <RestrictedSiteCreationSiteType>]
   [-RestrictedSiteCreationGroups <String>]
```

## DESCRIPTION

This cmdlet sets or updates the configuration or setting for the Restricted Site Creation feature.

> [!Important]
> You must use version 16.0.25513.12000 (published November 2024) or later of the [SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) for these commands to function properly. Earlier versions do not have the current list of site types and will not operate correctly.

## EXAMPLES

### Example 1

```powershell
Set-SPORestrictedSiteCreation –Enabled:$true
```

Example 1 enables the restricted site creation feature for the tenant. 

### Example 2

```powershell
Set-SPORestrictedSiteCreation –Mode Allow
```

Example 2 sets restricted site creation to allow mode. In this mode, a user is only able to create a site if they are a member of a group specified for a matching site type.

### Example 3

```powershell
Set-SPORestrictedSiteCreation –SiteType "All" -RestrictedSiteCreationGroups "281e395b-7316-4cb2-b5bb-8881426ee411"
```

Example 3 updates the policy for the `All` site type to apply to members of the Microsoft Entra security group with ID 281e395b-7316-4cb2-b5bb-8881426ee411. Members of this group are now either allowed or denied (depending on the current mode) from creating all OneDrive and SharePoint sites.

### Example 4

```powershell
Set-SPORestrictedSiteCreation –SiteType "Team" -RestrictedSiteCreationGroups "78159241-04a9-41d2-8dd4-ac568e9766a3,1f95829b-e1c8-4406-b2be-508c36f4bca5"
```

Example 4 updates the policy for the `Team` site type to apply to members of the two specified groups. Members of both specified security groups are now either allowed or denied from creating Team sites, depending on the current mode.
### Example 5

```powershell
Set-SPORestrictedSiteCreation –SiteType "OneDrive" -RestrictedSiteCreationGroups ""
```

Example 5 clears the policy for the `OneDrive` site type so that it no longer applies to any users.

## PARAMETERS

### -Enabled

PARAMVALUE: true | false
Enables or disables Restricted Site Creation feature in tenant.

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

### -Mode

Specifies whether policies allow or deny users from creating sites.
PARAMVALUE: Deny | Allow
- Deny – a user will be blocked from creating a site if any policy applies to them.
- Allow – a user will only be allowed to create a site if a policy applies to them.

> [!NOTE]
> The restricted site creation mode is shared across all site type policies. It is not possible to use deny mode for one site type and allow mode for a different site type. When the mode is changed, all polices are cleared.

```yaml
Type: RestrictedSiteCreationMode
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteType

When paired with the `–RestrictedSiteCreationGroups` parameter, creates a new policy which applies to the specified types of sites.

PARAMVALUE: All | SharePoint | OneDrive | Team | Communication
- All - OneDrive and all SharePoint sites 
- SharePoint - All SharePoint sites (but not OneDrive) 
- OneDrive - Only OneDrive 
- Team - Only SharePoint team sites (group-connected and classic) 
- Communication - Only SharePoint communication sites


```yaml
Type: RestrictedSiteCreationSiteType
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestrictedSiteCreationGroups

A comma-separated list of up to 10 Microsoft Entra security group IDs. When paired with the `–SiteType` parameter, defines a new policy which applies to the specified groups.
Set to the empty string ("") to clear the policy for a site type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: cf
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

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Set-SPORestrictedSiteCreation](Set-SPORestrictedSiteCreation.md)
