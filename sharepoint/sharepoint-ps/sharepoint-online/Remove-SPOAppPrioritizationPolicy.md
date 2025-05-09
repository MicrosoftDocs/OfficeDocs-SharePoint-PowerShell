---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Remove-SPOAppPrioritizationPolicy
applicable: SharePoint Online
title: Remove-SPOAppPrioritizationPolicy
schema: 2.0.0
author: killerewok2000
ms.author: Sibourda
ms.reviewer:
---

# Remove-SPOAppPrioritizationPolicy

## SYNOPSIS

Deletes an existing SPO app prioritization policy in your tenancy.  
> [!NOTE]
> This functionality is rolling out and might not be fully enabled in your environment yet. 
## SYNTAX

```
Remove-SPOAppPrioritizationPolicy -PolicyId <String> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet lets you delete an existing SPO app prioritization policy.  

## EXAMPLES

### Example 1

```powershell
Remove-SPOAppPrioritizationPolicy -PolicyId 48abxxa9 
```

Example 1 deletes the policy bearing the policyId 48abxxa9. Running the `Get-SPOAppPrioritizationPolicies` command will no longer show the policy in the result. 

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
### CommonParameters
This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Add-SPOAppPrioritizationPolicy](./Add-SPOAppPrioritizationPolicy.md)

[Get-SPOAppPrioritizationPolicies](./Get-SPOAppPrioritizationPolicies.md)

[Set-SPOAppPrioritizationPolicy](./Set-SPOAppPrioritizationPolicy.md)