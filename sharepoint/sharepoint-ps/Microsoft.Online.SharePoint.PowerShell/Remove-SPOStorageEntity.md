---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spostorageentity
applicable: SharePoint Online
title: Remove-SPOStorageEntity
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Remove-SPOStorageEntity

## SYNOPSIS

Tenant properties allow tenant administrators to add properties in the app catalog that can be read by various SharePoint Framework components. Because tenant properties are stored in the tenant app catalog, you must provide the tenant app catalog site collection URL or the site collection app catalog URL in the following cmdlets.
This cmdlet is used to remove a value in the property bag.

## SYNTAX

```
Remove-SPOStorageEntity [-Site] <SpoSitePipeBind> [-Key] <String> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a value within the property bag.

## EXAMPLES

### Example 1

```powershell
Remove-SPOStorageEntity "https://tenant-name.sharepoint.com/sites/app-catalog" -Key "MyCustomValue"
```

This example removes the value of my custom value.

## PARAMETERS

### -Key

The key in the property bag that should be removed.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Site

URL to the tenant or site collection app catalog.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
