---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Get-SPOCopilotPromoUsage
applicable: SharePoint Online
title: Get-SPOCopilotPromoUsage
schema: 
author: arakesh
ms.author: arakesh
ms.reviewer:
---

# Get-SPOCopilotPromoUsage

## SYNOPSIS

Returns the count of SharePoint Agent promotion queries used by the tenant.

## SYNTAX
```powershell
Get-SPOCopilotPromoUsage
```

## DESCRIPTION

This cmdlet retrieves the number of SharePoint Agent promotion queries used by the tenant each month. 
It provides a monthly breakdown of query usage, helping admins track consumption of the promotion queries over time. 

## EXAMPLES

### Example 1

```powershell
Get-SPOCopilotPromoUsage
```

Example 1 returns SharePoint Agent promotion queries usage by month.

## RELATED LINKS
- [Get-SPOCopilotPromoOptInStatus](./Get-SPOCopilotPromoOptInStatus.md)
- [Set-SPOCopilotPromoOptInStatus](./Set-SPOCopilotPromoOptInStatus.md)
- [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
