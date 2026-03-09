---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-sposerviceprioritizationappregistrationsbypolicy
schema: 2.0.0
---

# Remove-SPOServicePrioritizationAppRegistrationsByPolicy

## SYNOPSIS

Removes all app registrations linked to a specific SharePoint Online Service Prioritization billing policy.

## SYNTAX

```powershell
Remove-SPOServicePrioritizationAppRegistrationsByPolicy -PolicyId <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The `Remove-SPOServicePrioritizationAppRegistrationsByPolicy` cmdlet removes all app registrations associated with the specified billing policy in a single server-side operation.

Before deletion, the cmdlet verifies that the billing policy exists and that at least one app registration is linked to it. If neither condition is met, the cmdlet exits silently.

By default, the cmdlet prompts for confirmation before deleting. Use `-Force` to suppress the confirmation prompt.

You must be a SharePoint Online administrator to run this cmdlet.

## EXAMPLES

### Example 1: Remove all app registrations for a billing policy

```powershell
Remove-SPOServicePrioritizationAppRegistrationsByPolicy -PolicyId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
```

Prompts for confirmation, then removes all app registrations linked to the specified billing policy.

### Example 2: Remove without confirmation prompt

```powershell
Remove-SPOServicePrioritizationAppRegistrationsByPolicy -PolicyId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Force
```

Removes all app registrations linked to the specified billing policy without prompting for confirmation.

## PARAMETERS

### -PolicyId

The unique identifier of the SPO Service Prioritization billing policy whose app registrations should be removed.

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

Suppresses the confirmation prompt. Without this switch, the cmdlet displays the number of app registrations that will be deleted and requires confirmation before proceeding.

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

### Microsoft.Online.SharePoint.PowerShell.SPOServicePrioritizationBulkDeleteResult

| Property | Type | Description |
|---|---|---|
| SuccessCount | Int32 | The number of app registrations successfully removed. |
| FailedAppIds | List\<String\> | App IDs that could not be confirmed as deleted, populated only when the server reports fewer deletions than expected. `null` when all registrations were deleted successfully. |
| BillingPolicyDeleted | Boolean | Always `false` for this cmdlet. Use `Remove-SPOServicePrioritizationBillingPolicy` to delete the billing policy. |

## NOTES

## RELATED LINKS

[Get-SPOServicePrioritizationAppRegistrations](Get-SPOServicePrioritizationAppRegistrations.md)

[Add-SPOServicePrioritizationAppRegistration](Add-SPOServicePrioritizationAppRegistration.md)

[Remove-SPOServicePrioritizationAppRegistration](Remove-SPOServicePrioritizationAppRegistration.md)

[Remove-SPOServicePrioritizationBillingPolicy](Remove-SPOServicePrioritizationBillingPolicy.md)

[Get-SPOServicePrioritizationBillingPolicies](Get-SPOServicePrioritizationBillingPolicies.md)
