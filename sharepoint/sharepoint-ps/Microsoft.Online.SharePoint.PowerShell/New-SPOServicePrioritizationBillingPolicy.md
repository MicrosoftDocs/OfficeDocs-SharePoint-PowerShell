---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/New-SPOServicePrioritizationBillingPolicy
applicable: SharePoint Online
title: New-SPOServicePrioritizationBillingPolicy
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer: speedta
---

# New-SPOServicePrioritizationBillingPolicy

## SYNOPSIS
Creates a new billing policy for service prioritization in SharePoint Online.


## SYNTAX

```
New-SPOServicePrioritizationBillingPolicy -AzureSubscriptionId <Guid> -ResourceGroup <String>
 -AzureRegion <String> -FriendlyName <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet allows administrators to create a new billing policy for service prioritization in SharePoint Online. This cmdlet is useful for defining custom billing rules and policies for specific Azure subscriptions and resource groups.

## EXAMPLES

### Example 1
```powershell
New-SPOServicePrioritizationBillingPolicy -AzureSubscriptionId "12345678-1234-1234-1234-1234567890ab" -ResourceGroup "MyResourceGroup" -AzureRegion "EastUS" -FriendlyName "MyBillingPolicy"
```
This example creates a new billing policy for service prioritization with the specified Azure subscription, resource group, and region.

## PARAMETERS

### -AzureRegion
Specifies the Azure region where the billing policy applies.

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

### -AzureSubscriptionId
Specifies the unique identifier (GUID) of the Azure subscription associated with the billing policy.

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

### -FriendlyName
Specifies a user-friendly name for the billing policy.

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
Specifies the Azure resource group associated with the billing policy.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Add-SPOServicePrioritizationAppRegistration](./Add-SPOServicePrioritizationAppRegistration.md)

[Get-SPOServicePrioritizationAppRegistrations](./Get-SPOServicePrioritizationAppRegistrations.md)

[Remove-SPOServicePrioritizationAppRegistration](./Remove-SPOServicePrioritizationAppRegistration.md)

[Get-SPOServicePrioritizationBillingPolicies](./Get-SPOServicePrioritizationBillingPolicies.md)

[Set-SPOServicePrioritizationAppRegistration](./Set-SPOServicePrioritizationAppRegistration.md)
