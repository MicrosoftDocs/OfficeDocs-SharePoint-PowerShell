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

Get-SPOAppBillingPolicies [[-ApplicationId] <ApplicationId>] 
```

## DESCRIPTION

Get-SPOAppBillingPolicies retrieves the billing profile associated with the application. 

This cmdlet will return both active and inactive billing policies for the application.

## EXAMPLES

### Example 1

```powershell

Get-SPOAppBillingPolicies -ApplicationId 1653hhd-87100luhw-786265gk-00asa00

```

This cmdlet returns billing policies including 

- Application id : Application Identifier

- Azure subscription Id : Subscription ID associated with the appplication

- Resource Group : Resource group associated with the appplication

- Azure Region: Region 

- Subscription State: State of the subscription - Valid or Invalid

- UsageCharges: Who is charged for the usage - Application owner or consuming tenant

- Type ID :

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)
