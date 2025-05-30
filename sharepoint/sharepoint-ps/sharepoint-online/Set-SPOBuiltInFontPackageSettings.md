---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spobuiltinfontpackagesettings
applicable: SharePoint Online
title: Set-SPOBuiltInFontPackageSettings
schema: 2.0.0
author: Yixian15
ms.author: yixianpu
ms.reviewer:
---

# Set-SPOBuiltInFontPackageSettings

## SYNOPSIS

Use this cmdlet to set settings of [built-in font packages](/sharepoint/brand-center-font-packages).

## SYNTAX

```powershell
Set-SPOBuiltInFontPackageSettings [-HideBuiltInFontPackages] <Boolean>
```
## DESCRIPTION

Use this cmdlet to set settings of [built-in font packages](/sharepoint/brand-center-font-packages).

## EXAMPLES

### Example 1

```powershell
Set-SPOBuiltInFontPackageSettings -HideBuiltInFontPackages $true
```

This example sets the built-in font packages to be hidden from SharePoint sites.

## PARAMETERS

### -HideBuiltInFontPackages

Hide built in font packages from SharePoint sites if this value is true.

## RELATED LINKS

- [Get-SPOBuiltInFontPackageSettings](./Get-SPOBuiltInFontPackageSettings.md)