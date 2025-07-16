---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/export-spsitesubscriptionbusinessdatacatalogconfig
applicable: SharePoint Server Subscription Edition
title: Export-SPSiteSubscriptionBusinessDataCatalogConfig
schema: 2.0.0
---

# Export-SPSiteSubscriptionBusinessDataCatalogConfig

## SYNOPSIS

Exports all data from the Business Data Connectivity Metadata Store associated with a partition.


## SYNTAX

```
Export-SPSiteSubscriptionBusinessDataCatalogConfig -Path <String> -ServiceContext <SPServiceContextPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-Force] [-LocalizedNamesIncluded]
 [-ModelsIncluded] [-PermissionsIncluded] [-PropertiesIncluded] [-ProxiesIncluded] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
The SPSiteSubscriptionBusinessDataCatalogConfig cmdlet exports all data from the Business Data Connectivity Metadata Store associated with a specified partition.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Export-SPSiteSubscriptionBusinessDataCatalogConfig -ServiceContext http://contoso -Path "C:\folder\exportedFile.xml"
```

This example exports the data file named exportedFile.xml.

## PARAMETERS

### -Path

> Applicable: SharePoint Server Subscription Edition

Specifies the path and name to use to create the export file.

The type must be a valid path in either of the following forms:

- C:\folder_name\file.xml
- \\\\server_name\folder_name\file.xml
- ...\folder_name\file.xml

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

### -ServiceContext

> Applicable: SharePoint Server Subscription Edition

Specifies the service context of the data to be exported.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a service context (for example, http://ServiceContext1); or an instance of a valid SPServiceContext object.

```yaml
Type: SPServiceContextPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

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

### -Confirm

> Applicable: SharePoint Server Subscription Edition

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

> Applicable: SharePoint Server Subscription Edition

Overwrites the output file if the file exists.

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

### -LocalizedNamesIncluded

> Applicable: SharePoint Server Subscription Edition

Specifies that names for business data fields in multiple languages are exported.

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

### -ModelsIncluded

> Applicable: SharePoint Server Subscription Edition

Specifies that Business Data Connectivity models are included in the exported file.

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

### -PermissionsIncluded

> Applicable: SharePoint Server Subscription Edition

Specifies that permissions from the Business Data Connectivity Models are exported.

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

### -PropertiesIncluded

> Applicable: SharePoint Server Subscription Edition

Specifies that properties from the Business Data Connectivity Models are exported.

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

### -ProxiesIncluded

> Applicable: SharePoint Server Subscription Edition

Specifies that proxies for Business Data Connectivity Service applications are exported.

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

> Applicable: SharePoint Server Subscription Edition

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
