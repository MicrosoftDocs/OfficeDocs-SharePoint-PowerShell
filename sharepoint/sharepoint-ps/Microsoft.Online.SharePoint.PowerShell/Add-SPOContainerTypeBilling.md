---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spocontainertypebilling
applicable: SharePoint Online
title: Add-SPOContainerTypeBilling
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Add-SPOContainerTypeBilling

## SYNOPSIS

Adds the mentioned billing profile details to a standard container type.

## SYNTAX

```
Add-SPOContainerTypeBilling -ContainerTypeId <Guid> -AzureSubscriptionId <Guid> -ResourceGroup <String>
 -Region <String> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet attaches the Azure subscription ID, resource group and region with the container type ID provided.

You must be a SharePoint Embedded Administrator to run this cmdlet. You also need to have owner or contributor permissions on an Azure subscription, with active time bound permission on billing, and on the Resource group.

If you don't have an Azure subscription, follow steps here to [create a subscription](/azure/cloud-adoption-framework/ready/azure-best-practices/initial-subscriptions).

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Add-SPOContainerTypeBilling - ContainerTypeId aa1d89b3 -AzureSubscriptionId 5a8a4d9f -ResourceGroup "RG100" -Region "(US) East US"
```

Example 1 attaches the billing profile of Azure subscription ID "5a8a4d9f", resource group "RG100" and region "(US) East US" to the container type ID "aa1d89b3".

## PARAMETERS

### -AzureSubscriptionId

> Applicable: SharePoint Online

This parameter describes the Azure subscription ID to which the container type needs to be associated.

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

### -ContainerTypeId

> Applicable: SharePoint Online

This parameter specifies the ID of the container type corresponding to the SharePoint Embedded application.

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

### -Region

> Applicable: SharePoint Online

This parameter describes the region to which the billing profile of the container type is associated with.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup

> Applicable: SharePoint Online

This parameter describes the resource group to be used for the associated container type.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

[Set-SPOContainerType](./Set-SPOContainerType.md)

[Remove-SPOContainerType](./Remove-SPOContainerType.md)
