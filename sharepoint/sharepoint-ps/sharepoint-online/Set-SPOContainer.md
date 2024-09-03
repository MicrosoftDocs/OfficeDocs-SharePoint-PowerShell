---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-SPOContainer
Applicable: SharePoint Embedded
title: Set-SPOContainer
schema: 2.0.0
author: abiramisuresh
ms.author: abisuresh
ms.reviewer:
---

# Set-SPOContainer

## SYNOPSIS

Sets or updates one or more property values for a Container in SharePoint Embedded.

## SYNTAX

### ParamSet1

```powershell
Set-SPOContainer [-Identity] 
 [-BlockDownloadPolicy <Boolean>]
 [-ConditionalAccessPolicy <SPOConditionalAccessPolicyType>]
 [-SensitivityLabel <String>] 
 [-RemoveLabel]
```

## DESCRIPTION

For any parameters that are passed in, the `Set-SPOContainer` cmdlet sets or updates the setting for the Container collection identified by the parameter Identity.

You must be at least a SharePoint administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the online documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).

## EXAMPLES

### Example 1

```powershell
Set-SPOContainer -Identity https://contoso.sharepoint.com/contentstorage/CSP_33a63968-abae-49a3-a255-f83d0ab2260a/ -BlockDownloadPolicy $true
```

Example 1 sets the Block Download policy on the Container mentioned in the Identity parameter. 

### Example 2

```powershell
Set-SPOContainer -Identity https://contoso.sharepoint.com/contentstorage/CSP_33a63968-abae-49a3-a255-f83d0ab2260a/ -ConditionalAccessPolicy AllowLimitedAccess 
```

In this example, limited access is provided to content residing in the Container.

### Example 3

```powershell
Set-SPOContainer -Identity https://contoso.sharepoint.com/contentstorage/CSP_33a63968-abae-49a3-a255-f83d0ab2260a/ -SensitivityLabel ab310e93-9f19-43f2-bc19-bf3386dc0956
```
This example sets a sensitivity label on the Container.

### Example 4
```powershell
Set-SPOContainer -Identity https://contoso.sharepoint.com/contentstorage/CSP_33a63968-abae-49a3-a255-f83d0ab2260a/ -RemoveLabel
```
This example sets any previously set sensitivity label on the Container.

## PARAMETERS

### -BlockDownloadPolicy
As a SharePoint Administrator or above in Microsoft 365, you can block the download of files from SharePoint Embedded Containers. This feature does not need Microsoft Entra Conditional Access policies. This feature can be set for individual Containers but not at the organization level.

Blocking the download of files allows users to remain productive while addressing the risk of accidental data loss. Users have browser-only access with no ability to download, print, or sync files. They also won't be able to access content through apps, including the Microsoft Office desktop apps. When web access is limited, users will see the following message at the top of Containers: "Your organization doesn't allow you to download, print, or sync from this Container. For help contact your IT department." Read the full documentation for advanced capabilities at [Block download policy for SharePoint Containers and OneDrive](/sharepoint/block-download-from-sites).

PARAMVALUE: $true | $false

```yaml
Type: Boolean
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Embedded
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionalAccessPolicy
Read the [Control access from unmanaged devices](/sharepoint/control-access-from-unmanaged-devices) documentation to understand Conditional Access Policy usage in SharePoint Embedded Container.

Possible values:
- AllowFullAccess: Allows full access from desktop apps, mobile apps, and the web.
- AllowLimitedAccess: Allows limited, web-only access.
- BlockAccess: Blocks access.

```yaml
Type: SPOConditionalAccessPolicyType
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Embedded
Required: False
Position: Named
Default value: AllowFullAccess
Accept pipeline input: False
Accept wildcard characters: False
```

### -SensitivityLabel
Specifies the unique identifier (GUID) of the SensitivityLabel.

```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Embedded
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLabel
This parameter allows you to remove the assigned sensitivity label on a Container.

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

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Set-SPOTenant](set-spotenant.md)