---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/set-spwebapplication
applicable: SharePoint Server Subscription Edition
title: Set-SPWebApplication
schema: 2.0.0
---

# Set-SPWebApplication

## SYNOPSIS
Configures the specified Web application.


## SYNTAX

### UpdateGeneralSettings (Default)
```
Set-SPWebApplication [-Identity] <SPWebApplicationPipeBind> [-DefaultTimeZone <Int32>]
 [-DefaultQuotaTemplate <String>] [-ServiceApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>]
 [-NotProvisionGlobally] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UpdateClaimSettings
```
Set-SPWebApplication [-Identity] <SPWebApplicationPipeBind> -Zone <SPUrlZone>
 [-AuthenticationProvider <SPAuthenticationProviderPipeBind[]>]
 [-AdditionalClaimProvider <SPClaimProviderPipeBind[]>] [-SignInRedirectURL <String>]
 [-SignInRedirectProvider <SPTrustedIdentityTokenIssuerPipeBind>] [-AuthenticationMethod <String>] [-Force]
 [-NotProvisionGlobally] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UpdateIISSettings
```
Set-SPWebApplication [-Identity] <SPWebApplicationPipeBind> -Zone <SPUrlZone> [-SecureSocketsLayer]
 [-HostHeader <String>] [-Certificate <SPServerCertificatePipeBind>] [-UseServerNameIndication]
 [-AllowLegacyEncryption] -Port <Int32> [-Url <String>] [-NotProvisionGlobally]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateMailSettings
```
Set-SPWebApplication [-Identity] <SPWebApplicationPipeBind> -SMTPServer <String> [-SMTPServerPort <Int32>]
 [-OutgoingEmailAddress <String>] [-ReplyToEmailAddress <String>] [-SMTPCredentials <PSCredential>]
 [-DisableSMTPEncryption] [-Certificate <SPServerCertificatePipeBind>] [-NotProvisionGlobally]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://docs.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The `Set-SPWebApplication` cmdlet configures the Web application specified by the Identity parameter.
For any settings that are zone-specific (for the Zone parameter set), the zone to configure must be provided.
The provided zone must already exist.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://docs.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
$credentials = Get-Credential
Set-SPWebApplication -Identity http://servername -SMTPServer mail.example.com -SMTPServerPort 587 -OutgoingEmailAddress user@example.com -ReplyToAddress replyto@example.com -SMTPCredentials $credentials
```

This example sets the http://servername web application to use the SMTP server mail.example.com, the SMTP server port 587, the from address user@example.com, the reply-to address replyto@example.com, and the credentials stored in the $credentials object.

### EXAMPLE 2
```powershell
Set-SPWebApplication -Identity http://servername -SMTPServer mail.example.com -OutgoingEmailAddress user@example.com -ReplyToAddress replyto@example.com -SMTPCredentials $null
```

This example sets the http://servername web application to use the SMTP server mail.example.com, the default SMTP server port, the from address user@example.com, the reply-to address replyto@example.com, and to connect to the SMTP server anonymously.

## PARAMETERS

### -AdditionalClaimProvider
Adds a specific claim provider to the defined Web application.

```yaml
Type: SPClaimProviderPipeBind[]
Parameter Sets: UpdateClaimSettings
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
Parameter Sets: UpdateIISSettings
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
Use to set a Web application to classic Windows authentication.
The valid values are NTLM or Kerberos.

```yaml
Type: String
Parameter Sets: UpdateClaimSettings
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationProvider
Defines the authentication provider(s) that applies to the Web application.

```yaml
Type: SPAuthenticationProviderPipeBind[]
Parameter Sets: UpdateClaimSettings
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certificate
Specifies the certificate that will be used for the Secure Sockets Layer (SSL) binding of this IIS web site, or for authenticating to an SMTP server to send email.

When configuring the Secure Sockets Layer (SSL) binding of this IIS web site, this parameter is only valid when used with the SecureSocketsLayer parameter.
When configuring SMTP authentication, this parameter is only valid when the DisableSMTPEncryption parameter is not specified.

```yaml
Type: SPServerCertificatePipeBind
Parameter Sets: UpdateIISSettings, UpdateMailSettings
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultQuotaTemplate
Specifies the new default site quota template for this Web application.

```yaml
Type: String
Parameter Sets: UpdateGeneralSettings
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultTimeZone
Specifies the default time zone for new site collections in this Web application.

```yaml
Type: Int32
Parameter Sets: UpdateGeneralSettings
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSMTPEncryption
Specifies whether to turn on or off SMTP Encryption.

The default value is false.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateMailSettings
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Suppresses confirmation messages involved in settings for a Web application.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateClaimSettings
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: False
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
Parameter Sets: UpdateIISSettings
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
Specifies the name or URL of the Web application.

The type must be a valid name, in the form WebApplication-1212, or URL, in the form http://server_name.

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

### -NotProvisionGlobally
Skips the Web application provision process.

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

### -OutgoingEmailAddress
Specifies the new outgoing e-mail address for e-mail messages sent from this Web application.
The type must be a valid address; for example, someone@example.com.

```yaml
Type: String
Parameter Sets: UpdateMailSettings
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

If you specify a port number that has already been assigned, IIS does not start the new site until you change either the port number of the new site or the port number of the old site.

```yaml
Type: Int32
Parameter Sets: UpdateIISSettings
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplyToEmailAddress
Configures the reply e-mail address.

The type must be a valid address; for example, someone@example.com.

```yaml
Type: String
Parameter Sets: UpdateMailSettings
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
Parameter Sets: UpdateIISSettings
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
If this parameter is not specified, the farm's default proxy group is used.

```yaml
Type: SPServiceApplicationProxyGroupPipeBind
Parameter Sets: UpdateGeneralSettings
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
Parameter Sets: UpdateClaimSettings
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
Parameter Sets: UpdateClaimSettings
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SMTPCredentials
Specifies credentials to authenticate to the SMTP server.
Set the value to $null to connect to the SMTP server anonymously.
If this parameter isn't specified, the existing authentication settings will be preserved.

You must use the \`Set-SPApplicationCredentialKey\` PowerShell cmdlet to set an application credential key on each server in the farm before specifying credentials.

```yaml
Type: PSCredential
Parameter Sets: UpdateMailSettings
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SMTPServer
Specifies the new outbound SMTP server that this Web application will use.
Set to $null to clear the server setting.

```yaml
Type: String
Parameter Sets: UpdateMailSettings
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SMTPServerPort
Specifies a SMTP port value.

```yaml
Type: Int32
Parameter Sets: UpdateMailSettings
Aliases:

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
Parameter Sets: UpdateIISSettings
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
Parameter Sets: UpdateIISSettings
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
When configuring zone-specific settings, the zone to configure must be specified.
This zone must already exist.

The type must be any one of the following values: Default, Intranet, Internet, Extranet, or Custom.

```yaml
Type: SPUrlZone
Parameter Sets: UpdateClaimSettings, UpdateIISSettings
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
