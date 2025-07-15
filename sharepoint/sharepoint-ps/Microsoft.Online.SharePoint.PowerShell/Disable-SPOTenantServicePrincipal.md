---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/disable-spotenantserviceprincipal
applicable: SharePoint Online
title: Disable-SPOTenantServicePrincipal
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Disable-SPOTenantServicePrincipal

## SYNOPSIS

Disables the current tenant's "SharePoint Online Client" service principal.

## SYNTAX

```
Disable-SPOTenantServicePrincipal [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Disables the current tenant's "SharePoint Online Client" service principal.

When the service principal's account is disabled, clients and components that use this service principal
will not be able to request an access token for this service principal.

## EXAMPLES

### Example 1

```powershell
Disable-SPOTenantServicePrincipal
```

Disables the current tenant's "SharePoint Online Client" service principal.

## PARAMETERS

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
