---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositedesignrights
applicable: SharePoint Online
title: Get-SPOSiteDesignRights
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOSiteDesignRights

## SYNOPSIS

Displays a list of principals and their rights for usage of the site design. This can be used to determine the scope that your site design has with users on the tenant.

## SYNTAX

```powershell
Get-SPOSiteDesignRights  [-Identity] <SPOSiteDesignPipeBind>  [<CommonParameters>]
```

## DESCRIPTION

Displays a list of principals and their rights for usage of the site design. This can be used to determine the scope that your site design has with users on the tenant.

## EXAMPLES

### Example 1

This example gets the rights for a site design.

```powershell
Get-SPOSiteDesignRights 607aed52-6d61-490a-b692-c0f58a6981a1

DisplayName  PrincipalName                                      Rights
-----------  -------------                                      ------
Nestor Wilke i:0#.f|membership|nestorw@contoso.onmicrosoft.com   View
```

## PARAMETERS

### -Identity

The ID of the site design to get scoping information.

```yaml
Type: SPOSiteDesignPipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
