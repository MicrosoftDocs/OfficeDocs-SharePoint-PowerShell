---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/set-spbusinessdatacatalogserviceapplication
applicable: SharePoint Server Subscription Edition
title: Set-SPBusinessDataCatalogServiceApplication
schema: 2.0.0
---

# Set-SPBusinessDataCatalogServiceApplication

## SYNOPSIS
Sets global properties for a Business Data Connectivity service application in the farm.

## SYNTAX

```
Set-SPBusinessDataCatalogServiceApplication [-ApplicationPool <SPIisWebServiceApplicationPool>]
 [-DatabaseCredentials <PSCredential>] [-DatabaseName <String>] [-DatabasePassword <SecureString>]
 [-DatabaseServer <String>] [-DatabaseUsername <String>] [-FailoverDatabaseServer <String>]
 -Identity <SPServiceApplicationPipeBind> [-Name <String>] [-Sharing] [-Confirm] [-WhatIf]
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPBusinessDataCatalogServiceApplication` cmdlet sets global properties for a Business Data Connectivity service application in the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$sa = Get-SPServiceApplication | ?{$_.TypeName -eq 'Business Data Connectivity Service Application'}
Set-SPBusinessDataCatalogServiceApplication -Identity $sa -FailoverDatabaseServer "CONTOSO\Backup"
```

This example sets the failover database server to CONTOSO\Backup for the given service application.

## PARAMETERS

### -ApplicationPool

> Applicable: SharePoint Server Subscription Edition

Specifies the IIS application pool to use for the new Business Data Connectivity service application.

```yaml
Type: SPIisWebServiceApplicationPool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseCredentials

> Applicable: SharePoint Server Subscription Edition

Specifies the PSCredential object that contains the user name and password to be used for database SQL Server Authentication.

The type must be a valid PSCredential object.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the Business Data Connectivity database.

The type must be a valid name of a SQL Server database; for example, UsageLogDB1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabasePassword

> Applicable: SharePoint Server Subscription Edition

Specifies the password for the user specified in DatabaseUserName.
Use this parameter only if SQL Server Authentication is used to access the Business Data Connectivity database.

The type must be a valid password.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseServer

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the Business Data Connectivity database.

The type must be a valid name of a SQL Server database; for example, UsageLogDB1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseUsername

> Applicable: SharePoint Server Subscription Edition

Specifies the user name to use for connecting to the catalog database.
Use this parameter only if SQL Server Authentication is used to access the Business Data Connectivity database.

The type must be a valid user name; for example, UserName1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FailoverDatabaseServer

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the host server for the failover database server.

The type must be a valid SQL Server host name; for example, SQLServerHost1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the Business Data Connectivity service application associated with the new proxy.

```yaml
Type: SPServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies a display name for the new Business Data Connectivity service application proxy.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sharing

> Applicable: SharePoint Server Subscription Edition

Specifies that the Business Data Connectivity service application is published and shared across the farm.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

{{Fill AssignmentCollection Description}}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
