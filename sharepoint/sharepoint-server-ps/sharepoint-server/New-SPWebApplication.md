---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/new-spwebapplication
applicable: SharePoint Server Subscription Edition
title: New-SPWebApplication
schema: 2.0.0
---

# New-SPWebApplication

## SYNOPSIS
Creates a new Web application within the local farm.


## SYNTAX

```
New-SPWebApplication -Name <String> -ApplicationPool <String>
 [-ApplicationPoolAccount <SPProcessAccountPipeBind>]
 [-ServiceApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] [-SecureSocketsLayer]
 [-HostHeader <String>] [-Certificate <SPServerCertificatePipeBind>] [-UseServerNameIndication]
 [-AllowLegacyEncryption] [-Port <UInt32>] [-AllowAnonymousAccess] [-Path <String>] [-Url <String>]
 [-AuthenticationMethod <String>] [-AuthenticationProvider <SPAuthenticationProviderPipeBind[]>]
 [-AdditionalClaimProvider <SPClaimProviderPipeBind[]>] [-SignInRedirectURL <String>]
 [-SignInRedirectProvider <SPTrustedIdentityTokenIssuerPipeBind>]
 [-UserSettingsProvider <SPUserSettingsProviderPipeBind>] [-DatabaseCredentials <PSCredential>]
 [-DatabaseServer <String>] [-DatabaseName <String>] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Creates a new Web application specified by the Name parameter.
The user specified by the DatabaseCredentials parameter must be a member of the dbcreator fixed server role on the database server.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://docs.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).


## EXAMPLES

### ------------------EXAMPLE 1-----------------------
```powershell
New-SPWebApplication -Name "Contoso Internet Site" -Port 80 -HostHeader sharepoint.contoso.com -URL "https://www.contoso.com" -ApplicationPool "ContosoAppPool" -ApplicationPoolAccount (Get-SPManagedAccount "DOMAIN\jdoe")
```

This example creates a new Web application by using an internal host header of sharepoint.contoso.com and a public URL of https://www.contoso.com.

### ------------------EXAMPLE 2-----------------------
```powershell
New-SPWebApplication -Name "Contoso Internet Site" -Port 443 -SecureSocketsLayer -HostHeader sharepoint.contoso.com -URL "https://www.contoso.com:443" -ApplicationPool "ContosoAppPool" -ApplicationPoolAccount (Get-SPManagedAccount "DOMAIN\wa")
```

This example creates a new SSL enabled Web application by using an internal host header of sharepoint.contoso.com and a public URL of https://www.contoso.com.

### ------------------EXAMPLE 3-----------------------
```powershell
$ap = New-SPAuthenticationProvider
New-SPWebApplication -Name "Contoso Internet Site" -URL "https://www.contoso.com"  -Port 443 
-ApplicationPool "ContosoAppPool" 
-ApplicationPoolAccount (Get-SPManagedAccount "DOMAIN\wa") 
-AuthenticationProvider $ap -SecureSocketsLayer
```

Creates a Windows Claims web application at the URL https://www.contoso.com using the domain account domain\wa.

## PARAMETERS

### -AdditionalClaimProvider
Adds a specific claim provider to the defined Web application.

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
Allows anonymous access to the Web application.

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

### -ApplicationPool
Specifies the name of an application pool to use; for example, SharePoint - 1213.
If an application pool with the name provided does not exist, the ApplicationPoolAccount parameter must be provided and a new application pool will be created.
If no value is specified, the default application pool will be used.

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

### -ApplicationPoolAccount
Specifies the user account that this application pool will run as.
Use the `Get-SPIisWebServicApplicationPool` cmdlet to use a system account.

```yaml
Type: SPProcessAccountPipeBind
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
If no value is specified, the default NTLM is applied.

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
Specifies the authentication provider or providers that apply to a Web application.

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
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCredentials
Specifies the Windows PowerShell Credential object for the database user account.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Specifies the name of the initial content database for the new Web application.

The type must be a valid database name; for example, ContentDB1.
If no value is specified, a value in the format WSS_Content_\<GUID\> is auto-generated.

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

### -DatabaseServer
Specifies the database server name.
The type must be a valid database server name, in the form SQL1; where named instances are used, the format can appear as server\server.
The default SQL server instance is used if a value is not provided.

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

### -HostHeader
Specifies the host header binding for this IIS web site.
A host header binding allows multiple IIS web sites to share the same port number.
Web requests sent to a shared port number are routed to the correct IIS web site based on the value of the HTTP host header sent by the client.

If no host header binding is specified, then all web requests sent to this port number will be routed to this IIS web site unless another IIS web site has a host header binding that matches the HTTP host header sent by the client.

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

### -Name
Specifies the name of the new Web application.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path
Specifies the physical directory for the new Web application in the virtual directories folder.
The type is a valid path, in the form C:\Inetpub\wwwroot\MyWebApplication.
If no value is specified, the value %wwwroot%\wss\VirtualDirectories\\\<portnumber\> is applied.

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
Specifies the port on which this Web application can be accessed.
This can be any valid port number.
If no port is specified, a nonconflicting port number is automatically generated.

If you specify a port number that has already been assigned, IIS does not start the new site until you change either the port number of the new site or the port number of the old site.

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
If you choose to use SSL, you must import a server certificate to SharePoint and assign it to the IIS web site for this web application.
Until this is done, the Web application will be inaccessible from this IIS Web site.

The default value is False.

If this parameter is omitted or set to False, this Web application will use HTTP for the specified port.

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

### -ServiceApplicationProxyGroup
Specifies a custom service application proxy group for the Web application to use.
The Web application will use the proxies in this proxy group to connect to service applications.
If this parameter is not specified, the default proxy group for the farm is used.

```yaml
Type: SPServiceApplicationProxyGroupPipeBind
Parameter Sets: (All)
Aliases: ProxyGroup
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
Specifies the load-balanced URL for the Web application.

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

### -UserSettingsProvider
Provides access to external user settings provider.

```yaml
Type: SPUserSettingsProviderPipeBind
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
