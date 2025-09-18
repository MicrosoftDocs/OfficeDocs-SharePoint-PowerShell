---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/Remove-SPOServicePrioritizationAppRegistration
applicable: SharePoint Online
title: Remove-SPOServicePrioritizationAppRegistration
schema: 2.0.0
author: killerewok2000
ms.author: Sibourda
ms.reviewer:
---

# Remove-SPOServicePrioritizationAppRegistration

## SYNOPSIS
Removes an app registration from service prioritization in SharePoint Online.

## SYNTAX

```
Remove-SPOServicePrioritizationAppRegistration -AppId <Guid> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet removes a specified app registration from the service prioritization configuration in SharePoint Online. This is useful for administrators who need to decommission or update app registrations.

## EXAMPLES

### Example 1
```powershell
Remove-SPOServicePrioritizationAppRegistration -AppId "12345678-1234-1234-1234-1234567890ab"
```
This example removes the app registration with the specified AppId from service prioritization.

## PARAMETERS

### -AppId
The unique identifier (GUID) of the app registration to be removed from service prioritization. This parameter is required and must be specified.

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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

[New-SPOServicePrioritizationBillingPolicy](./New-SPOServicePrioritizationBillingPolicy.md)

[Get-SPOServicePrioritizationBillingPolicies](./Get-SPOServicePrioritizationBillingPolicies.md)

[Set-SPOServicePrioritizationAppRegistration](./Set-SPOServicePrioritizationAppRegistration.md)
