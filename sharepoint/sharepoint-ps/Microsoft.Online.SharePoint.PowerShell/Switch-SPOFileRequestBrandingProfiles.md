---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/switch-spofilerequestbrandingprofiles
applicable: SharePoint Online
title: Switch-SPOFileRequestBrandingProfiles
author: nabeelnaiyer
ms.author: nabeelnaiyer
ms.reviewer:
manager: ahackett
schema: 2.0.0
---

# Switch-SPOFileRequestBrandingProfiles

## SYNOPSIS

Switches the primary and secondary file request branding profiles configured for the tenant.

## SYNTAX

```
Switch-SPOFileRequestBrandingProfiles [<CommonParameters>]
```

## DESCRIPTION

This cmdlet exchanges the current primary and secondary branding profiles used for the file request feature. This allows administrators to quickly change which profile is active without re-uploading or modifying assets. To use this cmdlet, both a primary and a secondary branding profile must already exist. The primary will become the secondary, and vice versa. If only one profile is present, the switch operation will fail.

## EXAMPLES

### Example 1

```powershell
Switch-SPOFileRequestBrandingProfiles
```

This example switches the current primary and secondary branding profiles used for file request pages. After running this command, the existing secondary profile will become the new primary, and the current primary will become secondary.

## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-SPOFileRequestBrandingProfile](/powershell/module/microsoft.online.sharepoint.powershell/add-spofilerequestbrandingprofile)

[Get-SPOFileRequestBrandingProfiles](/powershell/module/microsoft.online.sharepoint.powershell/get-spofilerequestbrandingprofiles)

[Remove-SPOFileRequestBrandingProfile](/powershell/module/microsoft.online.sharepoint.powershell/remove-spofilerequestbrandingprofile)
