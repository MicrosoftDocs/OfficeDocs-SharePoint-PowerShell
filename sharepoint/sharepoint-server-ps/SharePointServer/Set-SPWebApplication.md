---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/set-spwebapplication
applicable: SharePoint Server Subscription Edition
title: Set-SPWebApplication
schema: 2.0.0
---

# Set-SPWebApplication

## SYNOPSIS
Configures the specified web application.

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
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The `Set-SPWebApplication` cmdlet configures the web application specified by the Identity parameter.
For any settings that are zone-specific (for the Zone parameter set), the zone to configure must be provided.
The provided zone must already exist.

All IIS binding settings should be respecified when updating the binding of an IIS website via the `Set-SPWebApplication` cmdlet. This includes the URL, secure sockets layer setting, the port number, the host header, and the certificate. If a binding setting isn't respecified, it will revert to its default value.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

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

> Applicable: SharePoint Server Subscription Edition

Adds a specific claim provider to the defined web application.

```yaml
Type: SPClaimProviderPipeBind[]
Parameter Sets: UpdateClaimSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowLegacyEncryption

> Applicable: SharePoint Server Subscription Edition

Specifies that older SSL and TLS protocol versions and cipher suites are allowed to be used with this IIS website.
Legacy encryption is weaker than modern encryption and is not recommended.

This feature requires Windows Server 2022 or higher.
This feature is not available when SharePoint is deployed with earlier versions of Windows Server.

This parameter is only valid when used with the SecureSocketsLayer parameter.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateIISSettings
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

### -AuthenticationMethod

> Applicable: SharePoint Server Subscription Edition

Use to set a web application to classic Windows authentication.
The valid values are NTLM or Kerberos.

```yaml
Type: String
Parameter Sets: UpdateClaimSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationProvider

> Applicable: SharePoint Server Subscription Edition

Defines the authentication provider(s) that applies to the web application.

```yaml
Type: SPAuthenticationProviderPipeBind[]
Parameter Sets: UpdateClaimSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certificate

> Applicable: SharePoint Server Subscription Edition

Specifies the certificate that will be used for the Secure Sockets Layer (SSL) binding of this IIS website, or for authenticating to an SMTP server to send email.

When configuring the Secure Sockets Layer (SSL) binding of this IIS website, this parameter is only valid when used with the SecureSocketsLayer parameter.
When configuring SMTP authentication, this parameter is only valid when the DisableSMTPEncryption parameter is not specified.

```yaml
Type: SPServerCertificatePipeBind
Parameter Sets: UpdateIISSettings, UpdateMailSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultQuotaTemplate

> Applicable: SharePoint Server Subscription Edition

Specifies the new default site quota template for this web application.

```yaml
Type: String
Parameter Sets: UpdateGeneralSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultTimeZone

> Applicable: SharePoint Server Subscription Edition

Specifies the default time zone for new site collections in this web application.

```yaml
Type: Int32
Parameter Sets: UpdateGeneralSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSMTPEncryption

> Applicable: SharePoint Server Subscription Edition

Specifies whether to turn on or off SMTP Encryption.

The default value is false.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateMailSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

> Applicable: SharePoint Server Subscription Edition

Suppresses confirmation messages involved in settings for a web application.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateClaimSettings
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostHeader

> Applicable: SharePoint Server Subscription Edition

Specifies the host header binding for this IIS website.
A host header binding allows multiple IIS websites to share the same port number.
Web requests sent to a shared port number are routed to the correct IIS website based on the value of the HTTP host header sent by the client.

If no host header binding is specified, then all web requests sent to this port number will be routed to this IIS website unless another IIS website has a host header binding that matches the HTTP host header sent by the client.

```yaml
Type: String
Parameter Sets: UpdateIISSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the name or URL of the web application.

The type must be a valid name, in the form WebApplication-1212, or URL, in the form https://example.contoso.com.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NotProvisionGlobally

> Applicable: SharePoint Server Subscription Edition

Only provisions the web application on the local server with the changes specified by this cmdlet. Web applications on other servers in the farm will not be provisioned with these changes.

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

### -OutgoingEmailAddress

> Applicable: SharePoint Server Subscription Edition

Specifies the new outgoing e-mail address for e-mail messages sent from this web application.
The type must be a valid address; for example, someone@example.com.

```yaml
Type: String
Parameter Sets: UpdateMailSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port

> Applicable: SharePoint Server Subscription Edition

Specifies the port on which this web application can be accessed.
This can be any valid port number.

If you specify a port number that has already been assigned, IIS does not start the new site until you change either the port number of the new site or the port number of the old site.

```yaml
Type: Int32
Parameter Sets: UpdateIISSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplyToEmailAddress

> Applicable: SharePoint Server Subscription Edition

Configures the reply e-mail address.

The type must be a valid address; for example, someone@example.com.

```yaml
Type: String
Parameter Sets: UpdateMailSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecureSocketsLayer

> Applicable: SharePoint Server Subscription Edition

Enables Secure Sockets Layer (SSL) encryption for this web application.
If you choose to use SSL, you must import a server certificate to SharePoint and assign it to the IIS website for this web application.
Until this is done, the web application will be inaccessible from this IIS website.

The default value is False.

If this parameter is omitted or set to False, this web application will use HTTP for the specified port.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateIISSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceApplicationProxyGroup

> Applicable: SharePoint Server Subscription Edition

Specifies a custom service application proxy group for the web application to use.
The web application will use the proxies in this proxy group to connect to service applications.
If this parameter is not specified, the farm's default proxy group is used.

```yaml
Type: SPServiceApplicationProxyGroupPipeBind
Parameter Sets: UpdateGeneralSettings
Aliases: ProxyGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignInRedirectProvider

> Applicable: SharePoint Server Subscription Edition

Sets the sign-in redirect URL to point to the URL that is defined in the specified authentication provider.

```yaml
Type: SPTrustedIdentityTokenIssuerPipeBind
Parameter Sets: UpdateClaimSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignInRedirectURL

> Applicable: SharePoint Server Subscription Edition

Specifies the sign-in redirect URL for the web application.

```yaml
Type: String
Parameter Sets: UpdateClaimSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SMTPCredentials

> Applicable: SharePoint Server Subscription Edition

Specifies credentials to authenticate to the SMTP server.
Set the value to $null to connect to the SMTP server anonymously.
If this parameter isn't specified, the existing authentication settings will be preserved.

You must use the `Set-SPApplicationCredentialKey` PowerShell cmdlet to set an identical application credential key on each server in the farm before specifying credentials.

```yaml
Type: PSCredential
Parameter Sets: UpdateMailSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SMTPServer

> Applicable: SharePoint Server Subscription Edition

Specifies the new outbound SMTP server that this web application will use.
Set to $null to clear the server setting.

```yaml
Type: String
Parameter Sets: UpdateMailSettings
Aliases:

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

> Applicable: SharePoint Server Subscription Edition

Specifies the load-balanced URL for the web application zone.

```yaml
Type: String
Parameter Sets: UpdateIISSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseServerNameIndication

> Applicable: SharePoint Server Subscription Edition

Specifies that the Secure Sockets Layer (SSL) binding of this IIS website should use Server Name Indication (SNI).
Server Name Indication allows multiple IIS websites with unique host headers and unique server certificates to share the same SSL port.
If Server Name Indication isn't used, all IIS websites sharing the same SSL port must share the same SSL certificate.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateIISSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone

> Applicable: SharePoint Server Subscription Edition

When configuring zone-specific settings, the zone to configure must be specified.
This zone must already exist.

The type must be any one of the following values: Default, Intranet, Internet, Extranet, or Custom.

```yaml
Type: SPUrlZone
Parameter Sets: UpdateClaimSettings, UpdateIISSettings
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
