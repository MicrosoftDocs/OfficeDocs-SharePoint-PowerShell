---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/connect-sposervice
applicable: SharePoint Online
title: Connect-SPOService
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Connect-SPOService

## SYNOPSIS

Connects a SharePoint Online administrator or SharePoint Embedded administrator to a SharePoint Online connection (the SharePoint Online Administration Center).
This cmdlet must be run before any other SharePoint Online cmdlets can run.

## SYNTAX

### AuthenticationUrl
```
Connect-SPOService [-Url] <UrlCmdletPipeBind> [[-Credential] <CredentialCmdletPipeBind>]
 [[-ClientTag] <String>] [-AuthenticationUrl] <String> [[-ModernAuth] <Boolean>]
 [[-UseSystemBrowser] <Boolean>] [<CommonParameters>]
```

### AuthenticationLocation

```
Connect-SPOService [-Url] <UrlCmdletPipeBind> [[-Credential] <CredentialCmdletPipeBind>]
 [[-ClientTag] <String>] [[-Region] <AADCrossTenantAuthenticationLocation>] [[-ModernAuth] <Boolean>]
 [[-UseSystemBrowser] <Boolean>] [<CommonParameters>]
```

## DESCRIPTION

The `Connect-SPOService` cmdlet connects a SharePoint Online administrator or the SharePoint Embedded administrator to the SharePoint Online Administration Center.

Only a single SharePoint Online service connection is maintained from any single Windows PowerShell session.
In other words, this is a per-geo within an organization administrator connection.
Running the `Connect-SPOService` cmdlet twice implicitly disconnects the previous connection.
The Windows PowerShell session will be set to serve the new SharePoint Online administrator or SharePoint Embedded administrator specified.

A delegated partner administrator has to swap connections for different organizations within the same Windows PowerShell session.

You must be a SharePoint Online administrator or SharePoint Embedded administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com -credential admin@contoso.com
```

Example 1 shows how a SharePoint Online administrator or SharePoint Embedded administrator with credential admin@contoso.com connects to a SharePoint Online Administration Center that has the URL `<https://contoso-admin.sharepoint.com.>`

### -----------------------EXAMPLE 2-----------------------------

```powershell
$username = "admin@contoso.sharepoint.com"
$password = "password"
$cred = New-Object -TypeName System.Management.Automation.PSCredential -argumentlist $userName, $(convertto-securestring $Password -asplaintext -force)
Connect-SPOService -Url https://contoso-admin.sharepoint.com -Credential $cred
```

Example 2 shows how a SharePoint Online administrator or SharePoint Embedded administrator with a username and password connects to a SharePoint Online Administration Center that has the URL `<https://contoso-admin.sharepoint.com.>`

### --------------------`---EXAMPLE 3-----------------------------

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com
```

Prompts for credentials. This is required if the account is using multi-factor authentication.

### -----------------------EXAMPLE 4-----------------------------

```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com -Region ITAR
```

Connects to a SharePoint Online Administration Center specifying the region.

### -----------------------EXAMPLE 5-----------------------------

 ```powershell
Connect-SPOService -Credential $creds -Url https://tenant-admin.sharepoint.com -ModernAuth $true -AuthenticationUrl https://login.microsoftonline.com/organizations
```
Connecting to SPO Service with ModernAuth Flag.

### -----------------------EXAMPLE 6-----------------------------

 ```powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com -UseSystemBrowser $true
```
Authenticates using the Microsoft Authentication Library (MSAL) and connects to the SharePoint Online Administration Center on successful authentication.

## PARAMETERS

### -AuthenticationUrl

Location for Microsoft Entra Cross-Tenant Authentication service. Can be optionally used if non-default Cross-Tenant Authentication Service is used.

```yaml
Type: String
Parameter Sets: AuthenticationUrl
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTag

Permits appending a client tag to existing client tag. Used optionally in the CSOM http traffic to identify used script or solution.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential

Specifies the credentials to use to connect. If no credentials are presented, a dialog will prompt for the credentials. The credentials must be those of a SharePoint Online administrator or SharePoint Embedded administrator who can access the SharePoint Online Administration Center site.

```yaml
Type: CredentialCmdletPipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Region

The valid values are: Default | ITAR | Germany | China

The default value is "default".

**Note**: The ITAR value is for GCC High and DoD tenancies only.

```yaml
Type: AADCrossTenantAuthenticationLocation
Parameter Sets: AuthenticationLocation
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Url

Specifies the URL of the SharePoint Online Administration Center site.

```yaml
Type: UrlCmdletPipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ModernAuth

 Ensures that SharePoint Online tenant administration cmdlets can connect to the service using modern TLS protocols.

To use it you also need to provide the **AuthenticationUrl** parameter.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```
### -UseSystemBrowser

 Used to authenticate the user using the Microsoft Authentication Library (MSAL).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -ProgressAction, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).


## RELATED LINKS

[Introduction to the SharePoint Online management shell](https://support.office.com/en-us/article/introduction-to-the-sharepoint-online-management-shell-c16941c3-19b4-4710-8056-34c034493429)

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Disconnect-SPOService](Disconnect-SPOService.md)
