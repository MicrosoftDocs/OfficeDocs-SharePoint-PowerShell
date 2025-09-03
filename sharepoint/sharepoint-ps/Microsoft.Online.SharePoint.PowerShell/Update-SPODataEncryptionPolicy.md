---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/update-spodataencryptionpolicy
applicable: SharePoint Online
title: Update-SPODataEncryptionPolicy
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
ms.date: 07/30/2025
---

# Update-SPODataEncryptionPolicy

## SYNOPSIS

Updates customer encryption status for a geo tenant.

## SYNTAX

### BYOK_MultipleParameters (Default)

```
Update-SPODataEncryptionPolicy -KeyVaultName <String> -KeyName <String> -KeyVersion <Guid>
 -KeyType <CustomerKeyVaultKeyType> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BYOK_Uri

```
Update-SPODataEncryptionPolicy -KeyVaultUri <Uri> -KeyType <CustomerKeyVaultKeyType> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use the Update-SPODataEncryptionPolicy cmdlet to update customer encryption status for your geo tenant.
For more information, see [Controlling your data in Office 365 using Customer Key](/microsoft-365/compliance/controlling-your-data-using-customer-key)

## EXAMPLES

### Example 1

```powershell
Update-SPODataEncryptionPolicy -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType Primary
```

This example updates the DEP used with SharePoint Online and OneDrive for Business to start using the new key

## PARAMETERS

### -KeyName

The name of the key

```yaml
Type: System.String
Parameter Sets: BYOK_MultipleParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType

The type of the key, possible values are

- Primary
- Secondary

```yaml
Type: Microsoft.SharePoint.Client.CustomerKeyVaultKeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary, Availability

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultName

The name of the Azure Key Vault Name

```yaml
Type: System.String
Parameter Sets: BYOK_MultipleParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultUri

> Applicable: SharePoint Online

The Uri of the Azure Key Vault

```yaml
Type: System.Uri
Parameter Sets: BYOK_Uri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVersion

The version of the key

```yaml
Type: System.Guid
Parameter Sets: BYOK_MultipleParameters
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
