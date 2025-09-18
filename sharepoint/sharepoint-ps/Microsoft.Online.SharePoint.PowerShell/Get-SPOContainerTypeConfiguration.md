---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/Get-SPOContainertypeConfiguration
applicable: SharePoint Online
title: Get-SPOContainerTypeConfiguration
schema: 2.0.0
author: FarreltinF
ms.author: fanyi
ms.reviewer:
---

# Get-SPOContainerTypeConfiguration

## SYNOPSIS

Use this cmdlet to read the configuration values set on the container type.

## SYNTAX

```
Get-SPOContainerTypeConfiguration -ContainerTypeId <Guid> [<CommonParameters>]
```

## DESCRIPTION

The `Get-SPOContainerTypeConfiguration` cmdlet retrieves and returns configuration settings set on a container type created under a SharePoint Embedded application. This can either be the default value or the previously set value on the container type.

You must be a SharePoint Embedded Administrator to run this cmdlet.

## EXAMPLES

### Example 1

```powershell
Get-SPOContainerTypeConfiguration -ContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604e4
```

This example returns a list of configurations set on a container type '4f0af585-8dcc-0000-223d-661eb2c604e4'.

## PARAMETERS

### -ContainerTypeId

> Applicable: SharePoint Online

This parameter specifies the ID of the SharePoint Embedded container type. Use the `Get-SPOContainerType` command to retrieve the ContainerTypeId.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Set-SPOContainerTypeConfiguration](Set-SPOContainerTypeConfiguration.md)

