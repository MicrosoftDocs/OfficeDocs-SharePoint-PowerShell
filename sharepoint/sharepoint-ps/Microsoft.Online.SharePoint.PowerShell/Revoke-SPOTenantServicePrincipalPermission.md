---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/revoke-spotenantserviceprincipalpermission
applicable: SharePoint Online
title: Revoke-SPOTenantServicePrincipalPermission
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---
# Revoke-SPOTenantServicePrincipalPermission

## SYNOPSIS

Revokes a permission that was previously granted to the "SharePoint Online Client" service principal

## SYNTAX

```
Revoke-SPOTenantServicePrincipalPermission -ObjectId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Revokes a permission that was previously granted to the "SharePoint Online Client" service principal.

## EXAMPLES

### EXAMPLE 1

```powershell
$grants = Get-SPOTenantServicePrincipalPermissionGrants
$grantToRemove = $grants | ? { $_.Resource -eq 'Office 365 SharePoint Online' -and $_.Scope -eq 'MyFiles.Read' } | Select-Object -First 1

if ($grantToRemove -ne $null)
{
    Revoke-SPOTenantServicePrincipalPermission -ObjectId $grantToRemove.ObjectId
}
```

Revokes the permission associated with the 'Office 365 SharePoint Online' resource and with scope claim 'MyFiles.Read'.
If there is no permission with those properties, then no revoke action will be taken.

## PARAMETERS

### -ObjectId

The Object ID of the permission grant to revoke

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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
