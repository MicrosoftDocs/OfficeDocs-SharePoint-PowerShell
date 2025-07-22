---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spoorgassetslibrary
applicable: SharePoint Online
title: Remove-SPOOrgAssetsLibrary
author: Maralesfahanpoor
ms.author: maesfaha
ms.reviewer:
manager: paulac
schema: 2.0.0
---

# Remove-SPOOrgAssetsLibrary

## SYNOPSIS

Removes a library that was designated as a central location for organization assets across the tenant.

## SYNTAX

### RemoveLibrary (Default)
```
Remove-SPOOrgAssetsLibrary [-LibraryUrl <String>] [-ListId <Guid>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BrandCenter
```
Remove-SPOOrgAssetsLibrary [-BrandCenter] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The Remove-SPOOrgAssetsLibrary cmdlet removes a library that was designated as a central location for organization assets across the tenant. Once this cmdlet is run, this library will no longer be accessible from the "Your organization" tab in the file picker (it might take up to 24 hours before the change applies). When running the cmdlet, either the library URL or library ID (not both) needs to be indicated.

When used with the `-BrandCenter` parameter, this cmdlet removes Brand Center related organization assets libraries and deactivates Brand Center features for the tenant.

Once the library is removed, CDN will still be enabled for this library. To disable CDN for this library, use Remove-SPOTenantCdnOrigin with the server relative URL (example: /sites/branding/assets).

## EXAMPLES

### Example 1

This example removes https://contoso.sharepoint.com/sites/branding/Assets as a designated library using the library ID. Assets within this library will no longer be accessible from the "Your organization" tab in the file picker.

```powershell
Remove-SPOOrgAssetsLibrary -ListId 58454454-6546-6466-9769-646464623988
```

### Example 2

This example removes Brand Center related organization assets libraries and deactivates Brand Center features for the tenant.

```powershell
Remove-SPOOrgAssetsLibrary -BrandCenter
```

## PARAMETERS

### -LibraryUrl

> Applicable: SharePoint Online

Indicates the server relative URL of the library to be removed as a central location for organization assets.

```yaml
Type: System.String
Parameter Sets: RemoveLibrary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListId

> Applicable: SharePoint Online

Indicates the library ID for the library to be removed as a central location for organization assets.

```yaml
Type: System.Guid
Parameter Sets: RemoveLibrary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BrandCenter

> Applicable: SharePoint Online

Deactivates Brand Center features for the tenant.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BrandCenter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/add-spoorgassetslibrary)

[Set-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/set-spoorgassetslibrary)

[Get-SPOOrgAssetsLibrary](/powershell/module/sharepoint-online/get-spoorgassetslibrary)
