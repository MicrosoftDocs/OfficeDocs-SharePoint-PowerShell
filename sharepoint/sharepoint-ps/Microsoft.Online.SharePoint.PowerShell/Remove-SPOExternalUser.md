---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/remove-spoexternaluser
applicable: SharePoint Online
title: Remove-SPOExternalUser
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Remove-SPOExternalUser

## SYNOPSIS

Removes a collection of external users from the tenancy's folder.

## SYNTAX

```
Remove-SPOExternalUser -UniqueIDs <String[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The `Remove-SPOExternalUser` cmdlet permanently removes a collection of external users from the tenancy's folder.

Users who are removed lose access to all tenant resources.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE

```powershell
$user = Get-SPOExternalUser -Filter someone@example.com
Remove-SPOExternalUser -UniqueIDs @($user.UniqueId)
```

This example removes a specific external user who has the address "someone@example.com". Organization members may still see the external user name displayed in the Shared With dialog, but the external user will not be able to sign in and will not be able to access any tenant resources.

## PARAMETERS

### -UniqueIDs

> Applicable: SharePoint Online

Specifies an ID that can be used to identify an external user based on their Windows Live ID.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOExternalUser](Get-SPOExternalUser.md)
