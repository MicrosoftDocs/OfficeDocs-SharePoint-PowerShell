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

You must be a SharePoint Administrator to run this cmdlet.

> [!NOTE]
> To use the Get-SPOAppBillingPolicies cmdlet, an admin must authenticate to SharePoint Online using modern authentication.
>
> Use the **Connect-SPOService** cmdlet shown below, which will prompt you to enter your credentials. If multi-factor authentication (MFA) is enabled, you will need to complete the MFA process (e.g., entering a verification code sent to your phone).
> 
> `Connect-SPOService -Url https://(your-tenant)-admin.sharepoint.com`
> 
> Replace (your-tenant) with your actual SharePoint Online domain, e.g. `https://contoso-admin.sharepoint.com. `

## EXAMPLES

### Example 1

```powershell

Get-SPOAppBillingPolicies

```

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)
