---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/rename-spserver
applicable: SharePoint Server Subscription Edition
title: Rename-SPServer
schema: 2.0.0
---

# Rename-SPServer

## SYNOPSIS
Renames a server that is currently connected to the farm.

## SYNTAX

```
Rename-SPServer [-Identity] <SPServerPipeBind> -Name <String> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The `Rename-SPServer` cmdlet changes the name of the server for internal use within SharePoint Products.
The server itself must be manually renamed.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Rename-SPServer -Identity "wfb1" -Name "WFE1"
```

This example changes the name of the SharePoint server wfb1 to WFE1.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the original name of the server.

The type must be a URL, in the form https://server_name, or a GUID, in the form 1234-4567-987gb.

```yaml
Type: SPServerPipeBind
Parameter Sets: (All)
Aliases: Address

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the new name of the server.

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
