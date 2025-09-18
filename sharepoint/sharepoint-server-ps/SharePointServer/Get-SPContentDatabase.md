---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/get-spcontentdatabase
applicable: SharePoint Server Subscription Edition
title: Get-SPContentDatabase
schema: 2.0.0
---

# Get-SPContentDatabase

## SYNOPSIS

Returns one or more content databases.


## SYNTAX

### DefaultSet
```
Get-SPContentDatabase [[-Identity] <SPContentDatabasePipeBind>]
 [-AssignmentCollection <SPAssignmentCollection>] [-NoStatusFilter] [<CommonParameters>]
```

### ContentDatabasesOfSite
```
Get-SPContentDatabase -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [<CommonParameters>]
```

### AllContentDatabasesInWebApplication
```
Get-SPContentDatabase -WebApplication <SPWebApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-NoStatusFilter] [<CommonParameters>]
```
### ContentDatabasesSinceLastProfileSync
```
Get-SPContentDatabase -DaysSinceLastProfileSync <Int32> [-NoStatusFilter]
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

### Unattached
```
Get-SPContentDatabase [-AssignmentCollection <SPAssignmentCollection>] [-ConnectAsUnattachedDatabase]
 [-DatabaseCredentials <PSCredential>] -DatabaseName <String> -DatabaseServer <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The Get-SPContentDatabase cmdlet returns the specified content databases.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Get-SPContentDatabase -WebApplication https://webAppUrl
```

This example returns all content databases used by the sitename Web application.

### EXAMPLE 2
```powershell
Get-SPContentDatabase -Site https://siteUrl
```

This example returns the content database that contains the site collection at https://siteUrl.

### EXAMPLE 3
```powershell
PS C:\>Get-SPContentDatabase -DaysSinceLastProfileSync 7
```
This example returns all content databases that were last synchronized with the User Profile service 7 or more days ago. Content databases that were last synchronized with the User Profile service less than 7 days ago would not be returned.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies a specific content database to get.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint content database (for example, SPContentDB1); or an instance of a valid SPContentDatabase object.

```yaml
Type: SPContentDatabasePipeBind
Parameter Sets: DefaultSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Site

> Applicable: SharePoint Server Subscription Edition

Returns the content database for the specified site collection.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form https://server_name; or an instance of a valid SPSite object.

```yaml
Type: SPSitePipeBind
Parameter Sets: ContentDatabasesOfSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

Returns the content databases for the specified Web application.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid SPWebApplication object.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: AllContentDatabasesInWebApplication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -ConnectAsUnattachedDatabase

> Applicable: SharePoint Server Subscription Edition

Specifies that only unattached databases in the farm are returned.

```yaml
Type: SwitchParameter
Parameter Sets: Unattached
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseCredentials

> Applicable: SharePoint Server Subscription Edition

Specifies the PSCredential object that contains the user name and password to be used for database SQL Server Authentication.

The type must be a valid PSCredential object.

```yaml
Type: PSCredential
Parameter Sets: Unattached
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the database in the farm.

```yaml
Type: String
Parameter Sets: Unattached
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseServer

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the database server in the farm.

```yaml
Type: String
Parameter Sets: Unattached
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysSinceLastProfileSync
Specifies the minimum number of days since the User Profile service last synchronized the content database.

```yaml
Type: Int32
Parameter Sets: ContentDatabasesSinceLastProfileSync
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoStatusFilter

> Applicable: SharePoint Server Subscription Edition

Specifies whether a status filter is turned on.

The valid values are True or False. The default value is False.

```yaml
Type: SwitchParameter
Parameter Sets: DefaultSet, AllContentDatabasesInWebApplication
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
