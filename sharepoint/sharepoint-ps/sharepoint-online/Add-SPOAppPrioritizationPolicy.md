---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Add-SPOAppPrioritizationPolicy
applicable: SharePoint Online
title: Add-SPOAppPrioritizationPolicy
schema: 2.0.0
author: killerewok2000
ms.author: Sibourda
ms.reviewer:
---

# Add-SPOAppPrioritizationPolicy

## SYNOPSIS

Adds a new SPO app prioritization Policy to your tenancy.

## SYNTAX

```
Add-SPOAppPrioritizationPolicy -AppId <String> -AzureSubscriptionId <String> -ResourceGroup <String> -Account <String> -QuotaMultiplier <Int32> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet adds a new SPO app prioritization billing policies to your tenancy. Ensure that you do not add a new billing policy to an app that already has one.

## EXAMPLES

### Example 1

```powershell
Add-SPOAppPrioritizationPolicies -AppId 48ab2ba9-5713-47d6-88a1-f6e3a0730833 -AzureSubscriptionId 48ab1ba4-9813-47d6-88a1-f6e3a0730822 -ResourceGroup newResourceGroup -Account newAccountName -QuotaMultiplier 5 
```

Example 1 adds the billing policy to your tenancy. It will not add the policy on invalid inputs or for apps that already have an associated policy. 


## PARAMETERS

### -AppId
 
This parameter specifies the app ID of the application to onboard.
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

### -AzureSubscriptionId

This parameter describes the Azure subscription ID to which the container type needs to be associated.

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


### -ResourceGroup

This parameter describes the resource group to be used for the associated container type.

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

### -Account

This parameter describes the account to which the billing profile of the container type is associated with.

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
### -QuotaMultiplier
 
This parameter specifies the multiplier for the scaling feature.

```yaml
Type: int
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).


## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppPrioritizationPolicies](./Get-SPOAppPrioritizationPolicies.md)

[Set-SPOAppPrioritizationPolicy](./Set-SPOAppPrioritizationPolicy.md)

[Remove-SPOAppPrioritizationPolicy](./Remove-SPOAppPrioritizationPolicy.md)
