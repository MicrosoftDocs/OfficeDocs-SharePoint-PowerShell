---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenantpreauthsettings
applicable: SharePoint Online
title: Get-SPOTenantPreAuthSettings
schema: 2.0.0
author: lw-msft
ms.author: laurenwong, neilh
ms.reviewer:
manager: bhaveshd
---

# Get-SPOTenantPreAuthSettings

## SYNOPSIS

Gets the configuration of Pre-Authentication.

## SYNTAX

```powershell
Get-SPOTenantPreAuthSettings [<CommonParameters>]
```

## DESCRIPTION

Gets the configuration of Pre-Authentication.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantPreAuthSettings
```

This example returns all the PreAuthentication settings for the tenant as an object.

**Example Output**:

```powershell
IsDisabled AllowList 
---------- ----------
True       {{Id: 1cddb994-de09-4ebd-b401-5d68ea148252, IncludedApps: [00000000-0000-0000-0000-000000000000], Exclude... 
```

### EXAMPLE 2

```powershell
Get-SPOTenantPreAuthSettings | ConvertTo-Json
```

Gets all the pre auth settings for the tenant. Note that this example uses `ConvertTo-Json` to display the settings in JSON format since more complex Allow or Deny lists may be hard to read as an object.

**Example Output**:

```powershell
{ 
  "IsDisabled":  true, 
  "AllowList":  [
    {
      "Id":  "1cddb994-de09-4ebd-b401-5d68ea148252", 
      "IncludedApps":  "00000000-0000-0000-0000-000000000000", 
      "ExcludedApps":  "", 
      "IncludedFeatures":  "", 
      "ExcludedFeatures":  "Download, WebRenderingEmbed" 
    }
  ], 
  "DenyList":  [

  ] 
} 
```

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

- [Set-SPOTenantPreAuthSettings](Set-SPOTenantPreAuthSettings.md)
- [Clear-SPOTenantPreAuthSettings](Clear-SPOTenantPreAuthSettings.md)
