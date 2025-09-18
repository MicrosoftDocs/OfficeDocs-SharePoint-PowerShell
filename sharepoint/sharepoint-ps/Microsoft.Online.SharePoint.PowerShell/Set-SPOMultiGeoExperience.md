---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/set-spomultigeoexperience
applicable: SharePoint Online
title: Set-SPOMultiGeoExperience
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Set-SPOMultiGeoExperience

## SYNOPSIS

Used to set a geo location into SPO mode.

## SYNTAX

```
Set-SPOMultiGeoExperience [-AllInstances] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to set a geo location into SPO mode. This upgrade action is not reversible. For more information see [Enabling SharePoint Multi-Geo in your satellite geo location](/office365/enterprise/enabling-sp-multigeo-satellite-geolocation)

## EXAMPLES

### Example 1

```powershell
Set-SPOMultiGeoExperience
```

This example will upgrade your instance's multi-geo experience to include SharePoint Online Multi-Geo. This operation usually takes about an hour while we perform various publish backs in the service and re-stamp your tenant.

## PARAMETERS

### -AllInstances

> Applicable: SharePoint Online

.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Online
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
