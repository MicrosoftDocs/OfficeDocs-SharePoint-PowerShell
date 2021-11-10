---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/set-spcentraladministration
applicable: SharePoint Server Subscription Edition
title: Set-SPCentralAdministration
schema: 2.0.0
---

# Set-SPCentralAdministration

## SYNOPSIS
Sets the IIS web site binding for the SharePoint Central Administration site.


## SYNTAX

```
Set-SPCentralAdministration -Port <Int32> [-SecureSocketsLayer] [-HostHeader <String>]
 [-Certificate <SPServerCertificatePipeBind>] [-UseServerNameIndication] [-AllowLegacyEncryption]
 [-Url <String>] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPCentralAdministration` cmdlet sets the IIS web site binding for the SharePoint Central Administration site.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [https://go.microsoft.com/fwlink/p/?LinkId=251831](https://go.microsoft.com/fwlink/p/?LinkId=251831).


## EXAMPLES

### ------------------EXAMPLE------------------
```powershell
Set-SPCentralAdministration -Port 8282
```

This example sets the port for the Central Administration web application on the local farm to 8282.


## PARAMETERS

### -AllowLegacyEncryption
Specifies that older SSL and TLS protocol versions and cipher suites are allowed to be used with this IIS web site.
Legacy encryption is weaker than modern encryption and is not recommended.

This feature requires Windows Server 2022 or higher.
This feature is not available when SharePoint is deployed with earlier versions of Windows Server.

This parameter is only valid when used with the SecureSocketsLayer parameter.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection
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
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Certificate
Specifies the certificate that will be used for the Secure Sockets Layer (SSL) binding of this IIS web site.
This parameter is only valid when used with the SecureSocketsLayer parameter.

```yaml
Type: SPServerCertificatePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostHeader
The host header of the Central Administration IIS web site.

If this parameter is omitted, there will be no host header binding and the URL of the Central Administration site will be based on the name of this server.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
Specifies the administration port for the Central Administration site.

The type must be a valid port number; for example, 8080.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecureSocketsLayer
Enables Secure Sockets Layer (SSL) encryption for the Central Administration IIS web site.
If you choose to use SSL, you must import a server certificate to SharePoint and assign it to the Central Administration IIS web site for this web application.
The Central Administration web application won't be accessible until you do this.

The default value is False.

If this parameter is omitted or set to False, the Central Administration site will use HTTP for the specified port.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Url
Specifies the load-balanced URL for Central Administration.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseServerNameIndication
Specifies that the Secure Sockets Layer (SSL) binding of this IIS web site should use Server Name Indication (SNI).
Server Name Indication allows multiple IIS web sites with unique host headers and unique server certificates to share the same SSL port.
If Server Name Indication isn't used, all IIS web sites sharing the same SSL port must share the same server certificate.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

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
Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: `get-help about_commonparameters`

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
