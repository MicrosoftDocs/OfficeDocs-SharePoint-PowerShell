---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Add-SPOAppPrioritizationPolicy
applicable: SharePoint Online
title: Add-SPOAppPrioritizationPolicy
schema: 2.0.0
author: Sibourda
ms.author: Sibourda
ms.reviewer:
---

# Add-SPOAppPrioritizationPolicy

## SYNOPSIS

Adds a new SPO App Prioritization Policy to your tenancy.

## SYNTAX

```powershell
Add-SPOAppPrioritizationPolicies -AppId <Guid string of the app you need SPAP enabled for> -AzureSubscriptionId <Guid string of the Azure Subscription Id> -ResourceGroup <String> -Account <String> -QuotaMultiplier <int> 
```

## DESCRIPTION

This cmdlet adds a new SPO App Prioritization Billing policies to your tenancy. You must be a SharePoint you must be a SharePoint Tenant Admin to run the commandlet. You need to make sure you’re not adding a new billing policy for an app that already has a billing policy to it. 

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


## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Add-SPOAppPrioritizationPolicy](./Add-SPOAppPrioritizationPolicy.md)

[Get-SPOAppPrioritizationPolicies](./Get-SPOAppPrioritizationPolicies.md)

[Set-SPOAppPrioritizationPolicy](./Set-SPOAppPrioritizationPolicy.md)

[Remove-SPOAppPrioritizationPolicy](./Remove-SPOAppPrioritizationPolicy.md)
