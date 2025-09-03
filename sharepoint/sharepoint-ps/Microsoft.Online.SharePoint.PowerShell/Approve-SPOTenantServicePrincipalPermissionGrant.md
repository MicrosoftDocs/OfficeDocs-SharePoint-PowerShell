---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/approve-spotenantserviceprincipalpermissiongrant
applicable: SharePoint Online
title: Approve-SPOTenantServicePrincipalPermissionGrant
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
ms.date: 07/16/2025
---

# Approve-SPOTenantServicePrincipalPermissionGrant

## SYNOPSIS

Approves a permission request for the current tenant's "SharePoint Online Client" service principal.

## SYNTAX

```
Approve-SPOTenantServicePrincipalPermissionGrant [-Resource] <String> [-Scope] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Adds a permission for the current tenant's "SharePoint Online Client" service principal. Can be used to add needed permissions to the service principal without specifically requesting them in the SharePoint Framework solution file (sppkg).

## EXAMPLES

### EXAMPLE 1

```powershell
Approve-SPOTenantServicePrincipalPermissionGrant -Resource "Microsoft Graph" -Scope "Mail.Read"
```

Adds a permission scope for the 'Microsoft Graph' resource with scope claim 'Mail.Read'.

## PARAMETERS

### -Resource

> Applicable: SharePoint Online

Resource of the permission request to add.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope

> Applicable: SharePoint Online

Scope of the permission request to add.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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
