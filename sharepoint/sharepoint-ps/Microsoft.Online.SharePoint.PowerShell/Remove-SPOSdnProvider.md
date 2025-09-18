---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/remove-sposdnprovider
applicable: SharePoint Online
title: Remove-SPOSdnProvider
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Remove-SPOSdnProvider

## SYNOPSIS

Removes Software-Defined Networking (SDN) Support in your SharePoint Online tenant

## SYNTAX

```
Remove-SPOSdnProvider [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Removes SDN Support in your SharePoint Online tenant

## EXAMPLES

### EXAMPLE 1

```yaml
Remove-SPOSdnProvider -Confirm:false
```

This command removes the SDN support for your Online Tenant without confirmation.

### EXAMPLE 2

```yaml
Remove-SPOSdnProvider -Confirm:true -WhatIf
```

This command will prompt for a confirmation before "simulating" that it will remove the support for SDN in the current SPO tenant (-WhatIf)

## PARAMETERS

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

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[New-SPOSdnProvider](New-SPOSdnProvider.md)
