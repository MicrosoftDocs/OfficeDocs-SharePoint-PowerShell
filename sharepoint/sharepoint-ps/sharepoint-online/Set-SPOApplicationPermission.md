---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spoapplicationpermission
applicable: SharePoint Online
title: Set-SPOApplicationPermission
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# Set-SPOApplicationPermission

## SYNOPSIS

Adds permissions for a guest application to access a SharePoint Embedded application.

## SYNTAX


### ParamSet1

```powershell
Set-SPOApplicationPermission 
[[-OwningApplicationId] <OwningApplicationid>] 
[[-ApplicationId] <ApplicationId>]
[[-PermissionAppOnly] <AppOnlyPermission>]
[[-PermissionDelegated] <DelegatedPermission>]
``` 

## DESCRIPTION

The `Set-SPOApplicationPermission` cmdlet adds a guest app permission to a SharePoint Embedded application. Currently only app-only permissions are supported at this time. Delegated permissions are not support for guest applications. A guest application is defined as any application within the enterprise applications of the owning tenant. 

You must be a SharePoint Online Administrator or Global Administrator to run this cmdlet. For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps). 

## EXAMPLES

### Example 1

```powershell
Set-SPOApplicationPermission
-OwningApplicationId a187e399-0c36-4b98-8f04-1edc167a0996 
-ApplicationId 12345678-1234-1234-abcd-abcdefghijkl
-PermissionAppOnly Read, Write, Delete
```


Example 1 gives the Guest App with ID `12345678-1234-1234-abcd-abcdefghijkl` app-only Read, Write, and Delete permissions to access the Owning Application Microsoft Loop of ID `a187e399-0c36-4b98-8f04-1edc167a0996`.

### Example 2

```powershell
Set-SPOApplicationPermission
-OwningApplicationId 5e2795e3-ce8c-4cfb-b302-35fe5cd01597 
-ApplicationId 12345678-1234-1234-abcd-abcdefghijkl>
-PermissionAppOnly ReadContent, WriteContent
-PermissionDelegated None
```

Example 2 gives the Guest App with ID `12345678-1234-1234-abcd-abcdefghijkl` app-only Read, Write, and Delete permissions to access the Owning Application Microsoft Designer of ID `a187e399-0c36-4b98-8f04-1edc167a0996`. Notice that delegated permissions are not supported at this time and are default set to `None`.



## PARAMETERS

### -OwningApplicationId

Use this parameter to specify the Owning Application where guest application access is granted.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

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
Applicable: SharePoint Online

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
Applicable: SharePoint Online

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

[Get-SPOApplication](./Get-SPOApplication.md)
[Set-SPOApplication] (Set-SPOApplication.md)
