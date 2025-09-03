---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/add-spclaimtypemapping
applicable: SharePoint Server Subscription Edition
title: Add-SPClaimTypeMapping
schema: 2.0.0
ms.date: 08/26/2025
---

# Add-SPClaimTypeMapping

## SYNOPSIS

Adds a claim mapping to a trusted security token service (STS) identity provider.


## SYNTAX

```
Add-SPClaimTypeMapping [-Identity] <SPClaimMappingPipeBind>
 [-TrustedIdentityTokenIssuer] <SPTrustedIdentityTokenIssuerPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Force] [<CommonParameters>]
```

## DESCRIPTION
The Add-SPClaimTypeMapping cmdlet adds a claim type mapping rule to a security token service (STS) identity provider from a farm trust STS authentication provider.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$trustedIdentityTokenIssuer = Get-SPTrustedIdentityTokenIssuer -Name "LiveIDSTS"

$trustedIdentityTokenIssuer.ClaimTypes.Add("http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier")

$trustedIdentityTokenIssuer.Update()

$mapping = New-SPClaimTypeMapping -IncomingClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier" -IncomingClaimTypeDisplayName "PUID" -LocalClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/thumbprint"

$mapping | Add-SPClaimTypeMapping -TrustedIdentityTokenIssuer $trustedIdentityTokenIssuer
```

This example adds a claim mapping to a trusted identity token issuer.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the STS for the farm that will issue the security token for the identity provider.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a claim mapping rule (for example, ClaimMap1); or an instance of a valid SPClaimMapping object.

```yaml
Type: SPClaimMappingPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TrustedIdentityTokenIssuer

> Applicable: SharePoint Server Subscription Edition

Specifies the farm trust Token Issuer (STS authentication provider).

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890abcdef; or a valid name of an authentication provider (for example, MyIDprovider1); or an instance of a valid SPTrustedIdentityTokenIssuer object.

```yaml
Type: SPTrustedIdentityTokenIssuerPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

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

### -Force

> Applicable: SharePoint Server Subscription Edition

Overwrites the claim mapping rule if it exists.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
