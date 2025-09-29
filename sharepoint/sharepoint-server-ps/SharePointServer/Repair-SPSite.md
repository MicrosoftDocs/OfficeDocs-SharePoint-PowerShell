---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/repair-spsite
applicable: SharePoint Server Subscription Edition
title: Repair-SPSite
schema: 2.0.0
---

# Repair-SPSite

## SYNOPSIS
Activates the RunRepairs method against the referenced SPSite object.

## SYNTAX

```
Repair-SPSite [-Identity] <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-RuleId <Guid>] [-RunAlways] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The `Repair-SPSite` cmdlet runs one or all site collection health checks on the site collection and its contents.
This cmdlet automatically repairs issues that it finds.

Run the `Test-SPSite` cmdlet for reports of rules which were run and a summary of the results.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Repair-SPSite https://<site name>/sites/testsite
```

This example runs all the site collection health checks in repair mode on the https://\<site name\>/sites/testsite site collection.

### EXAMPLE 2
```powershell
Repair-SPSite https://<site name>/sites/testsite -Rule "ee967197-ccbe-4c00-88e4-e6fab81145e1"
```

This example runs just the "Missing Galleries Check" in repair mode on the https://\<site name\>/sites/testsite site collection.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the URL or GUID of the site to run a repair.

```yaml
Type: SPSitePipeBind
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

### -RuleId

> Applicable: SharePoint Server Subscription Edition

Specifies the specific site health rule to run instead of running all applicable rules at once.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunAlways

> Applicable: SharePoint Server Subscription Edition

Forces a rule to run even if a health check was run.

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

[Test-SPSite](Test-SPSite.md)
