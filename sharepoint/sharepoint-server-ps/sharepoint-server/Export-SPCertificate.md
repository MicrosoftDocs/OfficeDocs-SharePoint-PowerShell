---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version:
schema: 2.0.0
---

# Export-SPCertificate

## SYNOPSIS
Exports certificates from the SharePoint farm.

## SYNTAX

### Pfx
```powershell
PS C:\> Export-SPCertificate [-Identity] <SPServerCertificatePipeBind> -Password <SecureString>
 [-EncryptionType <String>] [-IncludeAllCertificatesInCertificationPath] [-NoExtendedProperties]
 [-Path <String>] [-Force] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Cert/Pkcs7
```powershell
PS C:\> Export-SPCertificate [-Identity] <SPServerCertificatePipeBind> -Type <String>
 [-IncludeAllCertificatesInCertificationPath] [-Path <String>] [-Force]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Exports certificates from the SharePoint farm into a certificate file.
This exported certificate file is stored in the Central Administration site by default, but can also be stored in a path specified by the Path parameter.

SharePoint supports exporting certificates to PFX (PKCS #12) files, P7B (PKCS #7) files, and CER files.
Both PFX files and P7B files can contain multiple certificates, which is useful for exporting a chain of certificates from the end entity (leaf) certificate to the root certificate. 
However, only PFX files can contain private keys for certificates, which are necessary for a server certificate to be assigned to an IIS web site.
CER files contain only a single certificate.

## EXAMPLES

### ------------EXAMPLE 1-----------
```powershell
PS C:\> $password = ConvertTo-SecureString -AsPlainText -Force 
 
PS C:\> Export-SPCertificate -Identity "Team Site Certificate" -Password $password -IncludeAllCertificatesInCertificationPath -IncludeExtendedProperties -Path "\\server\fileshare\certificates.pfx"
```

This example exports the "Team Sites Certificate" certificate and its private key to the \\\\server\fileshare\certificates.pfx file.

### ------------EXAMPLE 2-----------
```powershell
PS C:\> Export-SPCertificate -Identity "Team Site Certificate" -Type Cert
```

This example exports the "Team Sites Certificate" certificate to a Cert file that's stored in Central Administration.

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

### -EncryptionType
Specifies the encryption algorithm to use to protect the exported PFX file.
AES256 specifies that AES-256 encryption with SHA256 hashing will be used.
TripleDes specifies that 3DES encryption with SHA1 hashing will be used.
AES-256 encryption is stronger than 3DES encryption, but is only supported with PFX files on Windows Server 2019 and newer operating systems.
Use 3DES encryption if the PFX file needs to be compatible with older operating systems.
If this parameter isn't specified, AES-256 encryption is used by default.
This parameter is only compatible with PFX files.

```yaml
Type: String
Parameter Sets: Pfx
Aliases:
Accepted values: AES256, TripleDes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Specifies to overwrite a file if it already exists at the specified path.

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

### -Identity
The certificate to export.

```yaml
Type: SPServerCertificatePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IncludeAllCertificatesInCertificationPath
Specifies whether to export additional certificates that are part of the certificate chain of the specified certificate.
This will only add parent certificates of the specified certificate, not child certificates issued by the specified certificate.
This parameter is only compatible with PFX and P7B files.

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

### -NoExtendedProperties
Specifies whether extended properties of the certificate should not be exported, such as the friendly name of the certificate.
This parameter is only compatible with PFX files.

```yaml
Type: SwitchParameter
Parameter Sets: Pfx
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
The password to use to protect the exported PFX file.
This parameter is only compatible with PFX files.

```yaml
Type: SecureString
Parameter Sets: Pfx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The path to the PFX, P7B, or CER file that the certificates should be exported to.

The certificates will also be exported to a certificate file stored in Central Administration regardless of whether this parameter is specified.

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

### -Type
Specifies the type of file to generate.
Cert will generate a CER file containing a single DER-encoded certificate.
Pkcs7 will generate a P7B (PKCS #7) file containing one or more certificates.
This parameter is only compatible with CER and P7B files.

```yaml
Type: String
Parameter Sets: Cert/Pkcs7
Aliases:
Accepted values: Cert, Pkcs7

Required: True
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
