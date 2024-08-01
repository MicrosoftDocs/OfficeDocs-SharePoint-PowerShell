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

Creates a new billing policy for an application owned by the tenant.

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

This cmdlet creates a new billing policy for an application that is owned by the tenant running the cmdlet. 

You must be a SharePoint Online Administrator or Global Administrator to run this cmdlet.

> [!NOTE]
> To sign into SharePoint Online PowerShell Module use the below cmdlet for authentication
> 
```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com
```
>This cmdlet will prompt for credentials. This is required if the account is using multi-factor authentication.

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
Type: GUID
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
Type: GUID
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

Resource Group Name associated with the Azure Subscription
 
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

The region of the Azure Subscription.
 
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

This parameters determined who is charged for the usage of the application. This parameter supports two values  - AppOwnerIsCharged or ConsumingTenantoftheAppischarged.
- AppOwnerIsCharged : The tenant owning the application is charged for the usage
- ConsumingTenantoftheAppischarged : The tenant using the application is charged for the usage.
 
```yaml
Type: Switch
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
