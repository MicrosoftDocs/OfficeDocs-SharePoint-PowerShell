---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-sproutingmachinepool
applicable: SharePoint Server Subscription Edition
title: Get-SPRoutingMachinePool
schema: 2.0.0
---

# Get-SPRoutingMachinePool

## SYNOPSIS

Returns all available routing pools.



## SYNTAX

```
Get-SPRoutingMachinePool [-RequestManagementSettings] <SPRequestManagementSettingsPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Name <String>] [<CommonParameters>]
```

## DESCRIPTION
Use the Get-SPRoutingMachinePool cmdlet to return all available routing pools by using the RequestManagementSettings parameter.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### --------------EXAMPLE--------- 
```powershell
$web=Get-SPWebApplication -Identity <URL of web application>
$rm=Get-SPRequestManagementSettings -Identity $web
Get-SPRoutingMachinePool -RequestManagementSettings $rm
```

This example returns a routing pool for the specified identity.

## PARAMETERS

### -RequestManagementSettings
Specifies the name of the request management settings object to return.

```yaml
Type: SPRequestManagementSettingsPipeBind
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection
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
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of the machine pool to return.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

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

[Add-SPRoutingMachinePool](Add-SPRoutingMachinePool.md)

[Remove-SPRoutingMachinePool](Remove-SPRoutingMachinePool.md)

[Set-SPRoutingMachinePool](Set-SPRoutingMachinePool.md)
