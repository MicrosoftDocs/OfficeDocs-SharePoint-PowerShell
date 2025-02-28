---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenantpreauthsettings
applicable: SharePoint Online
title: Get-SPOTenantPreAuthSettings
schema: 2.0.0
author: lw-msft
ms.author: laurenwong
ms.reviewer:
manager: bhaveshd
---

# Get-SPOTenantPreAuthSettings

## SYNOPSIS

Gets the configuration of pre-authentication.

## SYNTAX

```powershell
Get-SPOTenantPreAuthSettings [<CommonParameters>]
```

## DESCRIPTION

Gets the configuration of pre-authentication.

> [!NOTE]
> **What is pre-authentication?**
>
> SharePoint includes self-issued tokens in URLs called pre-authentication URLs (also known as tempauth URLs) to provide temporary access to a SharePoint resource, which helps support more rich user experiences. For example, a common scenario is downloading a file using a URL that includes a token in the `tempauth` query parameter like the following:
>
> `https://<tenant>.sharepoint.com/sites/samplesite/_layouts/15/download.aspx?UniqueId=<id>&tempauth=v1.ey...`
>
> But this feature is currently being deprecated. You can use the related [Set-SPOTenantPreAuthSettings](Set-SPOTenantPreAuthSettings.md) to control the use of pre-authentication in various use cases.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantPreAuthSettings
```

This example returns all the pre-authentication settings for the tenant as an object.

### EXAMPLE 2

```powershell
Get-SPOTenantPreAuthSettings | ConvertTo-Json
```

Gets all the pre-authentication settings for the tenant. Note that this example uses `ConvertTo-Json` to display the settings in JSON format since more complex Allow or Deny lists may be hard to read as an object.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

- [Set-SPOTenantPreAuthSettings](Set-SPOTenantPreAuthSettings.md)
- [Clear-SPOTenantPreAuthSettings](Clear-SPOTenantPreAuthSettings.md)
