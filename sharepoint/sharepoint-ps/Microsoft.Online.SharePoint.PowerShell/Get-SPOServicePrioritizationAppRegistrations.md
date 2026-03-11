---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/Get-SPOServicePrioritizationAppRegistrations
applicable: SharePoint Online
title: Get-SPOServicePrioritizationAppRegistrations
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer: speedta
---

# Get-SPOServicePrioritizationAppRegistrations

## SYNOPSIS

Returns app registrations enrolled in SharePoint Online Service Prioritization.

## SYNTAX

### All (Default)

```powershell
Get-SPOServicePrioritizationAppRegistrations [<CommonParameters>]
```

### ByPolicy

```powershell
Get-SPOServicePrioritizationAppRegistrations -PolicyId <Guid> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet retrieves all app registrations enrolled in SharePoint Online Service Prioritization for the tenant.

When `-PolicyId` is specified, only registrations linked to that billing policy are returned.

## EXAMPLES

### Example 1: Get all app registrations

```powershell
Get-SPOServicePrioritizationAppRegistrations
```

Returns all app registrations enrolled in SharePoint Online Service Prioritization for the tenant.

### Example 2: Get app registrations for a specific billing policy

```powershell
Get-SPOServicePrioritizationAppRegistrations -PolicyId 11111111-1111-1111-1111-111111111111
```

Returns only app registrations linked to the specified billing policy.

## PARAMETERS

### -PolicyId

The unique identifier of the SPO Service Prioritization billing policy to filter by.
When specified, only app registrations linked to this policy are returned.
When omitted, all app registrations for the tenant are returned.

```yaml
Type: Guid
Parameter Sets: ByPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-SPOServicePrioritizationAppRegistration](Add-SPOServicePrioritizationAppRegistration.md)

[Remove-SPOServicePrioritizationAppRegistration](Remove-SPOServicePrioritizationAppRegistration.md)

[Remove-SPOServicePrioritizationAppRegistrationsByPolicy](Remove-SPOServicePrioritizationAppRegistrationsByPolicy.md)

[Get-SPOServicePrioritizationBillingPolicies](Get-SPOServicePrioritizationBillingPolicies.md)
