---
external help file: Microsoft.Office.Server.WorkManagement.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/new-spworkmanagementserviceapplicationproxy
applicable: SharePoint Server 2013
title: New-SPWorkManagementServiceApplicationProxy
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# New-SPWorkManagementServiceApplicationProxy

## SYNOPSIS
Creates a new Work Management Service application proxy.

## SYNTAX

```
New-SPWorkManagementServiceApplicationProxy -Name <String> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-DefaultProxyGroup] [-ServiceApplication <SPWorkManagementServiceCmdletPipeBind>] [-Uri <String>]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the `New-SPWorkManagementServiceApplicationProxy` cmdlet to create a new Work Management Service application proxy object.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

Note: This functionality has been removed from SharePoint Server 2016, SharePoint Server 2019, but the cmdlet is still present in the product.

## EXAMPLES

### EXAMPLE
```
$sa = New-SPWorkManagementServiceApplication -Name 'Work Management Service Application' -ApplicationPool 'SharePoint Web Services Default'
New-SPWorkManagementServiceApplicationProxy -name 'Work Management Service Application Proxy' -ServiceApplication $sa
```

This example creates a new SPWorkManagementServiceApplicationProxy called Work Management Service Application Proxy mapped to the "Work Management Service Application" Service Application.

## PARAMETERS

### -Name

> Applicable: SharePoint Server 2013

Specifies the display name for the new Work Management Service application proxy.
The name that you use must be a unique name of a Work Management Service application proxy in the farm.
The maximum length is 128 characters.

The value must be a name of a valid Work Management Service application proxy; for example, WorkMgmtSvcProxy1.

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

> Applicable: SharePoint Server 2013

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

> Applicable: SharePoint Server 2013

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

### -DefaultProxyGroup

> Applicable: SharePoint Server 2013

Specifies that the Work Management Service application proxy be added to the default proxy group for the local farm.

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

### -ServiceApplication

> Applicable: SharePoint Server 2013

Specifies the local Work Management Service application that is associated with the new proxy.

The value must be in one of the following forms:

--A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh

--A valid name of a Work Management Service application (for example, WorkManServ1)

--An instance of a valid SPServiceApplication object

```yaml
Type: SPWorkManagementServiceCmdletPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uri

> Applicable: SharePoint Server 2013

Specifies the URI of a remote Work Management service application to connect to.

To specify the Work Management service application that this proxy is connecting to, you must set only the URI parameter or only the ServiceApplication parameter.

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

### -WhatIf

> Applicable: SharePoint Server 2013

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

[New-SPWorkManagementServiceApplication](New-SPWorkManagementServiceApplication.md)

[Set-SPWorkManagementServiceApplication](Set-SPWorkManagementServiceApplication.md)

[Set-SPWorkManagementServiceApplicationProxy](Set-SPWorkManagementServiceApplicationProxy.md)
