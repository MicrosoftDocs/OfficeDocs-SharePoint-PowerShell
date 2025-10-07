---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/set-spservicehostconfig
applicable: SharePoint Server Subscription Edition
title: Set-SPServiceHostConfig
schema: 2.0.0
---

# Set-SPServiceHostConfig

## SYNOPSIS
Configures one or more common settings for all web services.

## SYNTAX

### SslCertificateImport (Default)
```
Set-SPServiceHostConfig [-Identity] <SPIisWebServiceSettings> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-NetTcpPort <Int32>] [-ImportSslCertificate <X509Certificate2>] [-AllowLegacyEncryption] [-NoWait]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SslCertificateReference
```
Set-SPServiceHostConfig [-Identity] <SPIisWebServiceSettings> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-NetTcpPort <Int32>] -SslCertificateThumbprint <String> [-SslCertificateStoreName <String>]
 [-AllowLegacyEncryption] [-NoWait] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SslCertificateReferenceRunInProcess
```
Set-SPServiceHostConfig [-Identity] <SPIisWebServiceSettings> -SslCertificateThumbprint <String>
 [-SslCertificateStoreName <String>] [-RunInProcess] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The `Set- SPServiceHostConfig` cmdlet configures one or more common settings for all web services.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Set-SPServiceHostConfig -Port 12345
```

This example sets the HTTP port for the web services.

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
Parameter Sets: SslCertificateImport, SslCertificateReference
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

### -HttpPort

> Applicable: SharePoint Server Subscription Edition

Specifies the new port for the web service.

```yaml
Type: Int32
Parameter Sets: SslCertificateImport, SslCertificateReference
Aliases: Port

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpsPort

> Applicable: SharePoint Server Subscription Edition

Specifies the new secure port for the web service.

```yaml
Type: Int32
Parameter Sets: SslCertificateImport, SslCertificateReference
Aliases: SecurePort

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the identity of the web service application to configure.

```yaml
Type: SPIisWebServiceSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ImportSslCertificate

> Applicable: SharePoint Server Subscription Edition

Specifies the SSL Certificate to use for secure protocols.

```yaml
Type: X509Certificate2
Parameter Sets: SslCertificateImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetTcpPort

> Applicable: SharePoint Server Subscription Edition

Sets the TCP port for the web service.

```yaml
Type: Int32
Parameter Sets: SslCertificateImport, SslCertificateReference
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait

> Applicable: SharePoint Server Subscription Edition

For more information, see TechNet.

```yaml
Type: SwitchParameter
Parameter Sets: SslCertificateImport, SslCertificateReference
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunInProcess

> Applicable: SharePoint Server Subscription Edition

Specifies to update the web service application configuration using the current process instead of a SharePoint Timer job.

```yaml
Type: SwitchParameter
Parameter Sets: SslCertificateReferenceRunInProcess
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCertificateStoreName

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the certificate store containing the SSL certificate to retrieve for secure protocols.

```yaml
Type: String
Parameter Sets: SslCertificateReference, SslCertificateReferenceRunInProcess
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCertificateThumbprint

> Applicable: SharePoint Server Subscription Edition

Specifies the thumbprint of the SSL certificate to retrieve for secure protocols.

```yaml
Type: String
Parameter Sets: SslCertificateReference, SslCertificateReferenceRunInProcess
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before executing the command.
For more information, type the following command: \`get-help about_commonparameters\`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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
