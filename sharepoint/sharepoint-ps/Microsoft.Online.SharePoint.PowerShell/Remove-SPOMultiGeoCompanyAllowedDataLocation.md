---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spomultigeocompanyalloweddatalocation
applicable: SharePoint Online
title: Remove-SPOMultiGeoCompanyAllowedDataLocation
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
ms.date: 07/15/2025
---

# Remove-SPOMultiGeoCompanyAllowedDataLocation

## SYNOPSIS

Use this cmdlet to remove a multi geo allowed location.

## SYNTAX

```
Remove-SPOMultiGeoCompanyAllowedDataLocation [-Location] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Removes a specified multi-geo location that was previously allowed by [Set-SPOMultiGeoCompanyAllowedDataLocation](Set-SPOMultiGeoCompanyAllowedDataLocation.md).

## EXAMPLES

### Example 1

```powershell
Remove-SPOMultiGeoCompanyAllowedDataLocation -Location AUS
```
Removes AUS (Australia) as an allowed mutli-geo location.

## PARAMETERS

### -Location

> Applicable: SharePoint Online

The Preferred Data Location (PDL) to remove.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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

[Set-SPOMultiGeoCompanyAllowedDataLocation](Set-SPOMultiGeoCompanyAllowedDataLocation.md)
