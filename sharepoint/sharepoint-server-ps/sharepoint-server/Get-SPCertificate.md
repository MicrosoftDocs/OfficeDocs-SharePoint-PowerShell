---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/get-spcertificate
applicable: SharePoint Server Subscription Edition
title: Get-SPCertificate
schema: 2.0.0
author:
ms.author:
ms.reviewer:
---

# Get-SPCertificate

## SYNOPSIS
Returns all certificates that match the specified criteria.

## SYNTAX

### SearchFilters (Default)
```
Get-SPCertificate [-DisplayName <String>] [-Thumbprint <String>] [-SerialNumber <String>] [-Store <String>]
 [-InUse] [-DaysToExpiration <Int32>] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Identity
```
Get-SPCertificate [-Identity] <SPServerCertificatePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The Get-SPCertificate cmdlet returns either a single certificate that matches the Identity parameter, or all the certificates that match the filtering criteria of the optional parameters.
If no parameters are specified, all certificates in the farm are returned.

## EXAMPLES

### ------------EXAMPLE 1-----------
```powershell
Get-SPCertificate -DisplayName "Team Sites Certificate"
```

This example gets all certificates in the farm with the display name "Team Sites Certificate".

### ------------EXAMPLE 2-----------
```powershell
Get-SPCertificate -InUse -DaysToExpiration 30
```

This example gets all certificates that are in use and will expire within the next 30 days.

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

### -DaysToExpiration
If a positive number, only return certificates that will expire in the number of days from now specified by this parameter.
Specify "-1" to only return certificates that have already expired.
Specifying "0" will result in no filtering based on expiration date.

```yaml
Type: Int32
Parameter Sets: SearchFilters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
The display name of the certificate to find.
Use this parameter instead of the Identity parameter if multiple certificates might match this criteria.
The Identity parameter can only return a single certificate.

```yaml
Type: String
Parameter Sets: SearchFilters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
Specifies the display name, thumbprint, serial number, or GUID of the certificate to find.
If multiple certificates match the identity specified, no certificates will be returned.
Use the filtering criteria of the optional parameters when multiple certificates would match.

The type must be a valid display name, in the form "Certificate Display Name", a valid thumbprint, in the form "1234567890ABCDEF1234567890ABCDEF12345678", a valid serial number, in the form "1234567890ABCDEF1234567890ABCDEF", or a valid GUID, in the form "12345678-90ab-cdef-1234-567890abcdef".

```yaml
Type: SPServerCertificatePipeBind
Parameter Sets: Identity
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InUse
Specifies to only return certificates that are directly assigned to SharePoint objects (i.e.
currently in use).

```yaml
Type: SwitchParameter
Parameter Sets: SearchFilters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SerialNumber
The serial number of the certificate to find, in the form "1234567890ABCDEF1234567890ABCDEF".

```yaml
Type: String
Parameter Sets: SearchFilters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Store
Specifies the certificate store to search.
If this parameter isn't specified, all certificate stores will be searched.

```yaml
Type: String
Parameter Sets: SearchFilters
Aliases:
Accepted values: EndEntity, Intermediate, Pending, Root

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Thumbprint
The thumbprint of the certificate to find, in the form "1234567890ABCDEF1234567890ABCDEF12345678".

```yaml
Type: String
Parameter Sets: SearchFilters
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
