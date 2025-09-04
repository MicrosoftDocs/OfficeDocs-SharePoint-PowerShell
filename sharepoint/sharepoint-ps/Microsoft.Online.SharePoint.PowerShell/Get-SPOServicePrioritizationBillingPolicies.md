---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Get-SPOServicePrioritizationBillingPolicies
applicable: SharePoint Online
title: Get-SPOServicePrioritizationBillingPolicies
schema: 2.0.0
author: killerewok2000
ms.author: Sibourda
ms.reviewer:
---

# Get-SPOServicePrioritizationBillingPolicies

## SYNOPSIS
Retrieves the list of billing policies configured for service prioritization in SharePoint Online.
> [!NOTE]
> This functionality is rolling out and might not be fully enabled in your environment yet.

## SYNTAX

```
Get-SPOServicePrioritizationBillingPolicies [<CommonParameters>]
```

## DESCRIPTION
This cmdlet retrieves all billing policies that have been configured for service prioritization in SharePoint Online. This cmdlet is useful for administrators who need to review or audit the current billing policies and their associated configurations.

## EXAMPLES

### Example 1
```powershell
Get-SPOServicePrioritizationBillingPolicies
```
This example retrieves all billing policies configured for service prioritization in SharePoint Online.

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

[Get-SPOServicePrioritizationAppRegistrations](./Get-SPOServicePrioritizationAppRegistrations.md)

[Remove-SPOServicePrioritizationAppRegistration](./Remove-SPOServicePrioritizationAppRegistration.md)

[New-SPOServicePrioritizationBillingPolicy](./New-SPOServicePrioritizationBillingPolicy.md)

[Set-SPOServicePrioritizationAppRegistration](./Set-SPOServicePrioritizationAppRegistration.md)
