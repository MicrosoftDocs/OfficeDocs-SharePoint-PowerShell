---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainer
applicable: SharePoint Online
title: Remove-SPOAppBillingPolicy
schema: 2.0.0
author: arakesh
ms.author: arakesh
ms.reviewer:
---

# Remove-SPOAppBillingPolicy

## SYNOPSIS

Removes billing policy asscoiated with the application

## SYNTAX

```powershell

Remove-SPOAppBillingPolicy [[-ApplicationId] <ApplicationId>] 
```

## DESCRIPTION

Remove-SPOAppBillingPolicy removes the billing policy associated with the application. 

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

Remove-SPOAppBillingPolicy -ApplicationId 1653hhd-87100luhw-786265gk-00asa00

```

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)
