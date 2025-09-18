---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/set-spocontainertype
applicable: SharePoint Online
title: Set-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Set-SPOContainerType

## SYNOPSIS

Sets or updates one or more property values of a trial, standard or a direct to customer billed container type.

## SYNTAX

### ContainerTypeName

```
Set-SPOContainerType -ContainerTypeId <Guid> [-ContainerTypeName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### OwningApplicationId

```
Set-SPOContainerType -ContainerTypeId <Guid> [-OwningApplicationId] <Guid> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AzureSubscriptionId

```
Set-SPOContainerType -ContainerTypeId <Guid> [[-AzureSubscriptionId] <Guid>] [-ResourceGroup] <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationRedirectUrl

```
Set-SPOContainerType -ContainerTypeId <Guid> [-ApplicationRedirectUrl] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet updates the existing property of a container type with the new value provided. The cmdlet can be used to change the basic information of a container type such as container type name or the billing information of the container type.

You must be a SharePoint Embedded Administrator to run the cmdlet.

While you only need to be a SharePoint Embedded Administrator to set the basic information of a container type, you need owner or contributor access on the existing billing subscription associated with the container type and also on the new billing subscription, to change the billing information of the container type. List of parameters that cannot be updated includes container type ID and owning application ID.

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Set-SPOContainerType -ContainerTypeId da1d89b3-b4cf-4c0a-8e1c-0d131c57544f -OwningApplicationId 12a9d93c-18d7-46a0-b43e-28d20addd56a - ContainerTypeName 'Red Container Type'
```

Example 1 sets the container type name as 'Red Container Type'

### Example 2

```powershell
Set-SPOContainerType -ContainerTypeId da1d89b3-b4cf-4c0a-8e1c-0d131c57544f –Azure Subscription 12a9d93c-18d7-46a0-b43e-28d20addd56a -ResourceGroup RG200
```

In Example 2, the billing profile of the container type is updated.

### Example 3

```powershell
Set-SPOContainerType -ContainerTypeId 01f62754-0873-4ec6-ab4a-3eed48ba8be7 -OwningApplicationId 994b9586-253e-4a77-b51 - ContainerTypeName 'Blue Container Type'
```

In Example 3, the trial container type name is updated as 'Blue Container Type'

## PARAMETERS

### -ApplicationRedirectUrl

This parameter sets the application redirect Url for the container type.

```yaml
Type: System.String
Parameter Sets: ApplicationRedirectUrl
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureSubscriptionId

Use this parameter to set the Azure billing subscription ID you wish to attach to the container type.

```yaml
Type: System.Guid
Parameter Sets: AzureSubscriptionId
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerTypeId

Use this parameter to enter the container type ID

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerTypeName

Use this parameter to pass the conatiner type name you intend to use for the container type

```yaml
Type: System.String
Parameter Sets: ContainerTypeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup

Use this parameter to set the Azure resource group of the associated Azure billing subscription you intend to attach to the container type.

```yaml
Type: System.String
Parameter Sets: AzureSubscriptionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[New-SPOContainerType](./New-SPOContainerType.md)

[Get-SPOContainerType](./Get-SPOContainerType.md)

[Remove-SPOContainerType](./Remove-SPOContainerType.md)
