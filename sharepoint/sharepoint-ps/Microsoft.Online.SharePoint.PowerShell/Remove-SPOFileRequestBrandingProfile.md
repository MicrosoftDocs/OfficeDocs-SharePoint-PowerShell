---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spofilerequestbrandingprofile
applicable: SharePoint Online
title: Remove-SPOFileRequestBrandingProfile
author: nabeelnaiyer
ms.author: nabeelnaiyer
ms.reviewer:
manager: ahackett
schema: 2.0.0
ms.date: 07/28/2025
---

# Remove-SPOFileRequestBrandingProfile

## SYNOPSIS

Removes a branding profile (either primary or secondary) configured for the file request feature across the tenant.

## SYNTAX

```
Remove-SPOFileRequestBrandingProfile [-Primary] [-Secondary] 
[<CommonParameters>]
```

## DESCRIPTION

This cmdlet deletes either the primary or secondary branding profile associated with the file request feature. You must specify exactly one of the `-Primary` or `-Secondary` switches to indicate which profile to remove. If both switches are used or neither is specified, the cmdlet will throw an error.

> [!NOTE]
> If you remove the primary profile and a secondary profile exists, the secondary profile will automatically be promoted to primary. This ensures that the file request feature always has a primary branding profile if one is available.

## EXAMPLES

### Example 1

```powershell
Remove-SPOFileRequestBrandingProfile -Primary
```

This example removes the primary branding profile that was previously configured for file request pages in the tenant. If a secondary branding profile exists, it will automatically be promoted to primary after this command completes.

### Example 2

```powershell
Remove-SPOFileRequestBrandingProfile -Secondary
```

This example removes the secondary branding profile that was previously configured for file request pages in the tenant.

## PARAMETERS

### -Primary

Specifies the absolute URL of the asset library containing the branding assets.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Secondary

Specifies the relative URL of the logo image file.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-SPOFileRequestBrandingProfile](/powershell/module/sharepoint-online/add-spofilerequestbrandingprofile)

[Get-SPOFileRequestBrandingProfiles](/powershell/module/sharepoint-online/get-spofilerequestbrandingprofiles)

[Switch-SPOFileRequestBrandingProfiles](/powershell/module/sharepoint-online/switch-spofilerequestbrandingprofiles)
