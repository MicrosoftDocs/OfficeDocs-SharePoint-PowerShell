---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenanttempauthsettings
applicable: SharePoint Online
title: Get-SPOTenantTempAuthSettings
schema: 2.0.0
author: lw-msft
ms.author: laurenwong
ms.reviewer:
manager: bhaveshd
---

# Get-SPOTenantTempAuthSettings

## SYNOPSIS

Gets the temp auth settings for the tenant.

## SYNTAX

```powershell
Get-SPOTenantTempAuthSettings [<CommonParameters>]
```

## DESCRIPTION

Gets the temp auth settings for the tenant, including whether temp auth is disabled for the tenant overall, the allow list, and the deny list.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantTempAuthSettings | ConvertTo-Json
```

Gets all the temp auth settings for the tenant. Note that this example uses `ConvertTo-Json` to display the settings in JSON format since more complex Allow or Deny lists may be harder to read as an object.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Set-SPOTenantTempAuthSettings](Set-SPOTenantTempAuthSettings.md)
