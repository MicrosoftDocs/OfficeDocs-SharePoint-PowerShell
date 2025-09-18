---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/set-spostorageentity
applicable: SharePoint Online
title: Set-SPOStorageEntity
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Set-SPOStorageEntity

## SYNOPSIS

Tenant properties allow tenant administrators to add properties in the app catalog that can be read by various SharePoint Framework components. Because tenant properties are stored in the tenant app catalog, you must provide the tenant app catalog site collection URL or the site collection app catalog URL in the following cmdlets.

## SYNTAX

```
Set-SPOStorageEntity -Site <SpoSitePipeBind> -Key <String> -Value <String> -Comments <String>
 -Description <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet is used to set a value in the property bag.

## EXAMPLES

### Example 1

```powershell
Set-SPOStorageEntity -Site "https://tenant-name.sharepoint.com/sites/app-catalog"  -Key "MyCustomKey" -Value "{'MyKey':1234}" -Comments "This is an example" -Description "This is an example"
```

This example adds an entry to the property bag.

## PARAMETERS

### -Comments

> Applicable: SharePoint Online

Comment for this property bag entry.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

> Applicable: SharePoint Online

Description of the property.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Key

> Applicable: SharePoint Online

The key in the property bag that should be added or updated.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site

> Applicable: SharePoint Online

URL to the tenant or site collection app catalog.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value

> Applicable: SharePoint Online

Value to be set.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
