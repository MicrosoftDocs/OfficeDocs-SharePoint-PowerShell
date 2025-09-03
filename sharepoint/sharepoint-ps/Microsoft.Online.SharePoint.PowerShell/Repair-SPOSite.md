---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/repair-sposite
applicable: SharePoint Online
title: Repair-SPOSite
schema: 2.0.0
author: trent-green
ms.author: speedta
ms.reviewer:
---

# Repair-SPOSite

## SYNOPSIS

Checks and repairs the site collection and its contents.

## SYNTAX

```
Repair-SPOSite -Identity <SpoSitePipeBind> [-RuleId <Guid>] [-RunAlways] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The `Repair-SPOSite` cmdlet runs one or all site collection health checks on the site collection and its contents.
This cmdlet will make changes if issues are found and automatically repairable.

The cmdlet reports the health check rules with a summary of the results.
The rules might not support automatic repair.
Tests without repair mode can be initiated by running the `Test-SPOSite` cmdlet.

You must be at least a SharePoint administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
Repair-SPOSite https://contoso.sharepoint.com/sites/marketing
```

This example runs all the site collection health checks in repair mode on the <https://contoso.sharepoint.com/sites/marketing> site collection.

### EXAMPLE 2

```powershell
Repair-SPOSite https://contoso.sharepoint.com/sites/marketing -RuleID "ee967197-ccbe-4c00-88e4-e6fab81145e1"
```

This example runs the Missing Galleries Check rule in repair mode on the <https://contoso.sharepoint.com/sites/marketing> site collection.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the SharePoint Online site collection on which to run the repairs.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RuleId

> Applicable: SharePoint Online

Specifies a health check rule to run.

For example:

- "ee967197-ccbe-4c00-88e4-e6fab81145e1" for Missing Galeries.
- "befe203b-a8c0-48c2-b5f0-27c10f9e1622" for Conflicting Content Types.
- "a9a6769f-7289-4b9f-ae7f-5db4b997d284" for Missing Parent Content Types.
- "5258ccf5-e7d6-4df7-b8ae-12fcc0513ebd" for Missing Site Templates.
- "99c946f7-5751-417c-89d3-b9c8bb2d1f66" for Unsupported Language Pack References.
- "6da06aab-c539-4e0d-b111-b1da4408859a" for Unsupported MUI References.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunAlways

> Applicable: SharePoint Online

Displays a message that explains the effect of the command instead of executing the command.

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

Prompts you for confirmation before running the cmdlet.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Test-SPOSite](Test-SPOSite.md)
