---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/register-spodataencryptionpolicy
applicable: SharePoint Online
title: Register-SPODataEncryptionPolicy
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Register-SPODataEncryptionPolicy

## SYNOPSIS

Cmdlet to register customer encryption status for your geo tenant.
For more information, see [Controlling your data in Office 365 using Customer Key](/microsoft-365/compliance/controlling-your-data-using-customer-key)

## SYNTAX

### BYOK_MultipleParameters (Default)

```
Register-SPODataEncryptionPolicy -PrimaryKeyVaultName <String> -PrimaryKeyName <String>
 -PrimaryKeyVersion <Guid> -SecondaryKeyVaultName <String> -SecondaryKeyName <String>
 -SecondaryKeyVersion <Guid> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BYOK_Uri

```
Register-SPODataEncryptionPolicy -PrimaryKeyVaultUri <Uri> -SecondaryKeyVaultUri <Uri> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use the Register-DataEncryptionPolicy cmdlet to register customer encryption status for your geo tenant.
For more information, see [Controlling your data in Office 365 using Customer Key](/microsoft-365/compliance/controlling-your-data-using-customer-key)

## EXAMPLES

### Example 1

```powershell
Register-SPODataEncryptionPolicy -PrimaryKeyVaultName 'PKVaultName1' -PrimaryKeyName 'PrimaryKey1' -PrimaryKeyVersion 'f635a23bd4a44b9996ff6aadd88d42ba' -SecondaryKeyVaultName 'SKVaultName1' -SecondaryKeyName 'SecondaryKey2' -SecondaryKeyVersion '2b3e8f1d754f438dacdec1f0945f251a'
```

This example registers the DEP used with SharePoint Online and OneDrive for Business to start using the given primary key.

## PARAMETERS

### -PrimaryKeyName

> Applicable: SharePoint Online

The name of the primary key

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

### -PrimaryKeyVaultName

> Applicable: SharePoint Online

The name of the primary key vault

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

### -PrimaryKeyVaultUri

> Applicable: SharePoint Online

The Uri of the primary key vault

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

### -PrimaryKeyVersion

> Applicable: SharePoint Online

The version of the primary key

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

### -SecondaryKeyName

> Applicable: SharePoint Online

The name of the secondary key

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

### -SecondaryKeyVaultName

> Applicable: SharePoint Online

The name of the secondary key vault

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

### -SecondaryKeyVaultUri

> Applicable: SharePoint Online

The Uri of the secondary key vault

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

### -SecondaryKeyVersion

> Applicable: SharePoint Online

The version of the secondary key

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

> Applicable: SharePoint Online

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

> Applicable: SharePoint Online

The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
