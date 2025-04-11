---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/New-SPOServicePrioritizationBillingPolicy
applicable: SharePoint Online
title: New-SPOServicePrioritizationBillingPolicy
schema: 2.0.0
author: killerewok2000
ms.author: Sibourda
ms.reviewer:
---

# New-SPOServicePrioritizationBillingPolicy

## SYNOPSIS
Creates a new billing policy for service prioritization in SharePoint Online.
> [!NOTE]
> This functionality is rolling out and might not be fully enabled in your environment yet.

## SYNTAX

```
New-SPOServicePrioritizationBillingPolicy -AzureSubscriptionId <Guid> -ResourceGroup <String>
 -AzureRegion <String> -FriendlyName <String> [<CommonParameters>]
```

## DESCRIPTION
The `New-SPOServicePrioritizationBillingPolicy` cmdlet allows administrators to create a new billing policy for service prioritization in SharePoint Online. This cmdlet is useful for defining custom billing rules and policies for specific Azure subscriptions and resource groups.

## EXAMPLES

### Example 1
```powershell
PS C:\> New-SPOServicePrioritizationBillingPolicy -AzureSubscriptionId "12345678-1234-1234-1234-1234567890ab" -ResourceGroup "MyResourceGroup" -AzureRegion "EastUS" -FriendlyName "MyBillingPolicy"
```
This example creates a new billing policy for service prioritization with the specified Azure subscription, resource group, and region.

## PARAMETERS

### -AzureRegion
{{ Fill AzureRegion Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureSubscriptionId
{{ Fill AzureSubscriptionId Description }}

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

### -FriendlyName
{{ Fill FriendlyName Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
{{ Fill ResourceGroup Description }}

```yaml
Type: String
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

[Remove-SPOServicePrioritizationAppRegistration](./Remove-SPOServicePrioritizationAppRegistration.md)

[Get-SPOServicePrioritizationBillingPolicies](./Get-SPOServicePrioritizationBillingPolicies.md)

[Set-SPOServicePrioritizationAppRegistration](./Set-SPOServicePrioritizationAppRegistration.md)