---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spositedataencryptionpolicy
applicable: SharePoint Online
title: Get-SPOSiteDataEncryptionPolicy
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Get-SPOSiteDataEncryptionPolicy

## SYNOPSIS

Validates the encryption of a Group Site, Team Site, or OneDrive for Business site if a Customer Key has been registered for the site.

## SYNTAX

```
Get-SPOSiteDataEncryptionPolicy [-Identity] <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

When a Customer Key has been configured in the Azure tenant, it is possible to set and subsequently verify the encryption status of a SharePoint Online or OneDrive for Business site. This cmdlet verifies the encryption status of the particular site.

This cmdlet will return an error if the Azure tenant has not been configured with a Customer Key. See the Related Links section for more information on how to configure the Customer Key.

## EXAMPLES

### Example 1

```powershell
Get-SPOSiteDataEncryptionPolicy https://contoso.sharepoint.com/sites/Research
```

Verifies the encryption of the site https://contoso.sharepoint.com/sites/Research.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

The URL of the Site Collection.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS
### System.String

The URI of the primary key.

### System.String

The URI of the secondary key.

### System.Object

The encryption status for the geo. Possible states include:

* Unregistered: Customer Key encryption has not yet been applied.
* Registering: Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.
* Registered: Customer Key encryption has been applied, and all files in all sites have been encrypted.
* Rolling: A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.

## NOTES

## RELATED LINKS

[Register-SPODataEncryptionPolicy](/powershell/module/microsoft.online.sharepoint.powershell/register-spodataencryptionpolicy)

[Controlling your data in Office 365 using Customer Key](/microsoft-365/compliance/controlling-your-data-using-customer-key)

[Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business](/microsoft-365/compliance/controlling-your-data-using-customer-key#office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business)
