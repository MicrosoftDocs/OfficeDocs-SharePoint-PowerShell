---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/new-spclaimprovider
applicable: SharePoint Server Subscription Edition
title: New-SPClaimProvider
schema: 2.0.0
---

# New-SPClaimProvider

## SYNOPSIS

Registers a new claim provider in the farm.


## SYNTAX

```
New-SPClaimProvider -AssemblyName <String> -Description <String> -DisplayName <String> -Type <String>
 [-AssignmentCollection <SPAssignmentCollection>] [-Default] [-Enabled] [<CommonParameters>]
```

## DESCRIPTION
The New-SPClaimProvider cmdlet registers a new claim provider in the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
New-SPClaimProvider -Name "MyClaimProvider" -Type "MyClaimProvider.Providers.CustomProvider" -Default
```

This example registers a claim provider to all Web applications and zones.

## PARAMETERS

### -AssemblyName

> Applicable: SharePoint Server Subscription Edition

The type must be a valid name of an assembly; for example, ClaimAssembly1.

Specifies the name of the assembly with the claim provider.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

> Applicable: SharePoint Server Subscription Edition

Specifies the description of the claim provider.

The type must be a valid name of an assembly; for example, ClaimAssembly1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName

> Applicable: SharePoint Server Subscription Edition

Specifies the display name of the new claim provider.

The type must be a valid name of a claim provider; for example, ClaimProvider1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type

> Applicable: SharePoint Server Subscription Edition

Specifies the type of the claim.

The type must be a valid name of a claim type; for example MyClaimProvider.Providers.CustomProvider.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
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

### -Default

> Applicable: SharePoint Server Subscription Edition

Specifies that the claim provider applies to all Web applications and zones.

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

### -Enabled

> Applicable: SharePoint Server Subscription Edition

Turns on the claim provider.

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
