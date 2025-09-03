---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/update-spmachinekey
applicable: SharePoint Server Subscription Edition
title: Update-SPMachineKey
schema: 2.0.0
ms.date: 08/26/2025
---

# Update-SPMachineKey

## SYNOPSIS
Deploys ASP.NET view state decryption and validation keys to servers in the farm.

## SYNTAX

```
Update-SPMachineKey -WebApplication <SPWebApplicationPipeBind> [-Local]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The \`Update-SPMachineKey\` cmdlet deploys ASP.NET view state decryption and validation keys stored in the configuration database to servers in the farm.

## EXAMPLES

### EXAMPLE 1
```powershell
Update-SPMachineKey -WebApplication http://sitename
```

This example deploys the ASP.NET view state decryption and validation keys stored in the configuration database for web application 'http://sitename' to all servers in the farm.

### EXAMPLE 2
```powershell
Update-SPMachineKey -WebApplication http://sitename -Local
```

This example deploys the ASP.NET view state decryption and validation keys stored in the configuration database for web application 'http://sitename' to the local server.

## PARAMETERS

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

### -Local

> Applicable: SharePoint Server Subscription Edition

Deploy the decryption and validation keys only to the local server.
Other servers in the farm will continue to use the previous decryption and validation keys.
Web sessions that are load balanced across multiple servers in the farm will fail if these keys are not synchronized on every server in the farm.

If this parameter is not specified, the decryption and validation keys will be deployed to all servers in the farm.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the name, URL, or GUID of the Web application.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before running the cmdlet.

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

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
