---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/connect-sposervice
applicable: SharePoint Online
title: Connect-SPOService
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Connect-SPOService

## SYNOPSIS

Connects the SharePoint Online Administrator or the SharePoint Embedded Administrator to a SharePoint Online connection (the SharePoint Online Administration Center).
This cmdlet must be run before any other SharePoint Online cmdlets can run.

## SYNTAX

### AuthenticationCertificate

```
Connect-SPOService -Url <UrlCmdletPipeBind> [-ClientTag <String>] [-Region <AADCrossTenantAuthenticationLocation>] [-AuthenticationUrl <String>] [-Certificate <X509Certificate2>] [-CertificatePath <String>] [-CertificateThumbprint <String>] [-CertificatePassword <SecureString>] -ClientId <String> -TenantId <String>
 [<CommonParameters>]
```

### AuthenticationLocation

```
Connect-SPOService -Url <UrlCmdletPipeBind> [-Credential <CredentialCmdletPipeBind>] [-ClientTag <String>]
 [-Region <AADCrossTenantAuthenticationLocation>] [-ModernAuth <Boolean>] [-UseSystemBrowser <Boolean>]
 [<CommonParameters>]
```

### AuthenticationUrl

```
Connect-SPOService -Url <UrlCmdletPipeBind> [-Credential <CredentialCmdletPipeBind>] [-ClientTag <String>]
 -AuthenticationUrl <String> [-ModernAuth <Boolean>] [-UseSystemBrowser <Boolean>] [<CommonParameters>]
```

## DESCRIPTION

The `Connect-SPOService` cmdlet connects the SharePoint Online Administrator or the SharePoint Embedded Administrator to the SharePoint Online Administration Center.

Only a single SharePoint Online service connection is maintained from any single Windows PowerShell session.
In other words, this is a per-geo within an organization administrator connection.
Running the `Connect-SPOService` cmdlet twice implicitly disconnects the previous connection.
The Windows PowerShell session will be set to serve the new SharePoint Online administrator specified.

A delegated partner administrator has to swap connections for different organizations within the same Windows PowerShell session.

You must be a SharePoint Online Administrator or a SharePoint Embedded Administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com -credential admin@contoso.com
```

Example 1 shows how a SharePoint Online administrator with credential admin@contoso.com connects to a SharePoint Online Administration Center that has the URL `<https://contoso-admin.sharepoint.com.>`

### EXAMPLE 2

```powershell
$username = "admin@contoso.sharepoint.com"
$password = "password"
$cred = New-Object -TypeName System.Management.Automation.PSCredential -argumentlist $userName, $(convertto-securestring $Password -asplaintext -force)
Connect-SPOService -Url https://contoso-admin.sharepoint.com -Credential $cred
```

Example 2 shows how a SharePoint Online administrator with a username and password connects to a SharePoint Online Administration Center that has the URL `<https://contoso-admin.sharepoint.com.>`

### EXAMPLE 3

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com
```

Prompts for credentials. This is required if the account is using multi-factor authentication.

### EXAMPLE 4

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com -Region ITAR
```

Connects to a SharePoint Online Administration Center specifying the region.

### EXAMPLE 5

```powershell
Connect-SPOService -Credential $creds -Url https://tenant-admin.sharepoint.com -ModernAuth $true -AuthenticationUrl https://login.microsoftonline.com/organizations
```
Connecting to SPO Service with ModernAuth Flag.

### EXAMPLE 6

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com -UseSystemBrowser $true
```
Authenticates using the Microsoft Authentication Library (MSAL) and connects to the SharePoint Online Administration Center on successful authentication.

## PARAMETERS

### -AuthenticationUrl

> Applicable: SharePoint Online

Location for Microsoft Entra Cross-Tenant Authentication service. Can be optionally used if non-default Cross-Tenant Authentication Service is used.

```yaml
Type: System.String
Parameter Sets: AuthenticationUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certificate

> Applicable: SharePoint Online

An X.509 certificate used during authentication.

```yaml
Type: X509Certificate2
Parameter Sets: AuthenticationCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword

> Applicable: SharePoint Online

The password for the certificate file.

```yaml
Type: SecureString
Parameter Sets: AuthenticationCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePath

> Applicable: SharePoint Online

The path to the local .pfx certificate file.

```yaml
Type: String
Parameter Sets: AuthenticationCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint

> Applicable: SharePoint Online

The thumbprint of the certificate in the current user’s certificate store.

```yaml
Type: String
Parameter Sets: AuthenticationCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientId

> Applicable: SharePoint Online

The application’s client ID.

```yaml
Type: String
Parameter Sets: AuthenticationCertificate
Aliases: ApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTag

> Applicable: SharePoint Online

Permits appending a client tag to existing client tag. Used optionally in the CSOM http traffic to identify used script or solution.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential

> Applicable: SharePoint Online

Specifies the credentials to use to connect. If no credentials are presented, a dialog will prompt for the credentials. The credentials must be those of a SharePoint Online administrator who can access the SharePoint Online Administration Center site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.CredentialCmdletPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ModernAuth

> Applicable: SharePoint Online

Ensures that SharePoint Online tenant administration cmdlets can connect to the service using modern TLS protocols.

To use it you also need to provide the **AuthenticationUrl** parameter.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region

> Applicable: SharePoint Online

The valid values are: Default | ITAR | Germany | China

The default value is "default".

**Note**: The ITAR value is for GCC High and DoD tenancies only.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.AADCrossTenantAuthenticationLocation
Parameter Sets: AuthenticationLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId

> Applicable: SharePoint Online

The tenant ID to connect to.

```yaml
Type: String
Parameter Sets: AuthenticationCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Url

> Applicable: SharePoint Online

Specifies the URL of the SharePoint Online Administration Center site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.UrlCmdletPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -UseSystemBrowser

> Applicable: SharePoint Online

Used to authenticate the user using the Microsoft Authentication Library (MSAL).

> [!NOTE]
> To avoid adding the `-UseSystemBrowser` parameter every time you run `Connect-SPOService`, you can set a registry key instead.
>
> Set the `UseSystemBrowser` registry key (type `REG_DWORD`) at: 
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\SPO\CMDLETS\`
>
> If either registry key is set to a non-zero integer value or `-UseSystemBrowser` parameter is set to `true`, authentication flow will use system browser for sign-in.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Introduction to the SharePoint Online management shell](https://support.office.com/en-us/article/introduction-to-the-sharepoint-online-management-shell-c16941c3-19b4-4710-8056-34c034493429)

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Disconnect-SPOService](Disconnect-SPOService.md)
