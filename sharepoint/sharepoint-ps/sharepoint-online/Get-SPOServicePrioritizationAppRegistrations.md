---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Get-SPOServicePrioritizationAppRegistrations
applicable: SharePoint Online
title: Get-SPOServicePrioritizationAppRegistrations
schema: 2.0.0
author: killerewok2000
ms.author: Sibourda
ms.reviewer:
---

# Get-SPOServicePrioritizationAppRegistrations

## SYNOPSIS
Retrieves the list of app registrations configured for service prioritization in SharePoint Online.
> [!NOTE]
> This functionality is rolling out and might not be fully enabled in your environment yet.

## SYNTAX

```
Get-SPOServicePrioritizationAppRegistrations [<CommonParameters>]
```

## DESCRIPTION
This cmdlet retrieves all app registrations that have been configured for service prioritization in SharePoint Online. This cmdlet is useful for administrators who need to review or audit the current app registrations and their associated policies.

## EXAMPLES

### Example 1
```powershell
Get-SPOServicePrioritizationAppRegistrations
```
This example retrieves all app registrations configured for service prioritization in SharePoint Online.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Add-SPOServicePrioritizationAppRegistration](./Add-SPOServicePrioritizationAppRegistration.md)

[Remove-SPOServicePrioritizationAppRegistration](./Remove-SPOServicePrioritizationAppRegistration.md)

[New-SPOServicePrioritizationBillingPolicy](./New-SPOServicePrioritizationBillingPolicy.md)

[Get-SPOServicePrioritizationBillingPolicies](./Get-SPOServicePrioritizationBillingPolicies.md)

[Set-SPOServicePrioritizationAppRegistration](./Set-SPOServicePrioritizationAppRegistration.md)