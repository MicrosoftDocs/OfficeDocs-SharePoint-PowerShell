---
external help file: microsoft.office.access.server.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/set-spaccessservicesdatabaseserver
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: Set-SPAccessServicesDatabaseServer
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Set-SPAccessServicesDatabaseServer

## SYNOPSIS
Sets parameters associated with a database server hosting Access Services databases.

## SYNTAX

### SetAvailableForCreateParameterSet
```
Set-SPAccessServicesDatabaseServer [-ServiceContext] <SPServiceContextPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] -AvailableForCreate <Boolean> [-Confirm]
 -DatabaseServer <AccessServicesDatabaseServerPipeBind>
 -DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind> [-Exclusive <Boolean>] [-WhatIf]
 [<CommonParameters>]
```

### SetCredentialsParameterSet
```
Set-SPAccessServicesDatabaseServer [-ServiceContext] <SPServiceContextPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 -DatabaseServer <AccessServicesDatabaseServerPipeBind> [-DatabaseServerCredentials <PSCredential>]
 -DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind> [-DatabaseServerName <String>] [-WhatIf]
 [<CommonParameters>]
```

### SetEncryptParameterSet
```
Set-SPAccessServicesDatabaseServer [-ServiceContext] <SPServiceContextPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 -DatabaseServer <AccessServicesDatabaseServerPipeBind>
 -DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind> -Encrypt <Boolean>
 -TrustServerCertificate <Boolean> [-WhatIf] [<CommonParameters>]
```

### SetFailoverParameterSet
```
Set-SPAccessServicesDatabaseServer [-ServiceContext] <SPServiceContextPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 -DatabaseServer <AccessServicesDatabaseServerPipeBind>
 -DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind> -Failover <Boolean> [-WhatIf]
 [<CommonParameters>]
```

### SetSecondaryDatabaseServerNameParameterSet
```
Set-SPAccessServicesDatabaseServer [-ServiceContext] <SPServiceContextPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 -DatabaseServer <AccessServicesDatabaseServerPipeBind>
 -DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind> [-SecondaryDatabaseServerName <String>]
 [-WhatIf] [<CommonParameters>]
```

### SetUserDomainParameterSet
```
Set-SPAccessServicesDatabaseServer [-ServiceContext] <SPServiceContextPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 -DatabaseServer <AccessServicesDatabaseServerPipeBind>
 -DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind> -UserDomain <String> [-WhatIf]
 [<CommonParameters>]
```

### SetServerStateParameterSet
```
Set-SPAccessServicesDatabaseServer [-ServiceContext] <SPServiceContextPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 -DatabaseServer <AccessServicesDatabaseServerPipeBind>
 -DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind> -State <DatabaseServerStates>
 -StateOwner <ServerStateOwner> [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Sets parameters associated with a database server hosting Access Services databases allowing you to control database creation, credentials, and failover database servers.

## EXAMPLES

### EXAMPLE
```
$site = (Get-SPWebApplication -IncludeCentralAdministration | ?{$_.IsAdministrationWebApplication -eq $true}).Sites[0]
$dbsvr = (Get-SPAccessServicesDatabaseServer -ServiceContext $site -DatabaseServerGroup DEFAULT)[0]
Set-SPAccessServicesDatabaseServer -ServiceContext $site -DatabaseServerGroup DEFAULT -DatabaseServer $dbsvr -Exclusive $true -AvailableForCreate $false
```
Sets the first database in the database server group named DEFAULT to exclusive mode and disallowing creation of new Access Services database on the selected database server.

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -AvailableForCreate

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Indicates whether new Access Services databases can be created on the specified SQL Server.

```yaml
Type: Boolean
Parameter Sets: SetAvailableForCreateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -DatabaseServer

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the SQL Server hosting Access Services databases.

```yaml
Type: AccessServicesDatabaseServerPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseServerCredentials

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the Credential object for the database user. Use this parameter if you use SQL Server Authentication. If no database credentials are provided, Windows authentication is used.

```yaml
Type: PSCredential
Parameter Sets: SetCredentialsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseServerGroup

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

The name of the Access Services database server group containing the SQL Server object to set.

```yaml
Type: AccessServicesDatabaseServerGroupPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseServerName

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the database server hosting Access Services databases.

```yaml
Type: String
Parameter Sets: SetCredentialsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Encrypt

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Encrypts the database server connection.

```yaml
Type: Boolean
Parameter Sets: SetEncryptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Exclusive

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Sets the database server to exclusive mode. No further Access Services databases are allowed to be created on the database server.

```yaml
Type: Boolean
Parameter Sets: SetAvailableForCreateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Failover

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Enables or disables failover for the Access Services database server.

```yaml
Type: Boolean
Parameter Sets: SetFailoverParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecondaryDatabaseServerName

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the failover database server name.

```yaml
Type: String
Parameter Sets: SetSecondaryDatabaseServerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceContext

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the service context which is in the form of an instance of an SPServiceContext object, an SPSiteAdministration object identifier, or a SPSite object. An example of a service context value is an identifier from the ID field, a string identifier, a URI, or a string representation of a GUID.

```yaml
Type: SPServiceContextPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TrustServerCertificate

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Sets a value that indicates whether the channel will be encrypted while bypassing walking the certificate chain to validate trust.

```yaml
Type: Boolean
Parameter Sets: SetEncryptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDomain

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Sets the user domain for the specified database server.

```yaml
Type: String
Parameter Sets: SetUserDomainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -State

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Sets the database server state.
Valid values:

- Active

- Locked

- Reserved

```yaml
Type: DatabaseServerStates
Parameter Sets: SetServerStateParameterSet
Aliases:
Accepted values: Active, Locked, Reserved

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StateOwner

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Sets the state owner.

Valid values:

- NoOwner

- TenantMove

```yaml
Type: ServerStateOwner
Parameter Sets: SetServerStateParameterSet
Aliases:
Accepted values: NoOwner, TenantMove

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind
Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
