---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spbusinessdatacatalogthrottleconfig
applicable: SharePoint Server Subscription Edition
title: Set-SPBusinessDataCatalogThrottleConfig
schema: 2.0.0
---

# Set-SPBusinessDataCatalogThrottleConfig

## SYNOPSIS
Sets the throttling configuration for a Business Data Connectivity Service application.

## SYNTAX

### MaxDefault
```
Set-SPBusinessDataCatalogThrottleConfig -Default <Int32> -Identity <ThrottleConfig> -Maximum <Int32>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Enforcement
```
Set-SPBusinessDataCatalogThrottleConfig [-Enforced] -Identity <ThrottleConfig>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The `Set-SPBusinessDataCatalogThrottleConfig` cmdlet sets the throttling configuration for a Business Data Connectivity Service application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Get-SPBusinessDataCatalogThrottleConfig -Scope Database -ThrottleType Items -ServiceApplicationProxy $contosoServAppProxy | Set-SPBusinessDataCatalogThrottleConfig -Maximum 1000000000 -Default 500000
```

This example sets the database item throttling to values of 1000000000 maximum and 500000 default for the given service application.

## PARAMETERS

### -Default

> Applicable: SharePoint Server Subscription Edition

Specifies the default setting of the throttle configuration.

```yaml
Type: Int32
Parameter Sets: MaxDefault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enforced

> Applicable: SharePoint Server Subscription Edition

Specifies that the throttle configuration setting cannot be overridden.

```yaml
Type: SwitchParameter
Parameter Sets: Enforcement
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the throttle configuration to update.

```yaml
Type: ThrottleConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Maximum

> Applicable: SharePoint Server Subscription Edition

Specifies the maximum value of the throttling configuration setting.

```yaml
Type: Int32
Parameter Sets: MaxDefault
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
