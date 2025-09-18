---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/invoke-spomigrationencryptuploadsubmit
applicable: SharePoint Online
title: Invoke-SPOMigrationEncryptUploadSubmit
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Invoke-SPOMigrationEncryptUploadSubmit

## SYNOPSIS

**Note**: This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).

Creates a new migration job in the target site collection.

## SYNTAX

### ImplicitSourceParameterSet

```
Invoke-SPOMigrationEncryptUploadSubmit -MigrationSourceLocations <MigrationPackageLocation>
 -Credentials <CredentialCmdletPipeBind> -TargetWebUrl <String> [-NoLogFile] [-ParallelUpload]
 [<CommonParameters>]
```

### ExplicitSourceParameterSet

```
Invoke-SPOMigrationEncryptUploadSubmit -SourceFilesPath <String> -SourcePackagePath <String>
 -Credentials <CredentialCmdletPipeBind> -TargetWebUrl <String> [-NoLogFile] [-ParallelUpload]
 [<CommonParameters>]
```

## DESCRIPTION

Creates a new migration job in the target site collection, and then returns a GUID representing the JobID. This command will upload encrypted source files and manifests into temporary Azure blob storage per job.

## EXAMPLES

### Example 1

```powershell
$job = Invoke-SPOMigrationEncryptUploadSubmit -SourceFilesPath $sourceFiles -SourcePackagePath $spoPackagePath -Credentials $cred -TargetWebUrl $targetWebUrl
```

This example shows how to submit package data to create a new migration job

### Example 2

```Powershell
$sourceFiles = "sourceFiles"
$spoPackagePath = "packagePath"
$credentials = Get-Credential
$targetweburl = "https://contoso.sharepoint.com"
Invoke-SPOMigrationEncryptUploadSubmit -SourceFilesPath $sourceFiles -SourcePackagePath $spoPackagePath -Credentials $credentials -TargetWebUrl $targetweburl
```

This example shows how to submit package data to create a new migration job.

This article contains the steps on how to create this package: <https://support.office.com/en-us/article/upload-on-premises-content-to-sharepoint-online-using-powershell-cmdlets-555049c6-15ef-45a6-9a1f-a1ef673b867c>

### Example 3

This example shows how to submit package data to create new migration jobs for parallel import.

```Powershell
$jobs = $finalPackages | % {Invoke-SPOMigrationEncryptUploadSubmit -SourceFilesPath $_.FilesDirectory.FullName -SourcePackagePath $_.PackageDirectory.FullName -Credentials $cred -TargetWebUrl $targetWeb}
```

## PARAMETERS

### -Credentials

> Applicable: SharePoint Online

Parameter to fill out credentials of the SPO tenant.

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

### -MigrationSourceLocations

> Applicable: SharePoint Online

Migration Location where the package lies.

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

Controls if a log will be created or not

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

Source files Path, string

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

Source Package Path.

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

### -TargetWebUrl

> Applicable: SharePoint Online

Target web URL

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

[Upload on-premises content to SharePoint Online using PowerShell cmdlets](https://support.office.com/en-us/article/upload-on-premises-content-to-sharepoint-online-using-powershell-cmdlets-555049c6-15ef-45a6-9a1f-a1ef673b867c)

[Get-SPOAppErrors](Get-SPOAppErrors.md)
