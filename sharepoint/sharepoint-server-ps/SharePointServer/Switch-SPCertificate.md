---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/switch-spcertificate
applicable: SharePoint Server Subscription Edition
title: Switch-SPCertificate
schema: 2.0.0
---

# Switch-SPCertificate

## SYNOPSIS
Replaces existing certificate assignments with a new certificate.

## SYNTAX

```
Switch-SPCertificate [-Identity] <SPServerCertificatePipeBind> [-NewCertificate] <SPServerCertificatePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
You may wish to replace all usage of a certificate within SharePoint with a different certificate.
For example, if an existing certificate is approaching its expiration and you've imported a new certificate to replace it.
Use the Switch-SPCertificate cmdlet to replace the assignments of one certificate with a different certificate.
All usage of that certificate within SharePoint will then be replaced with the different certificate.

## EXAMPLES

### EXAMPLE
```powershell
Switch-SPCertificate -Identity "Team Sites Certificate (2020)" -NewCertificate "Team Sites Certificate (2021)"
```

This example replaces the assignments of the "Team Sites Certificate (2020)" certificate with the "Team Sites Certificate (2021)" certificate.

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

### -Identity
The certificate whose assignments you want to replace.

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

### -NewCertificate
The certificate that should replace all of the assignments of the certificate specified by the Identity parameter.

```yaml
Type: SPServerCertificatePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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
