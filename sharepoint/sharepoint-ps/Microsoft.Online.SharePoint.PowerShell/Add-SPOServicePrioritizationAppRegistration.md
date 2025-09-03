---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Add-SPOServicePrioritizationAppRegistration
applicable: SharePoint Online
title: Add-SPOServicePrioritizationAppRegistration
schema: 2.0.0
author: killerewok2000
ms.author: Sibourda
ms.reviewer:
ms.date: 07/15/2025
---

# Add-SPOServicePrioritizationAppRegistration

## SYNOPSIS
Adds a new app registration for service prioritization in SharePoint Online.
> [!NOTE]
> This functionality is rolling out and might not be fully enabled in your environment yet.

## SYNTAX

```
Add-SPOServicePrioritizationAppRegistration -AppId <Guid> -PolicyId <Guid> -QuotaMultiplier <Int32>
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet allows administrators to register a new app for service prioritization in SharePoint Online. This cmdlet is useful for configuring specific apps to receive prioritized service handling based on defined policies.

## EXAMPLES

### Example 1
```powershell
Add-SPOServicePrioritizationAppRegistration -AppId "12345678-1234-1234-1234-1234567890ab" -PolicyId "87654321-4321-4321-4321-0987654321ba" -QuotaMultiplier 2
```
This example adds a new app registration with the specified AppId and PolicyId, and sets the quota multiplier to 2.

## PARAMETERS

### -AppId
Specifies the unique identifier (GUID) of the app registration to be added.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyId
Specifies the unique identifier (GUID) of the policy to associate with the app registration.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QuotaMultiplier
This parameter specifies the quota multiplier limit for the scaling feature. Value must be between 2 and 10.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOServicePrioritizationAppRegistrations](./Get-SPOServicePrioritizationAppRegistrations.md)

[Remove-SPOServicePrioritizationAppRegistration](./Remove-SPOServicePrioritizationAppRegistration.md)

[New-SPOServicePrioritizationBillingPolicy](./New-SPOServicePrioritizationBillingPolicy.md)

[Get-SPOServicePrioritizationBillingPolicies](./Get-SPOServicePrioritizationBillingPolicies.md)

[Set-SPOServicePrioritizationAppRegistration](./Set-SPOServicePrioritizationAppRegistration.md)
