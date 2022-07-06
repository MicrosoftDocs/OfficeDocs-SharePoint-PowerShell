---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version:
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
```
Switch-SPCertificate -Identity "Team Sites Certificate (2020)" -NewCertificate "Team Sites Certificate (2021)"
```

This example replaces the assignments of the "Team Sites Certificate (2020)" certificate with the "Team Sites Certificate (2021)" certificate.

## PARAMETERS

### -AssignmentCollection
{{ Fill AssignmentCollection Description }}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
