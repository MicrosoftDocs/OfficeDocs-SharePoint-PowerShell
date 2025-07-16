---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spscaleoutdatabase
applicable: SharePoint Server Subscription Edition
title: Get-SPScaleOutDatabase
schema: 2.0.0
---

# Get-SPScaleOutDatabase

## SYNOPSIS

Returns all scale-out database objects.


## SYNTAX

```
Get-SPScaleOutDatabase -ServiceApplication <SPServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the Get-SPScaleOutDatabase cmdlet to returns all scale-out database objects for the specified service application.

A scale-out database is a database which implements the Shared Service Database Scale Out Generic Protocol.
For additional information about the Database Scale Out Generic Protocol, see SharePoint Shared Service Database Scale Out Generic Protocol Specification (https://msdn.microsoft.com/en-us/library/hh656675(office.12).aspx)

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$serviceApplication = Get-SPServiceApplication -Name "AppManagement"
Get-SPScaleOutDatabase -ServiceApplication $serviceApplication
```

This example gets all scale-out databases for the given service application by using the $serviceApplication variable.

## PARAMETERS

### -ServiceApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the service application of the scale-out databases.

```yaml
Type: SPServiceApplicationPipeBind
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

[Add-SPScaleOutDatabase](Add-SPScaleOutDatabase.md)

[Remove-SPScaleOutDatabase](Remove-SPScaleOutDatabase.md)

[Split-SPScaleOutDatabase](Split-SPScaleOutDatabase.md)
