---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Set-SPOCopilotPromoOptInStatus
applicable: SharePoint Online
title: Set-SPOCopilotPromoOptInStatus.md
schema: 
author: swathi.iruvanti
ms.author: siruvanti
ms.reviewer:
---
# Set-SPOCopilotPromoOptInStatus

## SYNOPSIS

Retrieves the IsCopilotPromoStatusEnabled ( "true/false" ) state of the Copilot promo opt-in bit and stores the information.

## SYNTAX
```powershell
Set-SPOCopilotPromoOptInStatus
```

### Parameters:

The following details are returned:

- Copilot promo status set successfully, returns nothing if successful. 

- Copilot promo status set failed, returns an error. 

## DESCRIPTION

The `Set-SPOCopilotPromoOptInStatus` cmdlet stores the opt-in state. The user must be a SharePoint Admin to run the cmlets.


## EXAMPLES

### Example 1

```powershell
Set-SPOCopilotPromoOptInStatusSetSuccessfully -SPOCopilotPromoOptInStatusEnabled true
```

Example 1: No success message returned, can validate by executing Get-SPOCopilotPromoOptInStatus.
If commandlet fails to execute for Set-CopilotPromoOptInStatus, an error message is shown to user.

### Example 2

```powershell
Set-SPOCopilotPromoOptInStatusSetSuccessfully -SPOCopilotPromoOptInStatusDisabled false
```

Example 2: Success message shown to user when commandlet executes successfully for Set-CopilotPromoOptInStatus
If commandlet fails to execute for Set-CopilotPromoOptInStatus, an error message is shown to user.


## RELATED LINKS

Get-SPOCopilotPromoOptInStatus
