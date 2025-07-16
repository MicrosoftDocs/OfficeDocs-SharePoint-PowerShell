---
external help file: Microsoft.SharePoint.PowerShell.SSOUpgrade-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spsecurestoreserviceapplication
applicable: SharePoint Server Subscription Edition
title: Set-SPSecureStoreServiceApplication
schema: 2.0.0
---

# Set-SPSecureStoreServiceApplication

## SYNOPSIS
Sets properties of a Secure Store Service application in the farm.

## SYNTAX

```
Set-SPSecureStoreServiceApplication -Identity <SPServiceApplicationPipeBind>
 [-ApplicationPool <SPIisWebServiceApplicationPool>] [-AssignmentCollection <SPAssignmentCollection>]
 [-AuditingEnabled] [-AuditlogMaxSize <Int32>] [-Confirm] [-DatabaseCredentials <PSCredential>]
 [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>]
 [-DatabaseUsername <String>] [-FailoverDatabaseServer <String>] [-Sharing] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPSecureStoreServiceApplication` cmdlet sets properties of a Secure Store Service application in the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Set-SPSecureStoreServiceApplication -Identity $contosoServApp -AuditlogMaxSize 40
```

This example sets the maximum size of the audit log to 40 days for the given service application.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the service application to update.

```yaml
Type: SPServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ApplicationPool

> Applicable: SharePoint Server Subscription Edition

Specifies the existing IIS application pool to run the Web service in for the new service application.

```yaml
Type: SPIisWebServiceApplicationPool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -AuditingEnabled

> Applicable: SharePoint Server Subscription Edition

Turns on auditing for the Secure Store Service.

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

### -AuditlogMaxSize

> Applicable: SharePoint Server Subscription Edition

Specifies the number of days to retain the audit log.

The type must be a valid integer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DatabaseCredentials

> Applicable: SharePoint Server Subscription Edition

Specifies the PSCredential object that contains the user name and password to be used for database SQL authentication.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the Secure Store service database.

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

### -DatabasePassword

> Applicable: SharePoint Server Subscription Edition

Specifies the password for the user specified in DatabaseUserName.
Use this parameter only if SQL authentication is used to access the metadata service application database.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseServer

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the host server for the database specified in DatabaseName.

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

### -DatabaseUsername

> Applicable: SharePoint Server Subscription Edition

Specifies the user name to use for connecting to the database for the Secure Store service application.
Use this parameter only if SQL authentication is used to access the service application database.

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

### -FailoverDatabaseServer

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the host server for the failover database server.

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

### -Sharing

> Applicable: SharePoint Server Subscription Edition

Specifies that the Secure Store Service application is published and shared across the farm.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
