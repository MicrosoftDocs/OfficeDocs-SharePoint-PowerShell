Get-SPOCopilotPromoOptInStatus 
---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Get-SPOCopilotPromoOptInStatus
applicable: SharePoint Online
title: Get-SPOCopilotPromoOptInStatus.md
schema: 
author: swathi.iruvanti
ms.author: siruvanti
ms.reviewer:
---
# Get-SPOCopilotPromoOptInStatus

## SYNOPSIS

Returns the true or false Opt-In Copilot promo status 

## SYNTAX
```powershell
Get-SPOCopilotPromoOptInStatus
```

## DESCRIPTION

The `Get-SPOCopilotPromoOptInStatus` cmdlet retrieves and returns the opt-in Copilot promo status. The user must be a SharePoint Admin to run the cmlets.

## EXAMPLES

### Example 1

```powershell
Get-SPOCopilotPromoOptInStatusEnabled
true
```

Example 1: Success message shown to user when commandlet returns a positive flag from Tenant store

### Example 2

```powershell
Get-SPOCopilotPromoOptInStatusDisabled
False
```

Example 2: Success message shown to user when commandlet returns a negative flag from Tenant store

## RELATED LINKS

Set-SPOCopilotPromoOptInStatus
![image](https://github.com/user-attachments/assets/09e50724-88f0-4e26-8298-085d62c3bdbd)
