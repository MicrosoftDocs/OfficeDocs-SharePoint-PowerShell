---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainer
applicable: SharePoint Online
title: New-SPOAppBillingPolicy
schema: 2.0.0
author: arakesh
ms.author: arakesh
ms.reviewer:
---

# New-SPOAppBillingPolicy

## SYNOPSIS

Creates a new billing policy for an application

## SYNTAX

```powershell

New-SPOAppBillingPolicy
[[-ApplicationId] <ApplicationId>]
[[-AzureSubscriptionId] <AzureSubscriptionID>]
[[-ResourceGroup] <ResourceGroup>]
[[-AzureRegion] <AzureRegion>]
[[-UsageCharges] <UsageCharges>]
```

## DESCRIPTION

This cmdlet creates a new billing policy for an application that wants to use services using the pay-as-you-go billign model. 

## EXAMPLES

### Example 1

```powershell

Get-SPOAppBillingPolicies -ApplicationId 50785fde-3082-47ac-a36d-06282ac5c7da  -AzureSubscriptionId c7170373-eb8d-4984-8cc9-59bcc88c65a0 -ResouceGroup "SPOPAYG" -AzureRegion "Uk-South" -UsageCharges AppOwnerIsCharged

```
### Example 2

```powershell

Get-SPOAppBillingPolicies -ApplicationId 50785fde-3082-47ac-a36d-06282ac5c7da  -AzureSubscriptionId c7170373-eb8d-4984-8cc9-59bcc88c65a0 -ResouceGroup "SPOPAYG" -AzureRegion "Uk-South" -UsageCharges ConsumingTenantOfTheAppisCharged

```
## PARAMETERS

### -ApplicationID

This parameter specifies the ID of the  application.
 
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

The unique identifier of the Azure Active Directory profile (Microsoft Entra ID) for billing purposes.
 
```yaml
Type: String
Parameter Sets: Standard
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup

The resource group of the Application
 
```yaml
Type: String
Parameter Sets: Standard
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureRegion

The region of the application.
 
```yaml
Type: String
Parameter Sets: Standard
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsageCharges

Which entity is charged for the usage - AppOwnerIsCharged or ConsumingTenantoftheAppischarged
 
```yaml
Type: String
Parameter Sets: All
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Syntex pay-as-you-go services](https://learn.microsoft.com/en-us/microsoft-365/syntex/syntex-pay-as-you-go-services)
