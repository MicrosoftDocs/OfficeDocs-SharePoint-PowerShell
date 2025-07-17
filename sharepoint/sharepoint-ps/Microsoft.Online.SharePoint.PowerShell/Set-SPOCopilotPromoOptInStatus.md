---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Set-SPOCopilotPromoOptInStatus
applicable: SharePoint Online
title: Set-SPOCopilotPromoOptInStatus
schema: 2.0.0
author: siruvanti
ms.author: siruvanti
ms.reviewer:
---
# Set-SPOCopilotPromoOptInStatus

## SYNOPSIS

Sets the Opt-In Copilot promo status for the tenant.

## SYNTAX

```
Set-SPOCopilotPromoOptInStatus -IsCopilotPromoStatusEnabled <Boolean> [<CommonParameters>]
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

> Applicable: SharePoint Online

Use this parameter to set Copilot opt-in promo status.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable,
-InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose,
-WarningAction, and -WarningVariable. For more information, see
[about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOCopilotPromoOptInStatus](./Get-SPOCopilotPromoOptInStatus.md)

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
