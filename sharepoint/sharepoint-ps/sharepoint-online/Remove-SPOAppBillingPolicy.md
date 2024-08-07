---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Remove-SPOAppBillingPolicy
applicable: SharePoint Online
title: Remove-SPOAppBillingPolicy
schema: 2.0.0
author: arakesh
ms.author: arakesh
ms.reviewer:
---
# Remove-SPOAppBillingPolicy

## SYNOPSIS

Removes billing policy asscoiated with the application.

## SYNTAX

```powershell

Remove-SPOAppBillingPolicy [[-ApplicationId] <ApplicationId>] 
```

## DESCRIPTION

Remove-SPOAppBillingPolicy removes the billing policy associated with the application. 

You must be a SharePoint Administrator to run this cmdlet.

> [!NOTE]
> To use the Remove-SPOAppBillingPolicy cmdlet, an admin must authenticate to SharePoint Online using modern authentication.
>
> Use the **Connect-SPOService** cmdlet shown below, which will prompt you to enter your credentials. If multi-factor authentication (MFA) is enabled, you will need to complete the MFA process (e.g., entering a verification code sent to your phone).
> 
>
> `Connect-SPOService -Url https://(your-tenant)-admin.sharepoint.com`
>
> Replace (your-tenant) with your actual SharePoint Online domain, e.g. `https://contoso-admin.sharepoint.com.`

## EXAMPLES

### Example 1

```powershell

Remove-SPOAppBillingPolicy -ApplicationId 1653hhd-87100luhw-786265gk-00asa00

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

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)
