---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spoapplication
applicable: SharePoint Online
title: Get-SPOApplication
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# Get-SPOApplication

## SYNOPSIS

Returns a list of SharePoint Embedded applications in the specified tenant.

## SYNTAX

### ParamSet1

```powershell
Get-SPOApplication [[-OwningApplicationId] <OwningApplicationid>] [<CommonParameters>]
```

### ParamSet2

```powershell
Get-SPOApplication [[-OwningApplicationId] <OwningApplicationid>] [[-ApplicationId] <ApplicationId>]
``` 

## DESCRIPTION

The `Get-SPOApplication` cmdlet retrieves and returns SharePoint Embedded applications of all publishers registered in a tenant that match the given criteria. You must be a SharePoint Online Administrator or Global Administrator to run the cmdlet. For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps). 

## EXAMPLES

### Example 1

```powershell
Get-SPOApplication
```

Example 1 returns all SharePoint Embedded applications registered in the specified tenant by their `OwningApplicationId` and `OwningApplicationName`.

### Example 2

```powershell
Get-SPOApplication -OwningApplicationId <OwningApplicationId>
```

Example 2 lists the details of the owning application corresponding to the `OwningApplicationId` registered in the specified tenant. This returns `Applications` which specifies the list of guest applications IDs with current access permissions to the owning application, `SharingCapability` settings, and `OverrideTenantSharingCapability` status.


### Example 3

```powershell
Get-SPOApplication -OwningApplicationId <OwningApplicationId> -ApplicationId <ApplicationId>
```

Example 3 list details of the guest application specified in `ApplicationId`. This inclues the list of guest application access permissions. Note that only app-only permissions are supported.

## PARAMETERS

### -OwningApplicationId

Use this parameter to get details about apps registered in the specified tenant.

The following details are returned:

- OwningApplicationId

- OwningApplicationName

- Applications (by id)

- SharingCapability

- OverrideTenantSharingCapability
  
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

### -ApplicationId

Use this parameter to enumerate app-only permissions of the guest application id with access to the specified owning application.

```yaml
Type: String
Parameter Sets: ParamSet2
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


## RELATED LINKS

[Get-SPOContainer](./Get-SPOContainer.md)
[Set-SPOApplication](./Set-SPOApplication.md)
