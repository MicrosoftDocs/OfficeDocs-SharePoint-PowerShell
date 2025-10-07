---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/set-sptrustedsecuritytokenissuer
applicable: SharePoint Server Subscription Edition
title: Set-SPTrustedSecurityTokenIssuer
schema: 2.0.0
---

# Set-SPTrustedSecurityTokenIssuer

## SYNOPSIS
Sets the trusted token issuer.

## SYNTAX

### ImportCertificateParameterSet
```
Set-SPTrustedSecurityTokenIssuer [-Identity] <SPTrustedSecurityTokenServicePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Certificate <X509Certificate2>] [-Confirm]
 [-Description <String>] [-IsTrustBroker] [-RegisteredIssuerName <String>] [-WhatIf] [<CommonParameters>]
```

### MetadataEndPointParameterSet
```
Set-SPTrustedSecurityTokenIssuer [-Identity] <SPTrustedSecurityTokenServicePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-Description <String>] [-IsTrustBroker]
 [-MetadataEndPoint <Uri>] [-RegisteredIssuerName <String>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

Use the `Set-SPTrustedSecurityTokenIssuer` cmdlet to set the trusted token issuer.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$a=Get-SPTrustedSecurityTokenIssuer
Set-SPTrustedSecurityTokenIssuer -Identity $a -MetadataEndpoint https://<webappurl/>/_layouts/15/metadata/json/1/
```

This example sets the metadata endpoint of the url for the self-issue.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the id of the SPTrustedSecurityTokenIssuer object to be set.

```yaml
Type: SPTrustedSecurityTokenServicePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

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

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Certificate

> Applicable: SharePoint Server Subscription Edition

Specifies the X509Certificate object that represents the public key of the signing certificate of the security token issuer.

```yaml
Type: X509Certificate2
Parameter Sets: ImportCertificateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

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

### -Description

> Applicable: SharePoint Server Subscription Edition

Specifies the description of the issuer.

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

### -IsTrustBroker

> Applicable: SharePoint Server Subscription Edition

Specifies whether the trust is established with a self-issuer partner app (that is, Exchange Server or Lync).

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

### -MetadataEndPoint

> Applicable: SharePoint Server Subscription Edition

Specifies the URI for the metadata endpoint of the issuer.

```yaml
Type: Uri
Parameter Sets: MetadataEndPointParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegisteredIssuerName

> Applicable: SharePoint Server Subscription Edition

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

### -WhatIf

> Applicable: SharePoint Server Subscription Edition

Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: `get-help about_commonparameters`

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-SPTrustedSecurityTokenIssuer](Get-SPTrustedSecurityTokenIssuer.md)

[New-SPTrustedSecurityTokenIssuer](New-SPTrustedSecurityTokenIssuer.md)

[Remove-SPTrustedSecurityTokenIssuer](Remove-SPTrustedSecurityTokenIssuer.md)
