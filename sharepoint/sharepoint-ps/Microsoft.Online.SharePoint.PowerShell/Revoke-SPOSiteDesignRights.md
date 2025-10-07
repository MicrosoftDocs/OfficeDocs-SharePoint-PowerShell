---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/revoke-spositedesignrights
applicable: SharePoint Online
title: Revoke-SPOSiteDesignRights
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Revoke-SPOSiteDesignRights

## SYNOPSIS

Revokes rights for specified principals from a site design.

## SYNTAX

```
Revoke-SPOSiteDesignRights [-Identity] <SPOSiteDesignPipeBind> -Principals <String[]> [<CommonParameters>]
```

## DESCRIPTION

Revokes rights for specified principals from a site design.

## EXAMPLES

### Example 1

This example shows how to revoke rights to a site design for Nestor.

```powershell
Revoke-SPOSiteDesignRights 44252d09-62c4-4913-9eb0-a2a8b8d7f863 `
   -Principals "nestorw@contoso.onmicrosoft.com"
```

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

The ID of the site design from which to revoke rights.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Principals

> Applicable: SharePoint Online

One or more principals to revoke rights on the specified site design.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
