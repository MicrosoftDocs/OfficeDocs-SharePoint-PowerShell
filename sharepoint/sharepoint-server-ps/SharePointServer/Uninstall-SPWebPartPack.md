---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/uninstall-spwebpartpack
applicable: SharePoint Server Subscription Edition
title: Uninstall-SPWebPartPack
schema: 2.0.0
---

# Uninstall-SPWebPartPack

## SYNOPSIS
Uninstalls the specified Web Part package.

## SYNTAX

```
Uninstall-SPWebPartPack [-Identity] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-Language <UInt32>] [-WebApplication <SPWebApplicationPipeBind>] [-WhatIf] [-CompatibilityLevel <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The `Uninstall-SPWebPartPack` cmdlet uninstalls the Web Part package specified by the Identity parameter.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Uninstall-SPWebPartPack  "mypart.wpp" -WebApplication https://portal
```

This example uninstalls mypart.wpp to from the Web application https://portal.

### EXAMPLE 2
```powershell
Get-SPWebPartPack -WebApplication https://portal | Uninstall-SPWebPartPack
```

This example uninstalls all Web part packages from the Web application https://portal.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the Web Part package in the farm's configuration database.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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
If objects are not immediately used, or disposed of by using the `Stop-SPAssignment` command, an out-of-memory scenario can occur.

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

### -Language

> Applicable: SharePoint Server Subscription Edition

Specifies the language ID of the Web Part package to delete.
If no language is specified, the Web Part package is uninstalled for all languages.

The type must be a valid language identifier, in the form 1033.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the Web application from which to uninstall the Web Part package.
If no Web application is specified, the Web Part package is uninstalled from all Web applications.

The type must be a valid name, in the form WebApplication-1212, or a URL, in the form  https://server_name/WebApplication-1212.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -CompatibilityLevel

> Applicable: SharePoint Server Subscription Edition

{{Fill CompatibilityLevel Description}}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
