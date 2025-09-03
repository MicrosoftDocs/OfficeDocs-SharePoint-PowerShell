---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spcentraladministration
applicable: SharePoint Server Subscription Edition
title: New-SPCentralAdministration
schema: 2.0.0
ms.date: 08/26/2025
---

# New-SPCentralAdministration

## SYNOPSIS

Creates a new SharePoint Central Administration Web application.


## SYNTAX

### SetIisWebSiteBinding
```
New-SPCentralAdministration [-Port] <Int32> [[-WindowsAuthProvider] <String>] [-SecureSocketsLayer]
 [[-HostHeader] <String>] [-Certificate <SPServerCertificatePipeBind>] [-UseServerNameIndication]
 [-AllowLegacyEncryption] [-Url <String>] [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

### SetAuthProvider
```
New-SPCentralAdministration [[-WindowsAuthProvider] <String>] [-AssignmentCollection <SPAssignmentCollection>]
 [<CommonParameters>]
```

## DESCRIPTION
The New-SPCentralAdministration cmdlet creates a new Central Administration Web application and starts the central administration service on the local computer.
Central Administration is available only on computers where this service runs.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
New-SPCentralAdministration -WindowsAuthProvider NTLM -Port 8080
```

This example creates the Central Administration site at port 8080 on the local farm using NTLM authentication.

### EXAMPLE 2
```powershell
New-SPCentralAdministration -WindowsAuthProvider Kerberos -Port 443 -SecureSocketsLayer -HostHeader centraladmin.example.com
```

This example creates the Central Administration site using SSL on port 443 with the host header centraladmin.example.com and Kerberos authentication.

## PARAMETERS

### -AllowLegacyEncryption

> Applicable: SharePoint Server Subscription Edition

Specifies that older SSL and TLS protocol versions and cipher suites are allowed to be used with this IIS website.
Legacy encryption is weaker than modern encryption and is not recommended.

This feature requires Windows Server 2022 or higher.
This feature is not available when SharePoint is deployed with earlier versions of Windows Server.

This parameter is only valid when used with the SecureSocketsLayer parameter.

```yaml
Type: SwitchParameter
Parameter Sets: SetIisWebSiteBinding
Aliases:

Required: False
Position: Named
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

### -Certificate

> Applicable: SharePoint Server Subscription Edition

Specifies the certificate that will be used for the Secure Sockets Layer (SSL) binding of this IIS website.
This parameter is only valid when used with the SecureSocketsLayer parameter.

```yaml
Type: SPServerCertificatePipeBind
Parameter Sets: SetIisWebSiteBinding
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -HostHeader

> Applicable: SharePoint Server Subscription Edition

Specifies the host header of the Central Administration IIS website.

If this parameter is omitted there will be no host header binding and the URL of the Central Administration site will be based on the name of this server.

```yaml
Type: String
Parameter Sets: SetIisWebSiteBinding
Aliases: Host

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Port

> Applicable: SharePoint Server Subscription Edition

Specifies the port number for Central Administration.
If no port is specified, a nonconflicting port number is auto-generated.

The type must be a valid port number.

If you specify a port number that has already been assigned, IIS does not start the new site until you change either the port number of the new site or the port number of the old site.

```yaml
Type: Int32
Parameter Sets: SetIisWebSiteBinding
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SecureSocketsLayer

> Applicable: SharePoint Server Subscription Edition

Enables Secure Sockets Layer (SSL) encryption for the Central Administration IIS website.
If you choose to use SSL, you must import a server certificate to SharePoint and assign it to the Central Administration IIS website.
The Central Administration web application won't be accessible until you do this.

The default value is False.

If this parameter is omitted or set to False the Central Administration site will use HTTP for the specified port.

```yaml
Type: SwitchParameter
Parameter Sets: SetIisWebSiteBinding
Aliases:

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Url

> Applicable: SharePoint Server Subscription Edition

Specifies the load-balanced URL for Central Administration.

```yaml
Type: String
Parameter Sets: SetIisWebSiteBinding
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -UseServerNameIndication

> Applicable: SharePoint Server Subscription Edition

Specifies that the Secure Sockets Layer (SSL) binding of this IIS website should use Server Name Indication (SNI).
Server Name Indication allows multiple IIS websites with unique host headers and unique server certificates to share the same SSL port.
If Server Name Indication isn't used, all IIS websites sharing the same SSL port must share the same server certificate.

```yaml
Type: SwitchParameter
Parameter Sets: SetIisWebSiteBinding
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsAuthProvider

> Applicable: SharePoint Server Subscription Edition

Specifies the authentication provider for this web application.
If no authentication provider is specified, the default value NTLM is used.

The type must be one of two values: Kerberos or NTLM.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters] (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
