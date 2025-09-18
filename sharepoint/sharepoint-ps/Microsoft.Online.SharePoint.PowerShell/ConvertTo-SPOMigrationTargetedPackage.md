---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/convertto-spomigrationtargetedpackage
applicable: SharePoint Online
title: ConvertTo-SPOMigrationTargetedPackage
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# ConvertTo-SPOMigrationTargetedPackage

## SYNOPSIS

Use this cmdlet to convert your XML files into a new migration package.

## SYNTAX

### DocumentLibraryImport
```
ConvertTo-SPOMigrationTargetedPackage [-SourceFilesPath] <String> [-SourcePackagePath] <String>
 [[-OutputPackagePath] <String>] [-TargetWebUrl] <String> -TargetDocumentLibraryPath <String>
 [-TargetDocumentLibrarySubFolderPath <String>] [-UserMappingFile <String>]
 -Credentials <CredentialCmdletPipeBind> [-AzureADUserCredentials <CredentialCmdletPipeBind>]
 [-NoAzureADLookup] [-TargetEnvironment <TargetEnvironment>] [-ParallelImport] [-PartitionSizeInBytes <Int64>]
 [-NoLogFile] [<CommonParameters>]
```

### ListImport
```
ConvertTo-SPOMigrationTargetedPackage [-SourceFilesPath] <String> [-SourcePackagePath] <String>
 [[-OutputPackagePath] <String>] [-TargetWebUrl] <String> -TargetListPath <String> [-UserMappingFile <String>]
 -Credentials <CredentialCmdletPipeBind> [-AzureADUserCredentials <CredentialCmdletPipeBind>]
 [-NoAzureADLookup] [-TargetEnvironment <TargetEnvironment>] [-ParallelImport] [-PartitionSizeInBytes <Int64>]
 [-NoLogFile] [<CommonParameters>]
```

## DESCRIPTION
Use this cmdlet to create a migration package from one Library to Another Library in form of a package. It converts the XML files and saves them as a new set of targeted migration package metadata files to the target directory.

## EXAMPLES

### Example 1

This example shows how to convert a package to a targeted one by looking up data in the target site collection. It uses the '-ParallelImport' parameter to boost file share migration performance.
```Powershell
$finalPackages = ConvertTo-SPOMigrationTargetedPackage -ParallelImport -SourceFilesPath $sourceFiles -SourcePackagePath $sourcePackage -OutputPackagePath $targetPackage -Credentials $cred -TargetWebUrl $targetWeb -TargetDocumentLibraryPath $targetDocLib
```

## PARAMETERS

### -AzureADUserCredentials

> Applicable: SharePoint Online

Receives Microsoft Entra User Credentials

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.CredentialCmdletPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credentials

> Applicable: SharePoint Online

Fill out the Regular Credentials (Get-Credential)

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.CredentialCmdletPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoAzureADLookup

> Applicable: SharePoint Online

Switch parameter that says if the command should or should not look up for Microsoft Entra ID.

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

### -OutputPackagePath

> Applicable: SharePoint Online

Output package path

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParallelImport

> Applicable: SharePoint Online

Switch parameter to boost file share migration performance.

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

### -PartitionSizeInBytes

> Applicable: SharePoint Online

Define the partition size in Bytes where it will be located the target package.

```yaml
Type: System.Int64
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
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePackagePath

> Applicable: SharePoint Online

Defines the source package path location.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDocumentLibraryPath

> Applicable: SharePoint Online

Defines the target document library path.

```yaml
Type: System.String
Parameter Sets: DocumentLibraryImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDocumentLibrarySubFolderPath

> Applicable: SharePoint Online

Defines the target document library subfolder path.

```yaml
Type: System.String
Parameter Sets: DocumentLibraryImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetEnvironment

> Applicable: SharePoint Online

Defines the Target environment: Production, ProductionChina, None or OnPremises.

```yaml
Type: Microsoft.Online.SharePoint.Migration.TargetEnvironment
Parameter Sets: (All)
Aliases:
Accepted values: Production, ProductionChina, None, OnPremises

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetListPath

> Applicable: SharePoint Online

Defines the Target list path

```yaml
Type: System.String
Parameter Sets: ListImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetWebUrl

> Applicable: SharePoint Online

Defines the Target Web URL of the package.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserMappingFile

> Applicable: SharePoint Online

Defines the file mapping of the user.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[ConvertTo-SPOMigrationEncryptedPackage](ConvertTo-SPOMigrationEncryptedPackage.md)
