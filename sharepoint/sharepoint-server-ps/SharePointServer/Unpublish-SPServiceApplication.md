---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/unpublish-spserviceapplication
applicable: SharePoint Server Subscription Edition
title: Unpublish-SPServiceApplication
schema: 2.0.0
---

# Unpublish-SPServiceApplication

## SYNOPSIS
Stops sharing the specified service application outside the farm.

## SYNTAX

```
Unpublish-SPServiceApplication [-Identity] <SPServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the `Unpublish-SPServiceApplication` cmdlet to stop publishing the service application, specified by the Identity parameter, outside the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
UnPublish-SPServiceApplication 053c34be-d251-488c-8e94-644eae94da26
```

This example stops publishing of the specified service application outside the farm.

The service application GUID is unique to every farm.
You can run the `Get-SPServiceApplication` cmdlet to see the GUID of the service applications and then use the result from the `Get-SPServiceApplication` cmdlet for other SPServiceApplication cmdlets; for example, `Publish-SPServiceApplication`.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the GUID of the service application to stop sharing outside the farm.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.

```yaml
Type: SPServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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
