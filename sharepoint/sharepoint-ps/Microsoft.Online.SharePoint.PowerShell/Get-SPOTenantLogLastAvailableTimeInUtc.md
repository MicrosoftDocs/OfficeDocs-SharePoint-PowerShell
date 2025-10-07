---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spotenantloglastavailabletimeinutc
applicable: SharePoint Online
title: Get-SPOTenantLogLastAvailableTimeInUtc
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Get-SPOTenantLogLastAvailableTimeInUtc

## SYNOPSIS

Returns the most recent time when the SharePoint Online organization logs were collected.

## SYNTAX

```
Get-SPOTenantLogLastAvailableTimeInUtc [<CommonParameters>]
```

## DESCRIPTION

This cmdlet retrieves the time in Coordinated Universal Time (UTC) when the logs were last collected.
After you know the time, you can use the `Get-SPOTenantLogEntry` cmdlet to retrieve the logs.

You must be at least a SharePoint Online administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantLogLastAvailableTimeInUtc
```

This example returns the time in UTC when the SharePoint Online organization logs were most recently collected.

## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Get-SPOTenantLogEntry](Get-SPOTenantLogEntry.md)
