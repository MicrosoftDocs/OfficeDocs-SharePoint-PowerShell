---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/export-spweb
applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: Export-SPWeb
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Export-SPWeb

## SYNOPSIS

Exports a site, list, or library.


## SYNTAX

```
Export-SPWeb [-Identity] <SPWebPipeBind> -Path <String> [-AppLogFilePath <String>]
 [-AssignmentCollection <SPAssignmentCollection>] [-CompressionSize <Int32>] [-Confirm] [-Force] [-HaltOnError]
 [-HaltOnWarning] [-IncludeUserSecurity] [-IncludeVersions <SPIncludeVersions>] [-ItemUrl <String>]
 [-NoFileCompression] [-NoLogFile] [-UseSqlSnapshot] [-WhatIf] [-IncludeAlerts] [<CommonParameters>]
```

## DESCRIPTION
The Export-SPWeb cmdlet exports a site, list, or library.
The capability to export from a library is a new feature in SharePoint.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE.
```
Export-SPWeb https://site -Path "C:\Temp\export.cmp"
```

This example exports the site at https://site/ to a file called site export.cmp in the current directory.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the URL or GUID of the Web to be exported.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint site (for example, MySPSite1); or an instance of a valid SPWeb object.

```yaml
Type: SPWebPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the export file.

If the NoFileCompression parameter is used, a directory must be specified; otherwise, any file format is valid.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppLogFilePath

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CompressionSize

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Sets the maximum file size for the compressed export files.
If the total size of the exported package is greater than this size, the exported package will be split into multiple files.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

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

### -Force

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Forcefully overwrites the export package if it already exists.

The type must be either of the following values:

-True

-False

The default value is False.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HaltOnError

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Stops the export process when an error occurs.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HaltOnWarning

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Stops the export process when a warning occurs.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeUserSecurity

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Preserves the user security settings.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeVersions

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Indicates the type of file and list item version history to be included in the export operation.
If the IncludeVersions parameter is absent, the Export-SPWeb cmdlet by default uses a value of 1.

The type must be any one of the following versions:

-Last major version for files and list items (default)

-The current version, either the last major version or the last minor version

-Last major and last minor version for files and list items

-All versions for files and list items

Valid values are:

All, CurrentVersion, LastMajor, LastMajorAndMinor

```yaml
Type: SPIncludeVersions
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ItemUrl

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the URL of the Web application, GUID, or object to be exported.

The type must be a valid URL; for example, https://server_name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoFileCompression

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Either enables or disables file compression in the export package.
The export package is stored in the folder specified by the Path parameter or Identity parameter.
We recommend that you use this parameter for performance reasons.
If compression is enabled, the export process can increase by approximately 30 percent.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoLogFile

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Suppresses the generation of an export log file.
If this parameter is not specified, the Export-SPWeb cmdlet will generate an export log file in the same location as the export package.
The log file uses Unified Logging Service (ULS).

It is recommended to use this parameter.
However, for performance reasons, you might not want to generate a log file.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSqlSnapshot

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies a SQL Database Snapshot will be created when the export process begins, and all exported data will be retrieved directly from the database snapshot.
This snapshot will be automatically deleted when export completes.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: `get-help about_commonparameters`

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

### -IncludeAlerts

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Indicates if alerts are turned on.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
