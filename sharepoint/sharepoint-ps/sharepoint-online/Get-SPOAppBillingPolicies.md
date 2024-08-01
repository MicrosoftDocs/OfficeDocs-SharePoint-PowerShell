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

Returns  billing policies asscoiated with the application

## SYNTAX

```powershell

Get-SPOAppBillingPolicies
```

## DESCRIPTION

Get-SPOAppBillingPolicies retrieves the billing profile associated with the application. 

This cmdlet will return both active and inactive billing policies for the application.

## EXAMPLES

### Example 1

```powershell

Get-SPOAppBillingPolicies

```

This cmdlet returns billing policies with information such as : 

- Application id : Application Identifier

- Azure subscription Id : Subscription ID associated with the appplication

- Resource Group : Resource group associated with the Azure Subscription 

- Azure Region: Azure Region associated with the Azure Subscription 

- Subscription State: Describes whether billing policy is valid or invalid

- UsageCharges: Who should be billed for Application Usage. Values are : AppOwnerIsCharged or ConsumingTenantOfTheAppIsCharged

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)
