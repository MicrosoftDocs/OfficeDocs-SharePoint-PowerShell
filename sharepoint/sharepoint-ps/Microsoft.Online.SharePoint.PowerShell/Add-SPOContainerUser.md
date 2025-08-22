---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spocontaineruser
applicable: SharePoint Online
title: Add-SPOContainerUser
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Add-SPOContainerUser

## SYNOPSIS

Adds a user to a SharePoint Embedded container with a specified role.

## SYNTAX

```
Add-SPOContainerUser [-ContainerId] <String> -LoginName <String> -Role <String> [<CommonParameters>]
```

##DESCRIPTION

Assigns a user to a defined role within a SharePoint Embedded container.

You must be a SharePoint Embedded Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

> [!NOTE]
> A user can be assigned to only one role within a container at a time.
> **Owner** and **principal owner** are distinct. A container can have multiple owners, but only one principal owner at any time.
> Principal ownership of a container can't be added—it can only be transferred.


## EXAMPLES

### Example 1

```powershell
Add-SPOContainerUser 423poi45 -LoginName shras@contoso.com-Role Owmer
```

Example 1 assigns the role of owner to user with User Principal Name "shras@contoso.com".

## PARAMETERS

-ContainerId

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

-LoginName

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

-Role

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

[Set-SPOContainerUser](./Set-SPOContainerUser.md)

[Remove-SPOContainerUser](./Remove-SPOContainerUser.md)

[Set-SPOContainer](./Set-SPOContainer.md)

[Get-SPOContainer](./Get-SPOContainer.md)




