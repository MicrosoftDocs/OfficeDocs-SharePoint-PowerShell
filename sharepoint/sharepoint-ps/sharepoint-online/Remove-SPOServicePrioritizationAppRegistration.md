---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Remove-SPOServicePrioritizationAppRegistration
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
> [!NOTE]
> This functionality is rolling out and might not be fully enabled in your environment yet.

## SYNTAX

```
Remove-SPOServicePrioritizationAppRegistration -AppId <Guid> [<CommonParameters>]
```

## DESCRIPTION
The `Remove-SPOServicePrioritizationAppRegistration` cmdlet removes a specified app registration from the service prioritization configuration in SharePoint Online. This is useful for administrators who need to decommission or update app registrations.

## EXAMPLES

### Example 1
```powershell
PS C:\> Remove-SPOServicePrioritizationAppRegistration -AppId "12345678-1234-1234-1234-1234567890ab"
```
This example removes the app registration with the specified AppId from service prioritization.

## PARAMETERS

### -AppId
The unique identifier (GUID) of the app registration to be removed from service prioritization. This parameter is required and must be specified.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

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