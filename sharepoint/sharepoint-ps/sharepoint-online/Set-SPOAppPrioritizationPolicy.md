---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Set-SPOAppPrioritizationPolicy
applicable: SharePoint Online
title: Set-SPOAppPrioritizationPolicy
schema: 2.0.0
author: killerewok2000
ms.author: Sibourda
ms.reviewer:
---

# Set-SPOAppPrioritizationPolicy

## SYNOPSIS

Edits an existing SPO app prioritization policy in your tenancy.
> [!NOTE]
> This functionnality is rolling out and might not be fully enabled on your environment yet. 

## SYNTAX

```
Set-SPOAppPrioritizationPolicy -PolicyId <String> [-Enabled <Boolean>] [-QuotaMultiplier <Int32>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet lets you enable or disable an existing policy and/or change the quota multiplier limit associated with the policy. Note that disabling the policy does not delete the policy. If you need to change only one of the two parameters, retain the value of the non-changing parameter from the `Get-SPOAppPrioritizationPolicies` commandlet. 

## EXAMPLES

### Example 1

```powershell
Set-SPOAppPrioritizationPolicies -PolicyId 48abxxa9 -Enabled $false 
```

Example 1 disables the policy bearing the policyId 48abxxa9

### Example 2

```powershell
Set-SPOAppPrioritizationPolicies -PolicyId 48abxxa9 -Enabled $true -QuotaMultiplier 7 
```

Example 2 enables the policy bearing the policyId 48abxxa9 and also sets the quota multiplier limit to 7. 

### Example 3

```powershell
Set-SPOAppPrioritizationPolicies -PolicyId 48abxxa9 -QuotaMultiplier 8 
```

Example 3 set the quota multiplier limit to 7 of the policy bearing the policyId 48abxxa9. 

## PARAMETERS

### -PolicyId 
 
This parameter specifies the ID of policy.
```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enabled

This parameter described the state wanted of the policy.

```yaml
Type: Bool
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### -QuotaMultiplier
 
This parameter specifies the quota multiplier limit for the scaling feature. Value must be between 1 and 10.

```yaml
Type: int
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Add-SPOAppPrioritizationPolicy](./Add-SPOAppPrioritizationPolicy.md)

[Get-SPOAppPrioritizationPolicies](./Get-SPOAppPrioritizationPolicies.md)

[Remove-SPOAppPrioritizationPolicy](./Remove-SPOAppPrioritizationPolicy.md)
