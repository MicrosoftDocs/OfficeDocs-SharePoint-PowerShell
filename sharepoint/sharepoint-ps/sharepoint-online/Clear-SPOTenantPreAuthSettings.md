---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/clear-spotenantpreauthsettings
applicable: SharePoint Online
title: Clear-SPOTenantPreAuthSettings
schema: 2.0.0
author: lw-msft
ms.author: laurenwong
ms.reviewer:
manager: bhaveshd
---

# Clear-SPOTenantPreAuthSettings

## SYNOPSIS

Clears the pre-authentication settings for either the allow or deny list. 

## SYNTAX

```powershell
Clear-SPOTenantPreAuthSettings -Type <TenantPreAuthSettingsListType> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Clears the pre-authentication settings for either the allow or deny list.

> [!NOTE]
> **What is pre-authentication?**
> 
> SharePoint includes self-issued tokens in URLs called pre-authentication URLs (also known as tempauth URLs) to provide temporary access to a SharePoint resource, which helps support more rich user experiences. For example, a common scenario is downloading a file using a URL that includes a token in the `tempauth` query parameter like the following:
>
> `https://<tenant>.sharepoint.com/sites/samplesite/_layouts/15/download.aspx?UniqueId=<id>&tempauth=v1.ey...`
>
> This feature is currently being deprecated and you can use the related [Set-SPOTenantPreAuthSettings](Set-SPOTenantPreAuthSettings.md) to control the use of pre-authentication in various use cases.

## EXAMPLES

### Example 1
```powershell
Clear-SPOTenantPreAuthSettings –Type Allow
```

This example clears all list items from the allow list.

### Example 2

```powershell
Clear-SPOTenantPreAuthSettings –Type Deny 
```

This example clears all list items from the deny list. 

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type

This parameter indicates whether the cmdlet is interacting with the allow list or the deny list.

```yaml
Type: TenantPreAuthSettingsListType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-5.1).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

- [Get-SPOTenantPreAuthSettings](Get-SPOTenantPreAuthSettings.md)
- [Set-SPOTenantPreAuthSettings](Set-SPOTenantPreAuthSettings.md)
