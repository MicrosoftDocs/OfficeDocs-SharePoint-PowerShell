---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/import-spcertificate
applicable: SharePoint Server Subscription Edition
title: Import-SPCertificate
schema: 2.0.0
ms.date: 08/26/2025
---

# Import-SPCertificate

## SYNOPSIS
Imports certificates into the SharePoint farm.

## SYNTAX

```
Import-SPCertificate [-Path] <String> [-Password <SecureString>] [-Store <String>] [-Exportable] [-Replace]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Imports certificates from the specified file into the SharePoint farm.

SharePoint supports both RSA and Elliptic Curve Cryptography (ECC) certificates.
You can import certificates from PFX (PKCS #12) files, P7B (PKCS #7) files, and CER files.
Only PFX files will contain private keys for certificates, which are necessary for a server certificate to be assigned to an IIS web site.
However, the entire certificate chain, from the end entity (leaf) certificate to the root certificate, must be imported to SharePoint for SSL connections to be successful.

Certificates are automatically deployed to the Windows certificate store on each server in the SharePoint farm when they are imported into SharePoint.
Certificates are also automatically deployed to new servers in the SharePoint farm when those servers join the farm.

Disconnecting a server from a SharePoint farm will not automatically remove SharePoint-managed certificates from that server's Windows certificate store.
Uninstalling SharePoint from a server will not automatically remove SharePoint-managed certificates from that server's Windows certificate store.

## EXAMPLES

### EXAMPLE 1
```powershell
$password = ConvertTo-SecureString -AsPlainText -Force

Import-SPCertificate -Path "\\server\fileshare\certificates.pfx" -Password $password -Exportable
```

This example imports certificates and any associated private keys from the \\\\server\fileshare\certificates.pfx file into the SharePoint farm.
It also allows private keys that were imported during this operation to be exported from SharePoint in the future.

### EXAMPLE 2
```powershell
Import-SPCertificate -Path D:\test.cer
```

This example imports a certificate from the D:\test.cer file into the SharePoint farm.

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

### -Exportable
Specifies whether private keys of the certificates imported into SharePoint may be exported.
If this parameter isn't specified, the private keys of certificates deployed to the Windows Certificate Store on each server in the SharePoint farm will not be exportable, and SharePoint will not allow you to export the private keys from within the SharePoint administration interface.

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

### -Password
The password if the certificate file is protected by a password (for PFX files).

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The path to the PFX, P7B, or CER file containing certificates.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Replace
Specifies that if the certificates being imported are renewing existing certificates, the certificate assignments of the existing certificates should be immediately replaced with the imported certificates.

If the certificates being imported aren't renewing existing certificates, no changes will be made to certificate assignment.

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

### -Store
The certificate store that certificates should be imported into.
Unless there's a need to override SharePoint's automatic certificate detection, we recommend omitting this parameter so that SharePoint will automatically select the appropriate certificate store for each certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EndEntity, Intermediate, Pending, Root

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
