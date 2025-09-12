---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spcertificatesettings
applicable: SharePoint Server Subscription Edition
title: Set-SPCertificateSettings
schema: 2.0.0
---

# Set-SPCertificateSettings

## SYNOPSIS
Configures certificate management settings.

## SYNTAX

```
Set-SPCertificateSettings [-OrganizationalUnit <String>] [-Organization <String>] [-Locality <String>]
 [-State <String>] [-Country <String>] [-KeyAlgorithm <KeyAlgorithmGroup>] [-KeySize <Int32>]
 [-EllipticCurve <EllipticCurveType>] [-HashAlgorithm <String>]
 [-RsaSignaturePadding <RsaSignaturePaddingType>] [-CertificateExpirationAttentionThreshold <Int32>]
 [-CertificateExpirationWarningThreshold <Int32>] [-CertificateExpirationErrorThreshold <Int32>]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
SharePoint supports farm-wide default settings for certificate management.
These include default properties for creating and renewing certificates and certificate health rule thresholds.

## EXAMPLES

### EXAMPLE
```powershell
Set-SPCertificateSettings -CertificateExpirationWarningThreshold 22
```

This examples changes the certificate expiration warning threshold to 22 days.
SharePoint will begin sending warnings about upcoming certificate expirations 22 days before they expire.

## PARAMETERS

### -AssignmentCollection
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

### -CertificateExpirationAttentionThreshold
Specifies the number of days before a certificate expires to trigger a certificate expiration notification.
This is a reminder of upcoming certificate expirations that can be handled with normal priority.
A certificate will only trigger a notification when it is assigned to SharePoint objects.
This notification is disabled when set to 0.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateExpirationErrorThreshold
Specifies the number of days after a certificate expired to trigger a certificate expiration alert.
This is an alert about certificates that have already expired and should be handled with critical priority.
A certificate will only trigger an alert when it is assigned to SharePoint objects.
This alert is disabled when set to 0.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateExpirationWarningThreshold
Specifies the number of days before a certificate expires to trigger a certificate expiration warning.
This is a warning of imminent certificate expirations that should be handled with high priority.
A certificate will only trigger a warning when it is assigned to SharePoint objects.
This warning is disabled when set to 0.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Country
The 2 letter country code where your organization is legally located.
This must be an ISO 3166-1 alpha-2 country code.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EllipticCurve
Specifies the elliptic curve of your public and private ECC keys.

Larger elliptic curves provide more cryptographic strength than smaller elliptic curves, but they're also more computationally expensive and take more time to complete the SSL/TLS connection.
Select nistP256 if you're unsure which elliptic curve to use.
Elliptic curves larger than nistP384 are not recommended.

```yaml
Type: EllipticCurveType
Parameter Sets: (All)
Aliases:
Accepted values: Default, nistP256, nistP384, nistP521

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HashAlgorithm
Specifies the hash algorithm of your certificate signature, which your certificate authority will use to verify that your certificate request hasn't been tampered with.

Larger hash algorithms provide more cryptographic strength than smaller hash algorithms, but they're also more computationally expensive.
Select SHA256 if you're unsure which hash algorithm to use.
Hash algorithms larger than SHA384 are not recommended.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Default, SHA256, SHA384, SHA512

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyAlgorithm
Specifies the key algorithm for your certificate.
This choice will be used for both the public key and the private key of your certificate.

RSA is the most common and widely supported key algorithm for certificates.
Select the RSA algorithm if you're unsure which type of key your certificate authority supports.

ECC uses elliptic curve cryptography based on ECDSA keys with NIST P-256, P-384, or P-521 curves.
SSL/TLS connections are faster to complete with ECC certificates than RSA certificates at the equivalent security strength.
Verify that your certificate authority supports ECC certificates before selecting it.

```yaml
Type: KeyAlgorithmGroup
Parameter Sets: (All)
Aliases:
Accepted values: ECC, RSA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeySize
Specifies the size of your public and private RSA keys in bits.

Larger key sizes provide more cryptographic strength than smaller key sizes, but they're also more computationally expensive and take more time to complete the SSL/TLS connection.
Select 2048 if you're unsure which key size to use.
Key sizes larger than 4096 are not recommended.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:
Accepted values: 0, 2048, 4096, 8192, 16384

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Locality
The name of the city or locality where your organization is legally located.
Do not abbreviate the name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Organization
The legally registered name of your organization or company.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrganizationalUnit
The name of your department within your organization or company.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RsaSignaturePadding
Specifies the RSA signature padding mode for creating and renewing certificates with RSA keys.
Pkcs1 represents the RSASSA-PKCS1-v1_5 padding mode.
Pss represents the RSASSA-PSS padding mode.
The default RSA signature padding mode is Pkcs1.

```yaml
Type: RsaSignaturePaddingType
Parameter Sets: (All)
Aliases:
Accepted values: Default, Pkcs1, Pss

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
The name of the state or province where your organization is legally located.
Do not abbreviate the name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

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

Required: False
Position: Named
Default value: None
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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
