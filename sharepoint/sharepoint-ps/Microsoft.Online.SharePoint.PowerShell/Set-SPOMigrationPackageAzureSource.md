---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spomigrationpackageazuresource
applicable: SharePoint Online
title: Set-SPOMigrationPackageAzureSource
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
ms.date: 07/30/2025
---

# Set-SPOMigrationPackageAzureSource

## SYNOPSIS

Cmdlet to create Azure containers, upload migration package files into the appropriate containers and snapshot the uploaded content.

## SYNTAX

### ImplicitSourceExplicitAzure

```
Set-SPOMigrationPackageAzureSource -MigrationSourceLocations <MigrationPackageLocation>
 [-FileContainerName <String>] [-PackageContainerName <String>] [-AzureQueueName <String>]
 -AccountName <String> -AccountKey <String> [-EncryptionParameters <EncryptionParameters>] [-NoUpload]
 [-NoSnapshotCreation] [-EncryptionMetaInfo <MigrationFileEncryptionInfo[]>] [-NoLogFile] [-Overwrite]
 [-ParallelUpload] [<CommonParameters>]
```

### ImplicitSourceImplicitAzure

```
Set-SPOMigrationPackageAzureSource -MigrationSourceLocations <MigrationPackageLocation>
 -MigrationPackageAzureLocations <MigrationPackageAzureLocations>
 [-EncryptionParameters <EncryptionParameters>] [-NoUpload] [-NoSnapshotCreation]
 [-EncryptionMetaInfo <MigrationFileEncryptionInfo[]>] [-NoLogFile] [-Overwrite] [-ParallelUpload]
 [<CommonParameters>]
```

### ExplicitSourceExplicitAzure

```
Set-SPOMigrationPackageAzureSource -SourceFilesPath <String> -SourcePackagePath <String>
 [-FileContainerName <String>] [-PackageContainerName <String>] [-AzureQueueName <String>]
 -AccountName <String> -AccountKey <String> [-EncryptionParameters <EncryptionParameters>] [-NoUpload]
 [-NoSnapshotCreation] [-EncryptionMetaInfo <MigrationFileEncryptionInfo[]>] [-NoLogFile] [-Overwrite]
 [-ParallelUpload] [<CommonParameters>]
```

### ExplicitSourceImplicitAzure

```
Set-SPOMigrationPackageAzureSource -SourceFilesPath <String> -SourcePackagePath <String>
 -MigrationPackageAzureLocations <MigrationPackageAzureLocations>
 [-EncryptionParameters <EncryptionParameters>] [-NoUpload] [-NoSnapshotCreation]
 [-EncryptionMetaInfo <MigrationFileEncryptionInfo[]>] [-NoLogFile] [-Overwrite] [-ParallelUpload]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see Cmdlet Parameter Sets.

This cmdlet returns a Microsoft.Online.SharePoint.Migration. MigrationPackageAzureLocations object, which can be used as a source for this cmdlet or, more commonly, as a source for the `Submit-SPOMigrationJob` cmdlet.

## EXAMPLES

### EXAMPLE 1

```powershell
$azurelocations = Set-SPOMigrationPackageAzureSource -SourcePath \\fileserver\share\folder1 -OutputPackagePath d:\MigrationPackages\Folder1_TgtPkg -FileContainerUri migration-files -PackageContainerUri migration-package -AccountName migrationstore -AccountKey "nmcXQ+1NctB7BlRVm+8+qWUn6GUFIH7E5ZQPThcjg8SfFWTJ34HthyOEoROwxHYIajpOYxYDt7qUwSEBQlLWoA=="
```

This example creates migration package containers in Azure storage using the supplied account credentials, uploads the package files into them, snapshots the files and lastly returns the connection strings to a PowerShell variable.

### EXAMPLE 2

```powershell
Set-SPOMigrationPackageAzureSource -SourcePath \\fileserver\share\folder1 -OutputPackagePath d:\MigrationPackages\Folder1_TgtPkg -MigrationPackageAzureLocations $azurelocations -AccountName migrationstore -AccountKey "nmcXQ+1NctB7BlRVm+8+qWUn6GUFIH7E5ZQPThcjg8SfFWTJ34HthyOEoROwxHYIajpOYxYDt7qUwSEBQlLWoA==" -NoUpload
```

This example uses existing migration package containers in Azure storage to snapshot previously uploaded files and then returns the connection strings to a PowerShell variable.

## PARAMETERS

### -AccountKey

> Applicable: SharePoint Online

The account key for the Azure Storage account.

```yaml
Type: System.String
Parameter Sets: ImplicitSourceExplicitAzure, ExplicitSourceExplicitAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountName

> Applicable: SharePoint Online

The account name for the Azure Storage account.

```yaml
Type: System.String
Parameter Sets: ImplicitSourceExplicitAzure, ExplicitSourceExplicitAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureQueueName

> Applicable: SharePoint Online

An optional name of the Azure Storage Reporting Queue where import operations lists events during import. This value must be in lower case and conform to Azure's queue naming rules.

```yaml
Type: System.String
Parameter Sets: ImplicitSourceExplicitAzure, ExplicitSourceExplicitAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionMetaInfo

> Applicable: SharePoint Online

PARAMVALUE: MigrationFileEncryptionInfo[]

```yaml
Type: Microsoft.Online.SharePoint.Migration.MigrationFileEncryptionInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionParameters

> Applicable: SharePoint Online

An EncryptionParameters object. See [New-SPOMigrationEncryptionParameters](/powershell/module/sharepoint-online/new-spomigrationencryptionparameters) for more information.

```yaml
Type: Microsoft.Online.SharePoint.Migration.EncryptionParameters
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileContainerName

> Applicable: SharePoint Online

The optional name of the Azure Blob Storage container that will be created if it does not currently exist. It will hold the uploaded package content files. The value must be in lower case and conform to Azure's container naming rules. If this not supplied a name will be generated using the format \<GUID\>-files.

```yaml
Type: System.String
Parameter Sets: ImplicitSourceExplicitAzure, ExplicitSourceExplicitAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationPackageAzureLocations

> Applicable: SharePoint Online

A set of fully qualified URLs and SAS tokens representing the Azure Blob Storage containers that hold the package content and metadata files and an optional Azure Storage Reporting Queue. This object is returned during successful processing of the `Set-SPOMigrationPackageAzureSource`

```yaml
Type: Microsoft.Online.SharePoint.Migration.MigrationPackageAzureLocations
Parameter Sets: ImplicitSourceImplicitAzure, ExplicitSourceImplicitAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationSourceLocations

> Applicable: SharePoint Online

Possible Source locations to migrate.

```yaml
Type: Microsoft.Online.SharePoint.Migration.MigrationPackageLocation
Parameter Sets: ImplicitSourceExplicitAzure, ImplicitSourceImplicitAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoLogFile

> Applicable: SharePoint Online

Indicates to not create a log file. The default is to create a new CopyMigrationPackage log file within the directory specified within the SourcePackagePath parameter.

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

### -NoSnapshotCreation

> Applicable: SharePoint Online

Indicates to not perform snapshots on the content in the containers. The default is to snapshot each of the packages files in the containers.

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

### -NoUpload

> Applicable: SharePoint Online

Indicates to not upload the package files. The default is to upload all the package files.

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

### -Overwrite

> Applicable: SharePoint Online

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

### -PackageContainerName

> Applicable: SharePoint Online

The optional name of the Azure Blob Storage container that will be created if it does not currently exist. It will hold the uploaded package metadata files. The value must be in lower case and conform to Azure's container naming rules. If this not supplied a name will be generated using the format \<GUID\>-package.

```yaml
Type: System.String
Parameter Sets: ImplicitSourceExplicitAzure, ExplicitSourceExplicitAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParallelUpload

> Applicable: SharePoint Online

Whether to enable parallel upload of files to Azure.

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

The directory location where the package's source content files exist.

```yaml
Type: System.String
Parameter Sets: ExplicitSourceExplicitAzure, ExplicitSourceImplicitAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePackagePath

> Applicable: SharePoint Online

The directory location where the package's metadata files exist.

```yaml
Type: System.String
Parameter Sets: ExplicitSourceExplicitAzure, ExplicitSourceImplicitAzure
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
