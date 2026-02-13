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

Connects a SharePoint Administrator or SharePoint Embedded Administrator to the SharePoint admin center. You must run this cmdlet before running any other SharePoint Online cmdlets.

## SYNTAX

### AuthenticationCertificate

```
Connect-SPOService [-Url] <UrlCmdletPipeBind> [[-ClientTag] <String>] [-Region <AADCrossTenantAuthenticationLocation>] [-AuthenticationUrl <String>] [-Certificate <X509Certificate2>] [-CertificatePath <String>] [-CertificateThumbprint <String>] [-CertificatePassword <SecureString>] -ClientId <String> -TenantId <String> [<CommonParameters>]
```

### AuthenticationLocation

```
Connect-SPOService [-Url] <UrlCmdletPipeBind> [[-Credential] <CredentialCmdletPipeBind>] [[-ClientTag] <String>] [-Region <AADCrossTenantAuthenticationLocation>] [[-ModernAuth] <Boolean>] [[-UseSystemBrowser] <Boolean>]
```

### AuthenticationUrl

```
Connect-SPOService [-Url] <UrlCmdletPipeBind> [[-Credential] <CredentialCmdletPipeBind>] [[-ClientTag] <String>] -AuthenticationUrl <String> [[-ModernAuth] <Boolean>] [[-UseSystemBrowser] <Boolean>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet connects a SharePoint Administrator or SharePoint Embedded Administrator to the SharePoint admin center.
Only one SharePoint Online service connection is supported per Windows PowerShell session and per geo within an organization. If you run this cmdlet again, the existing connection is automatically disconnected and replaced with the new connection. The PowerShell session then uses the newly specified administrator context.
Delegated partner administrators must switch connections when managing multiple organizations within the same PowerShell session.
To run this cmdlet, you must be a SharePoint Administrator or SharePoint Embedded Administrator.
For permission requirements and the latest guidance, see the [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell) documentation.

## EXAMPLES

### EXAMPLE 1

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com -Credential admin@contoso.com
```

This example shows how a SharePoint Administrator using the `admin@contoso.com` account connects to the SharePoint admin center at `https://contoso-admin.sharepoint.com`.

### EXAMPLE 2

```powershell
$username = "admin@contoso.sharepoint.com"
$password = Read-Host -Prompt "Enter user password" -AsSecureString
$cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $userName, $password
Connect-SPOService -Url https://contoso-admin.sharepoint.com -Credential $cred
```

This example shows how a SharePoint Administrator connects to the SharePoint admin center at `https://contoso-admin.sharepoint.com` by creating a credential object from a username and password.

### EXAMPLE 3

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com
```

This example prompts for credentials. This approach is required when the account uses multi-factor authentication.

### EXAMPLE 4

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com -Region ITAR
```

This example connects to the SharePoint admin center by specifying the authentication region.

### EXAMPLE 5

```powershell
Connect-SPOService -Credential $creds -Url https://tenant-admin.sharepoint.com -ModernAuth $true -AuthenticationUrl https://login.microsoftonline.com/organizations
```

This example connects to the SharePoint admin center by using modern authentication.

### EXAMPLE 6

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com -UseSystemBrowser $true
```

This example authenticates by using the Microsoft Authentication Library (MSAL) and connects to the SharePoint admin center after authentication succeeds.

### EXAMPLE 7

```powershell
$password = Read-Host -Prompt "Enter certificate password" -AsSecureString
Connect-SPOService -Url https://contoso-admin.sharepoint.com -ClientId 00000000-0000-0000-0000-000000000000 -TenantId 11111111-1111-1111-1111-111111111111 -CertificatePath C:\Certs\ContosoAppAuth.pfx -CertificatePassword $password
```

This example connects to the SharePoint admin center by using an app identity and a certificate file path, with an optional certificate password.

### EXAMPLE 8

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com -ClientId 00000000-0000-0000-0000-000000000000 -TenantId 11111111-1111-1111-1111-111111111111 -CertificateThumbprint "3FAAAA1111AAAAAAAAAAA2222AAAAAAAAAAAAAAA"
```

This example connects to the SharePoint admin center by using an app identity and a certificate thumbprint.

### EXAMPLE 9

```powershell
$thumbprint = "3F2A5C9D4E7B8A1234567890ABCDEF1234567890"
$cert = Get-ChildItem Cert:\LocalMachine\My\$thumbprint
Connect-SPOService -Url https://contoso-admin.sharepoint.com -ClientId 00000000-0000-0000-0000-000000000000 -TenantId 11111111-1111-1111-1111-111111111111 -Certificate $cert
```

This example connects to the SharePoint admin center by using an app identity and a certificate object.

## PARAMETERS

### -AuthenticationUrl

> Applicable: SharePoint Online

Specifies the URL for the Microsoft Entra cross-tenant authentication service. Use this parameter when a non-default cross-tenant authentication endpoint is required.

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

### -Certificate

> Applicable: SharePoint Online

Specifies the X.509 certificate used for authentication.

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

Specifies the password for the certificate file.

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

Specifies the path to the local `.pfx` certificate file.

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

Specifies the thumbprint of the certificate in the current user's certificate store.

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

Specifies the client ID of the application.

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

Optionally adds a client tag to CSOM HTTP traffic to help identify the calling script or solution.

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

Specifies the credentials used to connect. If you do not provide credentials, you are prompted to enter them. The credentials must belong to an administrator who has access to the SharePoint admin center.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.CredentialCmdletPipeBind
Parameter Sets: AuthenticationUrl, AuthenticationLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ModernAuth

> Applicable: SharePoint Online

Enables modern authentication when connecting to SharePoint administration cmdlets.
When you use this parameter, you must also specify the `AuthenticationUrl` parameter.

```yaml
Type: System.Boolean
Parameter Sets: AuthenticationUrl, AuthenticationLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region

> Applicable: SharePoint Online

Specifies the authentication region. Valid values are: `Default`, `ITAR`, `Germany`, and `China`.
The default value is `Default`.
**Note:** The `ITAR` value applies only to GCC High and DoD tenants.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.AADCrossTenantAuthenticationLocation
Parameter Sets: AuthenticationLocation, AuthenticationCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId

> Applicable: SharePoint Online

Specifies the ID of the tenant to connect to.

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

Specifies the URL of the SharePoint admin center.

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

Uses the Microsoft Authentication Library (MSAL) to authenticate the user by using the system browser.

> [!NOTE]
> To avoid adding the `-UseSystemBrowser` parameter every time you run `Connect-SPOService`, you can set a registry key instead.
>
> Set the `UseSystemBrowser` registry key (type `REG_DWORD`) at:
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\SPO\CMDLETS\`
>
> If either registry key is set to a non-zero integer value or `-UseSystemBrowser` parameter is set to `true`, authentication flow will use system browser for sign-in.

```yaml
Type: System.Boolean
Parameter Sets: AuthenticationUrl, AuthenticationLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.UrlCmdletPipeBind

### Microsoft.Online.SharePoint.PowerShell.CredentialCmdletPipeBind

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Introduction to the SharePoint Online management shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Disconnect-SPOService](./Disconnect-SPOService.md)