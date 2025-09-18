---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/import-spapppackage
applicable: SharePoint Server Subscription Edition
title: Import-SPAppPackage
schema: 2.0.0
---

# Import-SPAppPackage

## SYNOPSIS

Imports an app package.

## SYNTAX

```
Import-SPAppPackage -Path <String> -Source <SPAppSource> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-WhatIf] [-AssetId <String>] [-ContentMarket <String>] -Site <SPSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION
Use the Import-SPAppPackage cmdlet to import an app package from the content database and create an app inside the site collection by using the SiteCollection parameter.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Import-SPAppPackage -Path .\feature-upgrade-v1.spapp -Site https://localhost -Source ([microsoft.sharepoint.administration.spappsource]::ObjectModel)
```

This example imports an app package.

## PARAMETERS

### -Path

> Applicable: SharePoint Server Subscription Edition

Specifies the path of the input file.

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

### -Source

> Applicable: SharePoint Server Subscription Edition

Defines the source of the app. The source indicates where the app package originates from, for example, if the app was built by a developer but did not reside on the SharePoint Marketplace, you might use the CorporateCatalog source.

The following are valid values:

InvalidSource, Marketplace, CorporateCatalog, DeveloperSite, ObjectModel, RemoteObjectModel

The following are valid sources (not parameters of -Source) of the app:

--SharePoint Store (Marketplace)

--App catalog (CorporateCatalog)

--SharePointService - Indicates apps that were built in place with SharePoint features, for example Access Services (ObjectModel)

```yaml
Type: SPAppSource
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

### -AssetId

> Applicable: SharePoint Server Subscription Edition

Specifies the Asset Id to import.

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

### -ContentMarket

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the content market.

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

### -Site

> Applicable: SharePoint Server Subscription Edition

Specifies the SPSite object to import.

```yaml
Type: SPSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
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

[Export-SPAppPackage](Export-SPAppPackage.md)
