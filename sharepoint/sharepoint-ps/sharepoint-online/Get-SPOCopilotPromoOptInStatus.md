---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Get-SPOCopilotPromoOptInStatus
applicable: SharePoint Online
title: Get-SPOCopilotPromoOptInStatus
schema: 
author: siruvanti
ms.author: siruvanti
ms.reviewer:
---

# Get-SPOCopilotPromoOptInStatus

## SYNOPSIS

Returns the Opt-In Copilot promo status for the tenant.

## SYNTAX
```powershell
Get-SPOCopilotPromoOptInStatus
```

## DESCRIPTION

This cmdlet returns the Opt-In Copilot promo status for the tenant.
If the promo status is enabled, the return value is `True`, otherwise the return value is `False`.

## EXAMPLES

### Example 1

```powershell
Get-SPOCopilotPromoOptInStatus
```

Example 1 returns the value of the Opt-In promo status.

## RELATED LINKS
- [Set-SPOCopilotPromoOptInStatus](./Set-SPOCopilotPromoOptInStatus.md)
- [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
