---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/set-spobuiltindesignpackagevisibility
applicable: SharePoint Online
title: Set-SPOBuiltInDesignPackageVisibility
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Set-SPOBuiltInDesignPackageVisibility

## SYNOPSIS

Sets the visibility of the available built-in Design Packages at moment of site creation.

## SYNTAX

```
Set-SPOBuiltInDesignPackageVisibility -IsVisible <Boolean> -DesignPackage <DesignPackageType>
 [<CommonParameters>]
```

## DESCRIPTION

Sets the visibility of the available built-in Design Packages. For more information, see [Moving from Publishing sites to Communication sites](/sharepoint/publishing-sites-classic-to-modern-experience)

## EXAMPLES

### Example 1

```powershell
Set-SPOBuiltInDesignPackageVisibility -DesignPackage Showcase -IsVisible:$false
```

This example sets the visibility of Showcase design package to false.

## PARAMETERS

### -DesignPackage

Name of the design package, available names are
- Topic
- Showcase
- Blank
- TeamSite

```yaml
Type: Microsoft.SharePoint.Administration.DesignPackageType
Parameter Sets: (All)
Aliases:
Accepted values: None, Topic, Showcase, Blank, TeamSite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsVisible

Determines if the design package is visible

```yaml
Type: System.Boolean
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
