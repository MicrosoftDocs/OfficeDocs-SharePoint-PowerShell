---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/new-spconfigurationdatabase
applicable: SharePoint Server Subscription Edition
title: New-SPConfigurationDatabase
schema: 2.0.0
---

# New-SPConfigurationDatabase

## SYNOPSIS

Creates a new configuration database.


## SYNTAX

```
New-SPConfigurationDatabase [-DatabaseName] <String> [-DatabaseServer] <String> [[-DirectoryDomain] <String>]
 [[-DirectoryOrganizationUnit] <String>] [[-AdministrationContentDatabaseName] <String>]
 [[-DatabaseCredentials] <PSCredential>] [-FarmCredentials] <PSCredential> [-Passphrase] <SecureString>
 [-SkipRegisterAsDistributedCacheHost] [-AssignmentCollection <SPAssignmentCollection>]
 [-DatabaseFailOverServer <String>] [-LocalServerRole <SPServerRole>] [-ServerRoleOptional]
 [-DatabaseConnectionEncryption <SqlConnectionEncryptOption>] [-DatabaseServerCertificateHostName <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The New-SPConfigurationDatabase cmdlet creates a new configuration database on the specified database server.
This is the central database for a new SharePoint farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
New-SPConfigurationDatabase -DatabaseName "SharePointConfigDB1" -DatabaseServer "SQL-01" -Passphrase (ConvertTo-SecureString "MyPassword" -AsPlainText -force) -FarmCredentials (Get-Credential)
```

This example prompts the user to provide user credentials for the default Farm Administrator account.

### EXAMPLE 2
```powershell
New-SPConfigurationDatabase -DatabaseName "SharePointConfigDB1" -DatabaseServer "SQL-01" -Passphrase (ConvertTo-SecureString "MyPassword" -AsPlainText -force) -FarmCredentials (Get-Credential) -SkipRegisterAsDistributedCacheHost
```

This example prompts the user to provide user credentials for the default Farm Administrator account and skips registering the server as Distributed Cache host. Applies to SharePoint Server 2013 and SharePoint Server 2016, SharePoint Server 2019 only.

### EXAMPLE 3
```powershell
New-SPConfigurationDatabase -DatabaseName "SharePointConfigDB1" -DatabaseServer "SQL-01" -Passphrase (ConvertTo-SecureString "MyPassword" -AsPlainText -force) -FarmCredentials (Get-Credential) -LocalServerRole Custom
```

This example prompts the user to provide user credentials for the default Farm Administrator account and sets the Server Role to Custom. Applies to SharePoint Server 2016, SharePoint Server 2019 only.

## PARAMETERS

### -DatabaseName

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the new configuration database.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DatabaseServer

> Applicable: SharePoint Server Subscription Edition

Specifies the database server on which to create the configuration database.
If no value is specified, the default value is used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DirectoryDomain

> Applicable: SharePoint Server Subscription Edition

Specifies the directory domain for the new farm.
If no domain is specified, the domain in which the local computer is located is used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DirectoryOrganizationUnit

> Applicable: SharePoint Server Subscription Edition

Specifies the directory organizational unit for the new configuration database.
If no organizational unit is specified, the organizational unit in which the local computer is located is used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdministrationContentDatabaseName

> Applicable: SharePoint Server Subscription Edition

Specifies the name for the Central Administration content database for the new farm.
If no name is specified, a default name is used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DatabaseCredentials

> Applicable: SharePoint Server Subscription Edition

Specifies the Credential object for the database user.
Use this parameter if you use SQL Server Authentication.
If no database credentials are provided, Windows authentication is used.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -FarmCredentials

> Applicable: SharePoint Server Subscription Edition

Specifies credentials for the Farm Administrator account.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Passphrase

> Applicable: SharePoint Server Subscription Edition

Specifies the secure password phrase for the new farm.
This passphrase is used to join other machines to this farm.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SkipRegisterAsDistributedCacheHost

> Applicable: SharePoint Server Subscription Edition

By default all the servers in the farm are registered as a cache host (that is, DistributedCacheService is running by default).

Use this parameter to not register the server computer as a distributed cache host.
If you want to have a dedicated cache host, then use this parameter to make sure that caching service is not installed on the computer.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

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

### -DatabaseFailOverServer

> Applicable: SharePoint Server Subscription Edition

Specifies the SQL Server Database Mirror partner server for the Configuration and Central Administration database.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -LocalServerRole

> Applicable: SharePoint Server Subscription Edition

Specifies the Server Role. Valid options for all versions of SharePoint Server 2016, SharePoint Server 2019 are:
`Custom`, `SingleServerFarm`, `Application`, `WebFrontEnd`, `DistributedCache`, `Search`

With the addition of Feature Pack 1, new options include:
`ApplicationWithSearch`, `WebFrontEndWithDistributedCache `

```yaml
Type: SPServerRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerRoleOptional

> Applicable: SharePoint Server Subscription Edition

Configures the farm to not require a server role to be specified. If no server role is specified, the server defaults to the Custom role.

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

### -SiteMapDatabaseName

> Applicable: SharePoint Server Subscription Edition

Do not use. Specifies the database name of the Site Map site.

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

### -SiteMapDatabaseServer

> Applicable: SharePoint Server Subscription Edition

Do not use. Specifies the database server name of the Site Map site.

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

### -DatabaseConnectionEncryption

> Applicable: SharePoint Server Subscription Edition

Specifies whether TLS encryption is used for the connection between SharePoint and the database.
Mandatory requires that TLS encryption is used. If TLS encryption can't be successfully negotiated, the connection will fail.
Optional allows TLS encryption to be used. If the database server requires TLS encryption, then TLS encryption will be used. Otherwise, TLS encryption will not be used.
Strict requires that TLS encryption is used with TDS 8.0, which is the strongest encryption configuration. If TLS encryption with TDS 8.0 can't be successfully negotiated, the connection will fail.
Databases mounted to SharePoint before the Version 24H2 feature update was installed default to Optional encryption. If this parameter is not specified when mounting a new database to SharePoint after the Version 24H2 feature update is installed, the default is Mandatory.

```yaml
Type: SqlConnectionEncryptOption
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Mandatory
Accept pipeline input: True
Accept wildcard characters: False
```

### -DatabaseServerCertificateHostName

> Applicable: SharePoint Server Subscription Edition

Sets the host name to use when validating the server certificate for the connection.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
