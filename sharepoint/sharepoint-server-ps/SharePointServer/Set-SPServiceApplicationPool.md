---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spserviceapplicationpool
applicable: SharePoint Server Subscription Edition
title: Set-SPServiceApplicationPool
schema: 2.0.0
---

# Set-SPServiceApplicationPool

## SYNOPSIS
Changes the account used for the Identity of the specified application pool.

## SYNTAX

```
Set-SPServiceApplicationPool [-Identity] <SPIisWebServiceApplicationPoolPipeBind>
 [[-Account] <SPProcessAccountPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPServiceApplicationPool` cmdlet changes the account used for the Identity of the specified application pool.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Set-SPServiceApplicationPool  TestServiceWebApplicationPool -Account testdomain\testuser1
```

This example changes the identity of the selected service application pool.

For the Account parameter, the name of a managed account in the farm can be given.
Use the `Get-SPManagedAccount` cmdlet to view the existing managed account in the farm.
Also, a process account from the output of the `Get-SPProcessAccount` cmdlet can be used.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the identity of the Web service application pool to configure.

```yaml
Type: SPIisWebServiceApplicationPoolPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Account

> Applicable: SharePoint Server Subscription Edition

Specifies the credentials that will be the new Identity of the application pool.

```yaml
Type: SPProcessAccountPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
