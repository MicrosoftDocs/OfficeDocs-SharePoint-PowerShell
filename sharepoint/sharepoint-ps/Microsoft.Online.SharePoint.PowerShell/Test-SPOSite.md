---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/test-sposite
applicable: SharePoint Online
title: Test-SPOSite
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Test-SPOSite

## SYNOPSIS

Tests a SharePoint Online site collection.

## SYNTAX

```
Test-SPOSite -Identity <SpoSitePipeBind> [-RuleId <Guid>] [-RunAlways] [<CommonParameters>]
```

## DESCRIPTION

The `Test-SPOSite` cmdlet runs one or all site collection health checks on the site collection and its contents.
Tests are intended not to make any changes except in repair mode, which can be initiated by running the `Repair-SPOSite` cmdlet.
This cmdlet reports the rules together with a summary of the results.

You must be at least a SharePoint administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
Test-SPOSite https://contoso.sharepoint.com/sites/marketing
```

This example runs all the site collection health checks on the <https://contoso.sharepoint.com/sites/marketing> site collection.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the SharePoint Online site collection to test.

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

Specifies the health check rule to run.

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

Forces a rule to run even if a health check was run.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Get-SPOSite](Get-SPOSite.md)

[New-SPOSite](New-SPOSite.md)

[Repair-SPOSite](Repair-SPOSite.md)
