---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spocontaineruser
applicable: SharePoint Online
title: Remove-SPOContainerUser
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Remove-SPOContainerUser

## SYNOPSIS

Removes a user from a specified role in a SharePoint Embedded container.

## SYNTAX

```
Remove-SPOContainerUser [-ContainerId] <String> -LoginName <String> -Role <String> [<CommonParameters>]
```

## DESCRIPTION

Removes a user from a defined role within a SharePoint Embedded container.

You must be a SharePoint Embedded Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

> [!NOTE]
> You can't remove the principal owner of a container.


## EXAMPLES

### Example 1

```powershell
Remove-SPOContainerUser 423poi45 -LoginName shras@contoso.com -Role Owner
```

Example 1 removes the user with User Principal Name "shras@contoso.com" from the role of an owner of container whose ContainerId is 423poi45 . 

## PARAMETERS

### -ContainerId

> Applicable: SharePoint Online

The unique identifier of the container to which the user is being added.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoginName

> Applicable: SharePoint Online

The user’s login name to assign to the container. This is the User Principal Name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role

> Applicable: SharePoint Online

The role to assign to the user within the container. Valid roles are:

Owner: Has full control over the container and its contents.
Manager: Can add, update, and delete content, and manage permissions, but can't delete the container.
Writer: Can add, update, and delete content in the container.
Reader: Can only view content in the container.


```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Owner, Reader, Writer, Manager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)

[Add-SPOContainerUser](./Add-SPOContainerUser.md)

[Set-SPOContainerUser](./Set-SPOContainerUser.md)

[Set-SPOContainer](./Set-SPOContainer.md)

[Get-SPOContainer](./Get-SPOContainer.md)

