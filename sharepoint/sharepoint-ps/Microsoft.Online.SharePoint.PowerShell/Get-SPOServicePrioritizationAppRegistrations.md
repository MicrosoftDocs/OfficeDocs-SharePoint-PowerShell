---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/Get-SPOServicePrioritizationAppRegistrations
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

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