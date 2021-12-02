---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/new-spwebapplicationextension
applicable: SharePoint Server Subscription Edition
title: New-SPWebApplicationExtension
schema: 2.0.0
---

# New-SPWebApplicationExtension

## SYNOPSIS
Creates a new zone instance for the Web application.


## SYNTAX

```
New-SPWebApplicationExtension [-Identity] <SPWebApplicationPipeBind> -Name <String> -Zone <SPUrlZone>
 [-Port <UInt32>] [-HostHeader <String>] [-Certificate <SPServerCertificatePipeBind>]
 [-UseServerNameIndication] [-AllowLegacyEncryption] [-Path <String>] [-Url <String>]
 [-AuthenticationMethod <String>] [-AllowAnonymousAccess] [-SecureSocketsLayer]
 [-AuthenticationProvider <SPAuthenticationProviderPipeBind[]>]
 [-AdditionalClaimProvider <SPClaimProviderPipeBind[]>] [-SignInRedirectURL <String>]
 [-SignInRedirectProvider <SPTrustedIdentityTokenIssuerPipeBind>]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The `New-SPWebApplicationExtension` cmdlet creates a new zone instance for the Web application.
This is also known as extending a Web application and allows alternate permissions to be configured for the same content that is available in the existing Web application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://docs.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).


## EXAMPLES

### ------------------EXAMPLE-----------------------
```powershell
Get-SPWebApplication http://sitename | New-SPWebApplicationExtension -Name "ExtranetSite" -SecureSocketsLayer -Zone "Extranet" -URL "https://extranet.sitename.com"
```

This example extends the given Web application at http://sitename to the Extranet zone for SSL use.


## PARAMETERS

### -AdditionalClaimProvider
Adds a specific claim provider to the defined web application.

```yaml
Type: SPClaimProviderPipeBind[]
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowAnonymousAccess
Allows anonymous access to the web application zone.

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

### -AllowLegacyEncryption
Specifies that older SSL and TLS protocol versions and cipher suites are allowed to be used with this IIS website.
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

### -AuthenticationMethod
Uses Kerberos or NTLM to specify the authentication method.

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

### -AuthenticationProvider
Specifies the authentication provider(s) that applies to a Web apllication.

```yaml
Type: SPAuthenticationProviderPipeBind[]
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certificate
Specifies the certificate that will be used for the Secure Sockets Layer (SSL) binding of this IIS website.
This parameter is only valid when used with the SecureSocketsLayer parameter.

```yaml
Type: SPServerCertificatePipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -HostHeader
Specifies the host header binding for this IIS website.
A host header binding allows multiple IIS websites to share the same port number.
Web requests sent to a shared port number are routed to the correct IIS website based on the value of the HTTP host header sent by the client.

If no host header binding is specified, then all web requests sent to this port number will be routed to this IIS website unless another IIS website has a host header binding that matches the HTTP host header sent by the client.

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

### -Identity
Specifies the Web application to extend.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of the new IIS website in the web application.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the physical directory for the new website (in the virtual directories folder).
The type is a valid path, in the form C:\Inetpub\wwwroot\MyWebApplication.

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
Specifies the application port.
Can be any valid port number.

If no port is specified, a nonconflicting port number is automatically generated.

If you specify a port number that is already assigned, IIS does not start the new site until you change either the port number of the new site or the port number of the old site.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecureSocketsLayer
Enables Secure Sockets Layer (SSL) encryption for this Web application.
If you choose to use SSL, you must import a server certificate to SharePoint and assign it to the IIS website for this web application.
Until this is done, the web application will be inaccessible from this IIS website.

The default value is False.

If this parameter is omitted or set to False, this web application will use HTTP for the specified port.

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

### -SignInRedirectProvider
Sets the sign-in redirect URL to point to the URL that is defined in the specified authentication provider.

```yaml
Type: SPTrustedIdentityTokenIssuerPipeBind
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignInRedirectURL
Specifies the sign-in redirect URL for the Web application.

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

### -Url
Specifies the load-balanced URL for the Web application zone.

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
Specifies that the Secure Sockets Layer (SSL) binding of this IIS website should use Server Name Indication (SNI).
Server Name Indication allows multiple IIS websites with unique host headers and unique server certificates to share the same SSL port.
If Server Name Indication isn't used, all IIS websites sharing the same SSL port must share the same server certificate.

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

### -Zone
Specifies one of the five zones with which the internal URL of this new extension is to be associated.
This zone cannot already be in use.

The type must be any one of the following values: Default, Intranet, Internet, Extranet, or Custom

```yaml
Type: SPUrlZone
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
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
