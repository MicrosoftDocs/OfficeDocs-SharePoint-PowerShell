---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/restore-spodataencryptionpolicy
applicable: SharePoint Online
title: Restore-SPODataEncryptionPolicy
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Restore-SPODataEncryptionPolicy

## SYNOPSIS

Cmdlet to restore customer encryption status for your geo tenant when in recovery mode.
For more information, see [Controlling your data in Office 365 using Customer Key](/microsoft-365/compliance/controlling-your-data-using-customer-key)

## SYNTAX

### BYOK_MultipleParameters

```
Restore-SPODataEncryptionPolicy -PrimaryKeyVaultName <String> -PrimaryKeyName <String>
 -PrimaryKeyVersion <Guid> -SecondaryKeyVaultName <String> -SecondaryKeyName <String>
 -SecondaryKeyVersion <Guid> [<CommonParameters>]
```

### BYOK_Uri

```
Restore-SPODataEncryptionPolicy -PrimaryKeyVaultUri <Uri> -SecondaryKeyVaultUri <Uri> [<CommonParameters>]
```

## DESCRIPTION

Use the cmdlet to restore customer encryption status for your geo tenant when in recovery mode.
For more information, see [Controlling your data in Office 365 using Customer Key](/microsoft-365/compliance/controlling-your-data-using-customer-key)

## EXAMPLES

### Example 1

```powershell
Restore-SPODataEncryptionPolicy -PrimaryKeyVaultName 'PKVaultName1' -PrimaryKeyName 'PrimaryKey1' -PrimaryKeyVersion 'f635a23bd4a44b9996ff6aadd88d42ba' -SecondaryKeyVaultName 'SKVaultName1' -SecondaryKeyName 'SecondaryKey2' -SecondaryKeyVersion '2b3e8f1d754f438dacdec1f0945f251a'
```

This example restores the DEP used with SharePoint Online and OneDrive for Business to the given keys.

## PARAMETERS

### -PrimaryKeyName

> Applicable: SharePoint Online

The name of the primary key.

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

The name of the primary key vault.

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

The Uri of the primary key vault.

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

The version of the primary key.

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

The name of the secondary key.

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

The name of the secondary key vault.

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

The Uri of the secondary key vault.

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

The version of the secondary key.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
