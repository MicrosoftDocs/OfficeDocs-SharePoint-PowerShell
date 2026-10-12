---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositerestrictedappaccesscontrol
applicable: SharePoint Online
title: Get-SPOSiteRestrictedAppAccessControl
schema: 2.0.0
ms.author: neilh
ms.reviewer: neilh
description: Learn how to use Get-SPOSiteRestrictedAppAccessControl to read a SharePoint site's App Restrictions policy and check enforcement status with PowerShell.
ms.date: 10/12/2026
ms.topic: reference
---

# Get-SPOSiteRestrictedAppAccessControl

## SYNOPSIS

Returns the complete site-level App Restrictions policy for a site, including enablement, active mode, and both the allow list and the deny list.

## SYNTAX

```
Get-SPOSiteRestrictedAppAccessControl [-Identity] <String> [<CommonParameters>]
```

## DESCRIPTION

Use the `Get-SPOSiteRestrictedAppAccessControl` cmdlet to read the complete Restricted App Access Control policy stored for a single site.

App Restrictions adds a SharePoint authorization boundary for applications that already have Microsoft Entra consent and SharePoint permissions. It never grants permissions and it doesn't replace Entra consent. A request must pass both the existing permission model and App Restrictions.

A site policy has four parts:

- **Enabled** - whether site enforcement is turned on. Site enforcement is turned on only by `Enable-SPOSiteRestrictedAppAccessControl`. Mode and list changes are configuration-only and preserve the current enablement state.
- **Mode** - the active mode. When the mode is `Allow`, applications in the allow list are allowed and all other governed apps are denied. When the mode is `Deny`, applications in the deny list are denied and all other governed apps are allowed. `Allow` is the default mode when a site is enabled without existing configuration.
- **AllowList** - the persistent list used when the mode is `Allow`.
- **DenyList** - the persistent l
