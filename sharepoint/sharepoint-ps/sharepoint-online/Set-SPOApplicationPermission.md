---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spoapplicationpermission
applicable: SharePoint
title: Set-SPOApplicationPermission
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# Set-SPOApplicationPermission

## SYNOPSIS

Manages permissions for a guest application to access a SharePoint Embedded application.

## SYNTAX


### ParamSet1

```powershell
Set-SPOApplicationPermission 
[[-OwningApplicationId] <OwningApplicationid>] [[-ApplicationId] <ApplicationId>] [[-PermissionAppOnly] <AppOnlyPermission>] [[-PermissionDelegated] <DelegatedPermission>]
``` 

## DESCRIPTION

The `Set-SPOApplicationPermission` cmdlet manages permissions for a guest application's access to a SharePoint Embedded application. This includes adding, updating, and deleting guest application permissions. A guest application is defined as any application within the enterprise applications of the owning tenant. 

You must be a SharePoint Administrator to run this cmdlet. For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps). 

> [!NOTE]
> Only app-only permissions are supported for guest applications accessing SharePoint Embedded applications. Delegated permissions are not supported and are default set to `None`.

## EXAMPLES

### Example 1

```powershell
Set-SPOApplicationPermission -OwningApplicationId a187e399-0c36-4b98-8f04-1edc167a0996 -ApplicationId 12345678-1234-1234-abcd-abcdefghijkl -PermissionAppOnly Read, Write
```


Example 1 gives the guest application with ID `12345678-1234-1234-abcd-abcdefghijkl` app-only Read, Write permissions to access the owning application Microsoft Loop of ID `a187e399-0c36-4b98-8f04-1edc167a0996`.

### Example 2

```powershell
Set-SPOApplicationPermission -OwningApplicationId 5e2795e3-ce8c-4cfb-b302-35fe5cd01597 -ApplicationId 12345678-1234-1234-abcd-abcdefghijkl -PermissionAppOnly ReadContent, WriteContent -PermissionDelegated None
```

Example 2 gives the guest application with ID `12345678-1234-1234-abcd-abcdefghijkl` app-only ReadContent, WriteContent permissions to access the owning application Microsoft Designer of ID `a187e399-0c36-4b98-8f04-1edc167a0996`.
### Example 3

```powershell
Set-SPOApplicationPermission -OwningApplicationId 5e2795e3-ce8c-4cfb-b302-35fe5cd01597 -ApplicationId 12345678-1234-1234-abcd-abcdefghijkl -PermissionAppOnly None -PermissionDelegated None
```

Example 3 sets guest application permissions to None for the guest application with ID `12345678-1234-1234-abcd-abcdefghijkl`. This has deleted previous permissions for that guest application to access owning application of `a187e399-0c36-4b98-8f04-1edc167a0996`. 

## PARAMETERS

### -OwningApplicationId

Use this parameter to specify the Owning Application where guest application access is granted.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId

Use this parameter to specify the guest application ID. A guest application is any application within the tenant's enterprise applications.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionAppOnly

Use this parameter to specify the app-only permissions of the guest application.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
``` 

### -PermissionDelegated

This parameter specifies delegated permissions which are not supported for guest applications at this time.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
``` 


### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).


## RELATED LINKS

[Get-SPOApplication](./Get-SPOApplication.md)
[Set-SPOApplication](./Set-SPOApplication.md)
