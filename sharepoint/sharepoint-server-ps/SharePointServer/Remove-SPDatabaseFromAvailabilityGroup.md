---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/remove-spdatabasefromavailabilitygroup
applicable: SharePoint Server Subscription Edition
title: Remove-SPDatabaseFromAvailabilityGroup
schema: 2.0.0
ms.date: 08/26/2025
---

# Remove-SPDatabaseFromAvailabilityGroup

## SYNOPSIS
Removes one or more SharePoint databases from an availability group in SQL Server.

## SYNTAX

### Default
```
Remove-SPDatabaseFromAvailabilityGroup [-AGName] <String> [-AssignmentCollection <SPAssignmentCollection>]
 -DatabaseName <String> [-Force] [-KeepSecondaryData] [<CommonParameters>]
```

### AllDatabases
```
Remove-SPDatabaseFromAvailabilityGroup [-AGName] <String> [-AssignmentCollection <SPAssignmentCollection>]
 [-Force] [-KeepSecondaryData] [-ProcessAllDatabases] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [https://msdn.microsoft.com/library/dd878348(VS.85).aspx](https://msdn.microsoft.com/library/dd878348(VS.85).aspx).

## EXAMPLES

### EXAMPLE
```powershell
Remove-SPDatabaseFromAvailabilityGroup -AGName MyAvailabilityGroup -DatabaseName WSS_Content
```

This example removes the availability group named "MyAvailabilityGroup" from the WSS_Content database.

## PARAMETERS

### -AGName

> Applicable: SharePoint Server Subscription Edition

The name of the availability group from which the databases are being removed.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -DatabaseName

> Applicable: SharePoint Server Subscription Edition

The name of the database to be removed from the availability group.

NOTE: This parameter should not be used in conjunction with the ProcessAllDatabases parameter.

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

> Applicable: SharePoint Server Subscription Edition

Forces a remove from the group.

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

### -KeepSecondaryData

> Applicable: SharePoint Server Subscription Edition

Specifies that copies of the databases on the replicas in the availability group will not be deleted. Otherwise, those database copies will be dropped.

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

### -ProcessAllDatabases

> Applicable: SharePoint Server Subscription Edition

Removes all databases from the current SharePoint farm into the availability group.

```yaml
Type: SwitchParameter
Parameter Sets: AllDatabases
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
