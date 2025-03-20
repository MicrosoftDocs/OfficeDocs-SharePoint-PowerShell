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

Deletes an existing SPO app prioritization Policy in your tenancy.  

## SYNTAX

```powershell
Remove-SPOAppPrioritizationPolicy -PolicyId <string> 
```

## DESCRIPTION

This cmdlet lets you delete an existing policy.  

## EXAMPLES

### Example 1

```powershell
Remove-SPOAppPrioritizationPolicy -PolicyId 48abxxa9 
```

Example 1 deletes the policy bearing the policyId 48abxxa9. Running the Get command will no longer show the policy in the result. 

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

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Add-SPOAppPrioritizationPolicy](./Add-SPOAppPrioritizationPolicy.md)

[Get-SPOAppPrioritizationPolicies](./Get-SPOAppPrioritizationPolicies.md)

[Set-SPOAppPrioritizationPolicy](./Set-SPOAppPrioritizationPolicy.md)

[Remove-SPOAppPrioritizationPolicy](./Remove-SPOAppPrioritizationPolicy.md)
