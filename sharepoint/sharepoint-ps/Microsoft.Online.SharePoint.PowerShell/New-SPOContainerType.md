---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/new-spocontainertype
applicable: SharePoint Online
title: New-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# New-SPOContainerType

## SYNOPSIS

This cmdlet creates a new container type of standard or trial status. The standard container type can be created with the regular billing structure or direct to customer billing structure.

## SYNTAX

```
New-SPOContainerType [-ContainerTypeName] <String> -OwningApplicationId <Guid>
 [-ApplicationRedirectUrl <String>] [-TrialContainerType] [-IsPassThroughBilling]
 [-IsGovernableByAdmin <Boolean>] [-IsArchiveEnabled <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new standard or trial container type. A standard container type, by definition, has a billing profile associated with it and can be either regular billed or direct to consumer billed. A trial container type does not have a billing profile. In case of regular billing, the next step after creation is the addition of a billing profile using the [Add-SPOContainerTypeBilling](./Add-SPOContainerTypeBilling.md) cmdlet. With the use of `-IsPassThroughBilling`, you can create a direct to customer billed container type. There is no need to attach a billing profile in case this case. `–TrialContainerType` when used creates a trial container type that has a validity of 30 days.

You must be a SharePoint Embedded Administrator to run this cmdlet.

## EXAMPLES

### Example 1

```powershell
New-SPOContainerType -ContainerTypeName ContosoLegal -OwningApplicationId 2ce03211-353e-45d7-b487-8ac6981332cf
```

In Example 1, the cmdlet creates a new regular billed container type ContosoLegal.

### Example 2

```powershell
New-SPOContainerType –IsPassThroughBilling –ContainerTypeName ContosoLegal -OwningApplicationId 2ce03211-353e-45d7-b487-8ac6981332ed
```

In Example 2, the cmdlet creates a direct to customer billed container type ContosoLegal.

### Example 3

```powershell
New-SPOContainerType –TrialContainerType -ContainerTypeName ContosoLegal -OwningApplicationId 2ce03211-353e-45d7-b487-8ac6981332fl
```

In Example 3, the cmdlet creates a trial container type, ContosoLegal, valid for 30 days.

### Example 4

```powershell
New-SPOContainerType -ContainerTypeName ContosoLegal -OwningApplicationId 2ce03211-353e-45d7-b487-8ac6981332cf -GovernableByAdmin $false
```

In Example 4, the cmdlet creates a standard container type, ContosoLegal that has opted out of management through Microsoft-enabled administrator platforms.

### Example 5

```powershell
New-SPOContainerType -ContainerTypeName ContosoLegal -OwningApplicationId 2ce03211-353e-45d7-b487-8ac6981332cf -IsArchiveEnabled $true
```

In Example 5, the cmdlet creates a standard container type, ContosoLegal that supports archive and reactivate actions on its containers.

## PARAMETERS

### -ApplicationRedirectUrl

> Applicable: SharePoint Online

This parameter specifies the url of that the application should be redirected to.

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

### -ContainerTypeName

> Applicable: SharePoint Online

This parameter names your container type for your SharePoint Embedded application.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsArchiveEnabled

> Applicable: SharePoint Online

Use the `-IsArchiveEnabled` flag to enable archival of containers. Archival moves data to the cold tier, reducing storage costs. While archived, content is inaccessible until reactivated. Reactivation is immediate within the first seven days and can take up to 24 hours afterward. If you don’t include this flag, the value defaults to `False`, and all archive API calls fail. After you update the flag, allow up to 24 hours for the change to take effect in the consuming tenant.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsGovernableByAdmin

> Applicable: SharePoint Online

Using `-GovernableByAdmin`, you can decide whether consuming tenant administrators of the application should be provided management capabilities on Microsoft-enabled administrator support, through SharePoint admin center and PowerShell. When not passed, the value is set to True. When set to False, the consuming tenant administrator can perform only read-only actions on containers of the container type, in both SharePoint admin center and PowerShell.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsPassThroughBilling

> Applicable: SharePoint Online

This parameter is used to create a direct to customer billed container type.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OwningApplicationId

> Applicable: SharePoint Online

This parameter specifies the ID of the SharePoint Embedded application.

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

### -TrialContainerType

> Applicable: SharePoint Online

This parameter is used to specify that the cmdlet is used to create a trial container type and thereby the billing profile need not be provided.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Add-SPOContainerTypeBilling](./Add-SPOContainerTypeBilling.md)

[Get-SPOContainerType](./Get-SPOContainerType.md)

[Set-SPOContainerType](./Set-SPOContainerType.md)

[Remove-SPOContainerType](./Remove-SPOContainerType.md)
