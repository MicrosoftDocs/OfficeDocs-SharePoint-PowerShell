---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-sptrustedidentitytokenissuer
applicable: SharePoint Server Subscription Edition
title: Set-SPTrustedIdentityTokenIssuer
schema: 2.0.0
---

# Set-SPTrustedIdentityTokenIssuer

## SYNOPSIS
Sets the identity providers of a Web application.


## SYNTAX

### ImportCertificateParameterSet
```
Set-SPTrustedIdentityTokenIssuer [-Identity] <SPTrustedIdentityTokenIssuerPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-ClaimProvider <SPClaimProviderPipeBind>]
 [-ClaimsMappings <SPClaimMappingPipeBind[]>] [-Description <String>]
 -ImportTrustCertificate <X509Certificate2> [-Realm <String>] [-SignInUrl <String>] [-UseWReply] [-Confirm]
 [-RegisteredIssuerName <String>] [-UseStateToRedirect <Boolean>] [-WhatIf] [<CommonParameters>]
```

### MetadataEndPointParameterSet
```
Set-SPTrustedIdentityTokenIssuer [-Identity] <SPTrustedIdentityTokenIssuerPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-ClaimProvider <SPClaimProviderPipeBind>]
 [-ClaimsMappings <SPClaimMappingPipeBind[]>] [-Description <String>] -MetadataEndPoint <Uri> [-Realm <String>]
 [-SignInUrl <String>] [-UseWReply] [-Confirm] [-RegisteredIssuerName <String>] [-UseStateToRedirect <Boolean>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The Set-SPTrustedIdentityTokenIssuer cmdlet sets the identity providers of a Web application or extended Web application.
For the ASP.NET Membership provider and Role provider, this cmdlet changes the identity provider only if the result is piped to a variable and passed to a Web application.
For security token service (STS) identity providers, this cmdlet changes the persisted identity provider object in the SPFarm object.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### -------------------------EXAMPLE 1----------------------
```powershell
Set-SPTrustedIdentityTokenIssuer "LiveIDSTS" -Certificate (Get-ChildItem"cert:Certificates (LocalComputer)\Personal\Certificates -Name "LiveID Cert")
```

This example sets the identity provider to LiveIDSTS.


### -------------------------EXAMPLE 2----------------------
```powershell
$ip = @( (Get-SPTrustedIdentityTokenIssuer "LiveID STS"), (New-SPTrustedIdentityTokenIssuer -ASPNetMembershipProvider "myMembershipProvider" -ASPNetRoleProvider "myRoleProvider"), (Get-SPTrustedIdentityTokenIssuer "NTLM")) )
New-SPWebApplication https://contoso.com -IdentityProvider $ip
```

This example sets the identity provider using the .ASPNetMembership and Role parameters.
When these parameters are used, a variable must be set; otherwise, the values do not take effect.

### -------------------------EXAMPLE 3----------------------
```powershell
$cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2('C:\MyCert.cer')
Set-SPTrustedIdentityTokenIssuer "LiveIDSTS" -ImportTrustCertificate $cert
```

This example updates the certificate used by the identity provider.

## PARAMETERS

### -Identity
Specifies the identity provider to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of identity provider (for example, LiveID STS); or an instance of a valid SPIdentityProvider object.

```yaml
Type: SPTrustedIdentityTokenIssuerPipeBind
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

### -ClaimProvider
Specifies the IP STS that can resolve and search claims for claims people picker.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a claim provider (for example, MyIDprovider1); or an instance of a valid SPClaimProvider object.

```yaml
Type: SPClaimProviderPipeBind
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClaimsMappings
Specifies the mapping of the claims from the original token to the SharePoint token.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a claim mapping rule (for example, Email); or an instance of a valid SPClaimMapping object.

```yaml
Type: SPClaimMappingPipeBind[]
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description for the new identity provider.

The type must be a valid string; for example, LiveID STS.

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

### -ImportTrustCertificate
Specifies the X.509 certificate object from trusted authentication provider farm.

The type must be a name of a valid X.509 certificate; for example, Certificate1.

```yaml
Type: X509Certificate2
Parameter Sets: ImportCertificateParameterSet
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetadataEndPoint
Specifies the Uri of the metadata endpoint.

```yaml
Type: Uri
Parameter Sets: MetadataEndPointParameterSet
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Realm
Specifies the realm, or resource partition, associated with this trust.

The type must be a name of a valid realm; for example, MD_REALM.

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

### -SignInUrl
Specifies the sign-in URLs for this trusted identity provider STS.

The type must be a valid URL, in the form https://int.live.com/.

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

### -UseWReply
Includes a WReply with the token request.
Wreply is a URL at the relying party to which the requestor is redirected once sign-out processing is complete.

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
Prompts you for confirmation before running the cmdlet.

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

### -RegisteredIssuerName
Specifies the registered name of the token issuer, typically a URI, for example: "https://sts.windows.net/yourTenantId/"

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

### -UseStateToRedirect
Specifies whether or not to use the URI within the "state" property of client authentication requests to determine the proper page to redirect the client to after authentication.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
