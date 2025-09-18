---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/Set-SPOServicePrioritizationAppRegistration
applicable: SharePoint Online
title: Set-SPOServicePrioritizationAppRegistration
schema: 2.0.0
author: killerewok2000
ms.author: Sibourda
ms.reviewer:
---

# Set-SPOServicePrioritizationAppRegistration

## SYNOPSIS
Updates an existing app registration for service prioritization in SharePoint Online.

## SYNTAX

```
Set-SPOServicePrioritizationAppRegistration -AppId <Guid> [-Enabled <Boolean>] [-QuotaMultiplier <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet updates the configuration of an existing app registration for service prioritization in SharePoint Online. This cmdlet is useful for modifying properties such as enabling or disabling the app registration or adjusting the quota multiplier.

## EXAMPLES

### Example 1
```powershell
Set-SPOServicePrioritizationAppRegistration -AppId "12345678-1234-1234-1234-1234567890ab" -Enabled $true -QuotaMultiplier 3
```
This example updates the app registration with the specified AppId, enabling it and setting the quota multiplier to 3.

## PARAMETERS

### -AppId
Specifies the unique identifier (GUID) of the app registration to update.

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

### -Enabled
Specifies whether the app registration is enabled or disabled. Accepts a Boolean value.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Add-SPOServicePrioritizationAppRegistration](./Add-SPOServicePrioritizationAppRegistration.md)

[Get-SPOServicePrioritizationAppRegistrations](./Get-SPOServicePrioritizationAppRegistrations.md)

[Remove-SPOServicePrioritizationAppRegistration](./Remove-SPOServicePrioritizationAppRegistration.md)

[New-SPOServicePrioritizationBillingPolicy](./New-SPOServicePrioritizationBillingPolicy.md)

[Get-SPOServicePrioritizationBillingPolicies](./Get-SPOServicePrioritizationBillingPolicies.md)
