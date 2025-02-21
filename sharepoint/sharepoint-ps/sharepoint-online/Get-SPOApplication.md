---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spoapplication
applicable: SharePoint
title: Get-SPOApplication
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Get-SPOApplication

## SYNOPSIS

Returns a list of SharePoint Embedded applications in the specified tenant.

## SYNTAX

```
Get-SPOApplication [[-OwningApplicationId] <Guid>] [[-ApplicationId] <Guid>] [<CommonParameters>]
```

### ParamSet1

```powershell
Get-SPOApplication [<CommonParameters>]
```
### ParamSet2

```powershell
Get-SPOApplication [[-OwningApplicationId] <Guid>] [<CommonParameters>]
```

### ParamSet3

```powershell
Get-SPOApplication [[-OwningApplicationId] <Guid>] [[-ApplicationId] <Guid>][<CommonParameters>]
``` 

## DESCRIPTION

This cmdlet is used to retrieve and return SharePoint Embedded applications from all publishers registered within a tenant. This cmdlet can be further customized by pairing it with the `OwningApplicationId` parameter to target a specific application.

In addition to providing details about the application name, this cmdlet also returns essential information about guest applications and their associated permissions on the owning application. The cmdlet displays data related to the sharing capabilities, including the `OverrideTenantSharingCapability` status. Furthermore, the cmdlet lists all host URLs allowed to use the SharePoint Embedded application's declarative agent experience.

You must be a SharePoint Embedded Administrator to run the cmdlet. 


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

Example 2 provides details about the application corresponding to the "Owning Application Id" in the specified tenant. It returns Applications, which includes the list of guest application IDs with permissions to the owning application, as well as the SharingCapability settings, the `OverrideTenantSharingCapability` status and the list of all Copilot embedded chat host URLs. 

### Example 3

```powershell
Get-SPOApplication -OwningApplicationId <OwningApplicationId> -ApplicationId <ApplicationId>
```

Example 3 enumerates app-only permissions of the guest application specified in `ApplicationId`.

### Example 4

```powershell
Get-SPOApplication -OwningApplicationId <OwningApplicationId> | Select-Object CopilotEmbeddedChatHosts
```

Example 4 enumerates the entire list of the host URLs driving the Copilot embedded chat capability on the SharePoint Embedded application.

## PARAMETERS

### -OwningApplicationId

Use this parameter to get details about applications registered in the specified tenant.

The following details are returned:

- OwningApplicationId

- OwningApplicationName

- Applications (by id)

- SharingCapability

- OverrideTenantSharingCapability

- CopilotEmbeddedChatHosts
  
```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId

Use this parameter to enumerate app-only permissions of the guest application id with access to the specified owning application.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).


## RELATED LINKS

[Get-SPOContainer](./Get-SPOContainer.md)

[Set-SPOApplication](./Set-SPOApplication.md)
