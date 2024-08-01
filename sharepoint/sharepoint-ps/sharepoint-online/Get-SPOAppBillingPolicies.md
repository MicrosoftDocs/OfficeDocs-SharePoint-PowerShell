---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainer
applicable: SharePoint Online
title: Get-SPOAppBillingPolicies
schema: 2.0.0
author: arakesh
ms.author: arakesh
ms.reviewer:
---

# Get-SPOAppBillingPolicies

## SYNOPSIS

Returns billing policies athat are owned by the tenant.

## SYNTAX

```powershell

Get-SPOAppBillingPolicies
```

## DESCRIPTION

Get-SPOAppBillingPolicies returns billing policies athat are owned by the tenant. If the tenant has no billing policies associated, the cmdlet will produce no output. 

The output will include information about the billing policies available in the tenant such as Application Id, Azure subscription ID, Resource Group, Region, State of the subscription and which tenant is charged.

You must be a SharePoint Online Administrator or Global Administrator to run this cmdlet.

> [!NOTE]
> To sign into SharePoint Online PowerShell Module use the below cmdlet for authentication
> 
```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com
```
This cmdlet will prompt for credentials. This is required if the account is using multi-factor authentication.

## EXAMPLES

### Example 1

```powershell

Get-SPOAppBillingPolicies

```

This cmdlet returns billing policies with information such as : 

- Application id : Application Identifier

- UsageCharges: Who should be billed for Application Usage. Values are : AppOwnerIsCharged or ConsumingTenantOfTheAppIsCharged

- Azure subscription Id : Subscription ID associated with the appplication

- Resource Group : Resource group associated with the Azure Subscription 

- Azure Region: Azure Region associated with the Azure Subscription 

- Subscription State: Describes whether billing policy is valid or invalid

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)
