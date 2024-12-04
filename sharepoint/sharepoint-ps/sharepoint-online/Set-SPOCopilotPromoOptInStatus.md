---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Set-SPOCopilotPromoOptInStatus
applicable: SharePoint Online
title: Set-SPOCopilotPromoOptInStatus
schema: 
author: siruvanti
ms.author: siruvanti
ms.reviewer:
---
# Set-SPOCopilotPromoOptInStatus

## SYNOPSIS

Sets the Opt-In Copilot promo status for the tenant.

## SYNTAX
```powershell
Set-SPOCopilotPromoOptInStatus -IsCopilotPromoStatusEnabled <Boolean>

```
## DESCRIPTION

This cmdlet sets the Opt-In Copilot promo status for the tenant to `True` or `False`. 

## EXAMPLES

### Example 1

```powershell
Set-SPOCopilotPromoOptInStatus -IsCopilotPromoStatusEnabled $true
```

Example 1 sets the Opt-In Copilot promo status for the tenant to `True`.

## PARAMETERS

### -IsCopilotPromoStatusEnabled

Use this parameter to set Copilot opt-in promo status. 

```yaml
Type: Boolean
Parameter Sets: 
Aliases:
Applicable: SharePoint Online

Required: True
Default value: None
```
## RELATED LINKS
- [Get-SPOCopilotPromoOptInStatus](./Get-SPOCopilotPromoOptInStatus.md)
- [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
