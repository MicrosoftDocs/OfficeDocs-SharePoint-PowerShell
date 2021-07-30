---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/update-spdataretrievalserviceconfig
applicable: SharePoint Server Subscription Edition
title: Update-SPDataRetrievalServiceConfig
schema: 2.0.0
author:
ms.author:
ms.reviewer:
---

# Update-SPDataRetrievalServiceConfig

## SYNOPSIS
This cmdlet configures settings for data retrieval services.

## SYNTAX

### WebApplication
```powershell
PS C:\> Update-SPDataRetrievalServiceConfig [-WebApplication] <SPWebApplicationPipeBind> [-Inherit] [-Enable <Boolean>]
 [-LimitResponseSize <Int32>] [-EnableUpdateSupport <Boolean>] [-DataSourceTimeout <Int32>]
 [-EnableDataSourceControls <Boolean>] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Farm
```powershell
PS C:\> Update-SPDataRetrievalServiceConfig [-Farm] [-Enable <Boolean>] [-LimitResponseSize <Int32>]
 [-EnableUpdateSupport <Boolean>] [-DataSourceTimeout <Int32>] [-EnableDataSourceControls <Boolean>]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see Cmdlet Parameter Sets (https://go.microsoft.com/fwlink/?LinkID=187810).

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at Windows PowerShell for SharePoint Server 2016 reference (https://go.microsoft.com/fwlink/p/?LinkId=671715).

## EXAMPLES

### -------------EXAMPLE 1------------- 
```powershell
PS C:\> Update-SPDataRetrievalServiceConfig -Farm -Enable $false
```

This example turns off the data retrieval service for the farm.

### -------------EXAMPLE 2------------- 
```powershell
PS C:\> Update-SPDataRetrievalServiceConfig -WebApplication http://MyOfficeApp1 -Inherit
```

This example enables the Web application, MyOfficeApp1, to inherit the global settings.

### -------------EXAMPLE 3------------- 
```powershell
PS C:\> Update-SPDataRetrievalServiceConfig -WebApplication http://MyOfficeApp1 -Enable $false
```

This example turns off the data retrieval service for the Web application, MyOfficeApp1.

## PARAMETERS

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

### -DataSourceTimeout
Set the response timeout in second.

This setting applies to the following data retrieval services:

OLEDB/

SOAP Passthrough

XML-URL

SoapDataSource

XmlUrlDataSource

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
@{Text=}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDataSourceControls
Enable or disable the set of data source controls on this server.

This setting applies to the following data source controls:

SPXmlDataSource

XmlUrlDataSource

SoapDataSource

AggregateDataSource

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUpdateSupport
Enable or disable the support for update queries.

This setting applies to the following data retrieval services:

OLEDB

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Farm
Apply the setting to the farm, and to all the SharePoint Web applications inherit the config.

```yaml
Type: SwitchParameter
Parameter Sets: Farm
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inherit
Set whether inherit the global setting of the farm.

```yaml
Type: SwitchParameter
Parameter Sets: WebApplication
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitResponseSize
The maximum size of the SOAP response that the data source returns to the data retrieval service, specified by kilobytes(KB).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplication
Apply the setting to the specified SharePoint Web application.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: WebApplication
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before executing the command.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Describes what would happen if you executed the command without actually executing the command.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: SharePoint Server Subscription Edition

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
