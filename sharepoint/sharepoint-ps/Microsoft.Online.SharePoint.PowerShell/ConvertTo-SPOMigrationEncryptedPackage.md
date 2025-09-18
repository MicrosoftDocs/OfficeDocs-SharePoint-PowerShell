---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/convertto-spomigrationencryptedpackage
applicable: SharePoint Online
title: ConvertTo-SPOMigrationEncryptedPackage
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# ConvertTo-SPOMigrationEncryptedPackage

## SYNOPSIS

Use this Cmdlet to convert your XML files into a new encrypted migration package.

## SYNTAX

### ImplicitSourceParameterSet
```
ConvertTo-SPOMigrationEncryptedPackage -MigrationSourceLocations <MigrationPackageLocation>
 -EncryptionParameters <EncryptionParameters> -TargetFilesPath <String> -TargetPackagePath <String>
 [-NoLogFile] [<CommonParameters>]
```

### ExplicitSourceParameterSet
```
ConvertTo-SPOMigrationEncryptedPackage -SourceFilesPath <String> -SourcePackagePath <String>
 -EncryptionParameters <EncryptionParameters> -TargetFilesPath <String> -TargetPackagePath <String>
 [-NoLogFile] [<CommonParameters>]
```

## DESCRIPTION

This command convert the XML file on your temporary XML folder files into a new set of targeted migration encrypted metadata files to the target directory.

## EXAMPLES

### Example 1

```powershell
ConvertTo-SPOMigrationEncryptedPackage -EncryptionParameters SHA256 -MigrationSourceLocations $MigrationPackageLocation -NoLogFile -TargetFilesPath $TargetFilesPath -TargetPackagePath $TargetPackagePath
```

Changes a migration package to a migration encrypted package on the "migrationSourceLocations" , with log file on the current tenant

### Example 2

```powershell
ConvertTo-SPOMigrationEncryptedPackage -EncryptionParameters SHA384 -MigrationSourceLocations $MigrationPackageLocation  -TargetFilesPath $TargetFilesPath -TargetPackagePath $TargetPackagePath
```

Same as example1 but without log file and using an encryption type SHA384

## PARAMETERS

### -EncryptionParameters

> Applicable: SharePoint Online

Parameters of the encryption, it doesn't accept wildcard characters.
It accepts parameters like SHA384, SHA256, etc.

```yaml
Type: Microsoft.Online.SharePoint.Migration.EncryptionParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationSourceLocations

> Applicable: SharePoint Online

Possible Source locations to migrate

```yaml
Type: Microsoft.Online.SharePoint.Migration.MigrationPackageLocation
Parameter Sets: ImplicitSourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoLogFile

> Applicable: SharePoint Online

Switch Parameter to determine if you should get or not a log file.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilesPath

> Applicable: SharePoint Online

Defines the temporary Path where are located the XML source files.

```yaml
Type: System.String
Parameter Sets: ExplicitSourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePackagePath

> Applicable: SharePoint Online

Defines the source package path location.

```yaml
Type: System.String
Parameter Sets: ExplicitSourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFilesPath

> Applicable: SharePoint Online

Defines the temporary Path where are located the XML source files.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetPackagePath

> Applicable: SharePoint Online

Defines the source package path location of the package to be encrypted.

```yaml
Type: System.String
Parameter Sets: (All)
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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[ConvertTo-SPOMigrationTargetedPackage](ConvertTo-SPOMigrationTargetedPackage.md)
[Migrate to SharePoint Online using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets)
