---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Get-SPOCopilotPromoUsage
applicable: SharePoint Online
title: Get-SPOCopilotPromoUsage
schema: 2.0.0
author: arakesh
ms.author: arakesh
ms.reviewer:
---

# Get-SPOCopilotPromoUsage

## SYNOPSIS

Returns the count of SharePoint Agent promotion queries used by the tenant.

## SYNTAX

```
Get-SPOCopilotPromoUsage [<CommonParameters>]
```

## DESCRIPTION

This cmdlet retrieves the number of SharePoint Agent promotion queries used by the tenant each month, starting the month tenant qualified for trial.
It provides a monthly breakdown of query usage, helping admins track consumption of the promotion queries over time.

## EXAMPLES

### Example 1

```powershell
Get-SPOCopilotPromoUsage
```

Example 1 returns SharePoint Agent promotion queries usage by month.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOCopilotPromoOptInStatus](./Get-SPOCopilotPromoOptInStatus.md)

[Set-SPOCopilotPromoOptInStatus](./Set-SPOCopilotPromoOptInStatus.md)

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
