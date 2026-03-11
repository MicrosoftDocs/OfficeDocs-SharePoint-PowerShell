---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-sposerviceprioritizationbillingpolicy
title: Remove-SPOServicePrioritizationBillingPolicy
schema: 2.0.0
author: juanoriana
ms.author: 
ms.reviewer:
---

# Remove-SPOServicePrioritizationBillingPolicy

## SYNOPSIS

Removes all app registrations linked to a SharePoint Online Service Prioritization billing policy and then deletes the billing policy itself.

## SYNTAX

```powershell
Remove-SPOServicePrioritizationBillingPolicy -PolicyId <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet removes all app registrations associated with the specified billing policy in a single server-side operation, and then deletes the billing policy from Azure Resource Manager.

The billing policy is only deleted if all linked app registrations were successfully removed. If any registrations could not be confirmed as deleted, the billing policy is left intact and the unconfirmed app IDs are reported in `FailedAppIds`.

By default, the cmdlet prompts for confirmation before deleting. Use `-Force` to suppress the confirmation prompt.

You must be a SharePoint Online administrator to run this cmdlet.

## EXAMPLES

### Example 1

```powershell
Remove-SPOServicePrioritizationBillingPolicy -PolicyId 11111111-1111-1111-1111-111111111111
```

Example 1 prompts for confirmation, then removes all app registrations linked to the specified billing policy and deletes the billing policy.

### Example 2

```powershell
Remove-SPOServicePrioritizationBillingPolicy -PolicyId 11111111-1111-1111-1111-111111111111 -Force
```

Example 2 removes all app registrations linked to the specified billing policy and deletes the billing policy without prompting for confirmation.

## PARAMETERS

### -PolicyId

The unique identifier of the SPO Service Prioritization billing policy to remove.

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

### -Force

Suppresses the confirmation prompt. Without this switch, the cmdlet displays the number of app registrations and billing policy that will be deleted and requires confirmation before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

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

If `BillingPolicyDeleted` is `false` and `FailedAppIds` is `null`, the app registrations were removed but the billing policy itself could not be deleted. The billing policy may need to be removed manually.

## RELATED LINKS

[Get-SPOServicePrioritizationAppRegistrations](Get-SPOServicePrioritizationAppRegistrations.md)

[Remove-SPOServicePrioritizationAppRegistration](Remove-SPOServicePrioritizationAppRegistration.md)

[Remove-SPOServicePrioritizationAppRegistrationsByPolicy](Remove-SPOServicePrioritizationAppRegistrationsByPolicy.md)

[New-SPOServicePrioritizationBillingPolicy](New-SPOServicePrioritizationBillingPolicy.md)

[Get-SPOServicePrioritizationBillingPolicies](Get-SPOServicePrioritizationBillingPolicies.md)
