---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spwopisuppressionsetting
applicable: SharePoint Server Subscription Edition
title: Get-SPWOPISuppressionSetting
schema: 2.0.0
---

# Get-SPWOPISuppressionSetting

## SYNOPSIS

Returns the suppression settings on the current SharePoint farm where this cmdlet is run.


## SYNTAX

```
Get-SPWOPISuppressionSetting [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
The Get-SPWOPISuppressionSetting cmdlet returns the suppression settings on the current SharePoint farm where this cmdlet is run.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Get-SPWOPISuppressionSetting
```

This example returns all the suppression settings on the current SharePoint farm where this cmdlet is run.
The suppression settings returned include the DocType and WOPIAction.

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Content roadmap for Office Web Apps]()

[Use Office Web Apps with SharePoint 2013]()

[New-SPWOPISuppressionSetting](New-SPWOPISuppressionSetting.md)

[Remove-SPWOPISuppressionSetting](Remove-SPWOPISuppressionSetting.md)
