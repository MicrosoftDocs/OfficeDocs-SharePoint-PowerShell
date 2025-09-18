---
external help file: sharepointserver.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/set-spexcelbiserver
applicable: SharePoint Server 2010, SharePoint Server 2013
title: Set-SPExcelBIServer
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Set-SPExcelBIServer

## SYNOPSIS

Specifies a description for an existing BI server for Excel Services.

## SYNTAX

```
Set-SPExcelBIServer [-Identity] <SPExcelBIServerPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-Description <String>] -ExcelServiceApplication <SPExcelServiceApplicationPipeBind>
 [-ServerId <String>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the Set-SPExcelBIServer cmdlet to specify a description for an existing BI server for Excel Services.

## EXAMPLES

### EXAMPLE
```
$sa = Get-SPServiceApplication | ?{$_.TypeName -eq 'Excel Services Application Web Service Application'}
Set-SPExcelBIServer -Identity "ExcelServices" -ExcelServiceApplication $sa
```

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server 2010, SharePoint Server 2013

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

**NOTE**: When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

> Applicable: SharePoint Server 2010, SharePoint Server 2013

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

### -Description

> Applicable: SharePoint Server 2010, SharePoint Server 2013

Specifies the description of the Analysis server.

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

### -ExcelServiceApplication

> Applicable: SharePoint Server 2010, SharePoint Server 2013

Specifies the Excel Services Application Web service application that contains the SPExcelFileLocation list object.The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an Excel Services Application Web service application in the farm (for example, MyExcelService1); or an instance of a valid SPExcelServiceApplication object.

```yaml
Type: SPExcelServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Server 2010, SharePoint Server 2013

Specifies the ExcelServiceApplication identity.

```yaml
Type: SPExcelBIServerPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServerId

> Applicable: SharePoint Server 2010, SharePoint Server 2013

The name of the Analysis Services server.

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

> Applicable: SharePoint Server 2010, SharePoint Server 2013

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Office.Excel.Server.Cmdlet.SPExcelBIServerPipeBind
Microsoft.Office.Excel.Server.Cmdlet.SPExcelServiceApplicationPipeBind
Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
