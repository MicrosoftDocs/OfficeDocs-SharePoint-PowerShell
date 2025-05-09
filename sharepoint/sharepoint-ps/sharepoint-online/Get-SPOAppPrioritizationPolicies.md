external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Get-SPOAppPrioritizationPolicies
applicable: SharePoint Online
title: Get-SPOAppPrioritizationPolicies
schema: 2.0.0
author: killerewok2000
ms.author: Sibourda
ms.reviewer:
---

# Get-SPOAppPrioritizationPolicies

## SYNOPSIS

Gets all existing SPO app prioritization policies of your tenancy. 
> [!NOTE]
> This functionality is rolling out and might not be fully enabled in your environment yet. 
## SYNTAX

```
Get-SPOAppPrioritizationPolicies [<CommonParameters>]
```


## DESCRIPTION

This cmdlet gets all existing SPO App prioritization billing policies for your tenancy.

## EXAMPLES

### Example 1

```powershell
Get- SPOAppPrioritizationPolicies 
```

Example 1 returns a collection of all existing SPO app prioritization policies. Each policy will contain PolicyId, AppId, AzureSubscription, ResourceGroup, Account, Enabled (status of this policy i.e true or false) and QuotaMultiplier 


## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Add-SPOAppPrioritizationPolicy](./Add-SPOAppPrioritizationPolicy.md)

[Set-SPOAppPrioritizationPolicy](./Set-SPOAppPrioritizationPolicy.md)

[Remove-SPOAppPrioritizationPolicy](./Remove-SPOAppPrioritizationPolicy.md)