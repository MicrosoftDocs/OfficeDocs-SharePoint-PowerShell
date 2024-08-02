---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Get-SPOAppBillingPolicies
applicable: SharePoint Online
title: Get-SPOAppBillingPolicies
schema: 2.0.0
author: arakesh
ms.author: arakesh
ms.reviewer:
---

# Get-SPOAppBillingPolicies

## SYNOPSIS

Returns billing policies that are owned by the tenant.

## SYNTAX

```powershell

Get-SPOAppBillingPolicies
```

## DESCRIPTION

Get-SPOAppBillingPolicies returns a list of billing policies that are owned by the tenant. If the tenant has no billing policies associated, the cmdlet will produce no output. 

The output of this cmdlet will include information related to the billing policy such as Application Id, Azure subscription ID, Resource Group, Region, State of the subscription and the usage charging model.

You must be a SharePoint Administrator or Global Administrator to run this cmdlet.

> [!NOTE]
> To use the Get-SPOAppBillingPolicies cmdlet, an admin must authenticate to SharePoint Online using modern authentication.
>
> Use the **Connect-SPOService** cmdlet shown below, which will prompt you to enter your credentials. If multi-factor authentication (MFA) is enabled, you will need to complete the MFA process (e.g., entering a verification code sent to your phone).
> 
>```powershell
> Connect-SPOService -Url https://(your-tenant)-admin.sharepoint.com
>```
> Replace (your-tenant) with your actual SharePoint Online domain. E.g. https://contoso-admin.sharepoint.com

## EXAMPLES

### Example 1

```powershell

Get-SPOAppBillingPolicies

```

## PARAMETERS

### -ApplicationID

This parameter specifies the ID of the  application.
 
```yaml
Type: GUID
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureRegion

The region of the Azure Subscription.
 
```yaml
Type: String
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -IsActivated

Statement if the billing policy is active
 
```yaml
Type: String
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup

Resource Group Name associated with the Azure Subscription
 
```yaml
Type: String
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -AzureSubscriptionId

The unique identifier of the Azure subscription for billing purposes.
 
```yaml
Type: GUID
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionState

Describes whether billing policy is valid or invalid
 
```yaml
Type: String
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -UsageCharges

This parameters determines who is charged for the usage of the application. This parameter supports two values  - AppOwnerIsCharged or ConsumingTenantoftheAppischarged.
- AppOwnerIsCharged : The tenant owning the application is charged for the usage
- ConsumingTenantoftheAppischarged : The tenant using the application is charged for the usage.
 
```yaml
Type: String
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)
