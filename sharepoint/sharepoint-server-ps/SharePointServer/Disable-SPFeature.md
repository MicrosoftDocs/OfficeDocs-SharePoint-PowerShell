---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/disable-spfeature
applicable: SharePoint Server Subscription Edition
title: Disable-SPFeature
schema: 2.0.0
---

# Disable-SPFeature

## SYNOPSIS

Disables an installed SharePoint Feature at a given scope.


## SYNTAX

```
Disable-SPFeature [-Identity] <SPFeatureDefinitionPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-Force] [-Url <String>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The Disable-SPFeature cmdlet disables a SharePoint Feature at the given scope.
If the scope of the Feature is the farm, the URL is not needed.
Otherwise, provide the URL at which this Feature is to be deactivated (explicit scope is not needed).

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Disable-SPFeature -identity "MyCustom" -URL https://somesite
```

This example disables the "MyCustom" Web site scoped feature at   https://somesite.

### EXAMPLE 2
```powershell
$w = Get-SPWeb https://somesite/myweb | ForEach{ $_.URL }
Get-SPFeature -Web $w | ForEach-Object { Disable-SPFeature -Identity $_ -URL $w}
```

This example disables all features in the subsite at https://somesite/myweb.

You do not need to use the SPAssignment cmdlets in this case because the Web object is not stored -- only the string value for the URL.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the Feature or GUID to disable.

The type must be the name of the Feature folder located in the "$env:ProgramFiles\Common Files\Microsoft Shared\Web Server Extensions\[14|15|16]\Template\Features" folder or GUID, in the format 21d186e1-7036-4092-a825-0eb6709e9281.

```yaml
Type: SPFeatureDefinitionPipeBind
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

### -Force

> Applicable: SharePoint Server Subscription Edition

Forces a Feature to be disabled.

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

### -Url

> Applicable: SharePoint Server Subscription Edition

Specifies the URL of the Web application, site collection, or Web site to which the Feature is being disabled.

The type must be a valid URL, such as https://server_name.

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
