---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/set-spcontentdatabase
applicable: SharePoint Server Subscription Edition
title: Set-SPContentDatabase
schema: 2.0.0
---

# Set-SPContentDatabase

## SYNOPSIS
Sets global properties of a SharePoint content database.

## SYNTAX

```
Set-SPContentDatabase [-Identity] <SPContentDatabasePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-MaxSiteCount <Int32>] [-Status <SPObjectStatus>] [-WarningSiteCount <Int32>] [-WhatIf]
 [-DatabaseFailoverServer <String>] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPContentDatabase` cmdlet sets global properties of a SharePoint content database.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Get-SPContentDatabase https://contoso.com | Set-SPContentDatabase -MaxSiteCount 1
```

This example sets the MaxSiteCount for the content database that contains contoso.com to 1.

### EXAMPLE 2
```powershell
Get-SPContentDatabase -WebApplication https://sitename | Set-SPContentDatabase -WarningSiteCount $null
```

This example clears the WarningSiteCount for all databases in the sitename Web application.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the content database to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint content database (for example, SPContentDB1); or an instance of a valid SPContentDatabase object.

```yaml
Type: SPContentDatabasePipeBind
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

### -MaxSiteCount

> Applicable: SharePoint Server Subscription Edition

Specifies the maximum number of site collections that this database can host.

The type must be a positive integer.
Set to $null to clear this value.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Status

> Applicable: SharePoint Server Subscription Edition

Specifies the status of the SQL Server database.
Set this parameter to Online to make the database available to host new sites.
Set this parameter to Disabled to make the database unavailable to host new sites.

The type must be either of the following: Online or Disabled

```yaml
Type: SPObjectStatus
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WarningSiteCount

> Applicable: SharePoint Server Subscription Edition

Specifies the number of site collections that can be created before a warning event is generated and the owner of the site collection is notified.

The type must be a positive integer.
Set to $null to clear this value.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -DatabaseFailoverServer

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the mirror server for failover.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
