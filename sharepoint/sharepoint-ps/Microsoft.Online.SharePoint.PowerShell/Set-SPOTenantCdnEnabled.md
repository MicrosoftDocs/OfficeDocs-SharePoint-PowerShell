---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/set-spotenantcdnenabled
applicable: SharePoint Online
title: Set-SPOTenantCdnEnabled
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Set-SPOTenantCdnEnabled

## SYNOPSIS

Enables or disables Public content delivery network (CDN) or Private CDN on the tenant level. Requires Tenant administrator permissions.

## SYNTAX

```
Set-SPOTenantCdnEnabled [-Enable <Boolean>] [-CdnType <SPOTenantCdnTypeClient>] [-NoDefaultOrigins] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Enables or disables Public content delivery network (CDN) or Private CDN on the tenant level.

## EXAMPLES

### EXAMPLE 1

```powershell
Set-SPOTenantCdnEnabled -CdnType public -Enable $true
```

The example enables a CDN.

## PARAMETERS

### -CdnType

> Applicable: SharePoint Online

Specifies the CDN type. The valid values are: public or private.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOTenantCdnTypeClient
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private, Both

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable

> Applicable: SharePoint Online

Specifies if the CDN is enabled.

The valid values are: $True and $False.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoDefaultOrigins

> Applicable: SharePoint Online

PARAMVALUE: SwitchParameter

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Online

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

> Applicable: SharePoint Online

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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Set-SPOTenantCdnEnabled](Set-SPOTenantCdnEnabled.md)
