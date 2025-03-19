---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Get-SPOAppPrioritizationPolicies
applicable: SharePoint Online
title: Get-SPOAppPrioritizationPolicies
schema: 2.0.0
author: Sibourda
ms.author: Sibourda
ms.reviewer:
---

# Get-SPOAppPrioritizationPolicies

## SYNOPSIS

Gets all existing SPO App Prioritization Policies of your tenancy 

## SYNTAX

```powershell
Get-SPOAppPrioritizationPolicies
```


## DESCRIPTION

This cmdlet adds a new SPO App Prioritization Billing policies to your tenancy. You must be a SharePoint you must be a SharePoint Tenant Admin to run the commandlet. You need to make sure you’re not adding a new billing policy for an app that already has a billing policy to it. 

## EXAMPLES

### Example 1

```powershell
Get- SPOAppPrioritizationPolicies 
```

Example 1 returns a collection of all existing SPO App Prioritization Policies. Each Policy will contain PolicyId, AppId, AzureSubscription, ResourceGroup, Account, Enabled (status of this policy i.e true or false) and QuotaMultiplier 


## PARAMETERS



## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Add-SPOAppPrioritizationPolicy](./Add-SPOAppPrioritizationPolicy.md)

[Get-SPOAppPrioritizationPolicies](./Get-SPOAppPrioritizationPolicies.md)

[Set-SPOAppPrioritizationPolicy](./Set-SPOAppPrioritizationPolicy.md)

[Remove-SPOAppPrioritizationPolicy](./Remove-SPOAppPrioritizationPolicy.md)
