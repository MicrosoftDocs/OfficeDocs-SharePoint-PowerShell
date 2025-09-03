---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/remove-spwopisuppressionsetting
applicable: SharePoint Server Subscription Edition
title: Remove-SPWOPISuppressionSetting
schema: 2.0.0
ms.date: 08/28/2025
---

# Remove-SPWOPISuppressionSetting

## SYNOPSIS
Removes the suppression settings for a file name extension or programmatic ID and action on the current SharePoint farm where this cmdlet is run.

## SYNTAX

### DocTypeAndAction
```
Remove-SPWOPISuppressionSetting [-Action <String>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-Extension <String>] [-ProgId <String>] [-WhatIf] [<CommonParameters>]
```

### Identity
```
Remove-SPWOPISuppressionSetting [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-Identity <String>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The `Remove-SPWOPISuppressionSetting` cmdlet removes the suppression settings for a file name extension or programmatic indentifier (ProgID) and action on the current SharePoint farm where this cmdlet is run.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Remove-SPWOPISuppressionSetting -Extension "XLSX" -Action "view"
```

This example removes suppression settings for viewing Excel workbooks that have the file name extension ".xlsx."

### EXAMPLE 2
```powershell
Get-SPWOPISuppressionSetting | Remove-SPWOPISuppressionSetting
```

This example removes all suppression settings on the current SharePoint farm where this cmdlet is run.

## PARAMETERS

### -Action

> Applicable: SharePoint Server Subscription Edition

Specifies the action for a given file name extension or programmatic identifier (ProgId).
For example, "view," "edit," and "embedview."

```yaml
Type: String
Parameter Sets: DocTypeAndAction
Aliases:

Required: False
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
If objects are not immediately used, or disposed of by using the `Stop-SPAssignment` command, an out-of-memory scenario can occur.

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
For more information, type the following command: `get-help about_commonparameters`.

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

### -Extension

> Applicable: SharePoint Server Subscription Edition

Specifies the file name extension.
Run `Get-SPWOPIBinding` to get the list of file name extensions the WOPI application supports.

```yaml
Type: String
Parameter Sets: DocTypeAndAction
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies a string that represents a SPWOPISuppressionSetting.
Run `Get-SPWOPISuppressionSetting` to see examples of such strings.

```yaml
Type: String
Parameter Sets: Identity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProgId

> Applicable: SharePoint Server Subscription Edition

Specifies the programmatic identifier (ProgID) for an application to suppress.
Run `Get-SPWOPIBinding` to get the list of ProgIDs that the WOPI application supports.

```yaml
Type: String
Parameter Sets: DocTypeAndAction
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

[New-SPWOPISuppressionSetting](New-SPWOPISuppressionSetting.md)

[Get-SPWOPISuppressionSetting](Get-SPWOPISuppressionSetting.md)
