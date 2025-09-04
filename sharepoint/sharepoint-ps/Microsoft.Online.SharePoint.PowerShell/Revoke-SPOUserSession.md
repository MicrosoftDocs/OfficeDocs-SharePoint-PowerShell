---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/revoke-spousersession
applicable: SharePoint Online
title: Revoke-SPOUserSession
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Revoke-SPOUserSession

## SYNOPSIS

Provides IT administrators the ability to invalidate a particular users' O365 sessions across all their devices.

## SYNTAX

```
Revoke-SPOUserSession [-User] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

You must be a Global Administrator to run the cmdlet.

Requires a valid `Connect-SPOService` context to identify the tenant. For information about how to connect to the tenant, see `Connect-SPOService`.

When the cmdlet is run the following will occur:

User will be signed out of browser, desktop and mobile applications accessing Office 365 resources across all devices.

Will not be applicable for guest users.

Possible results for this cmdlet are:

Result |                                                                                             Reason
--- | ---
Warning : We couldn't find the user@contoso.com. Check for typos and try again. |                    Invalid input for -User parameter.
We successfully signed out \<user\> from all devices. |                                                Successful instantaneous revocation.
It can take up to an hour to sign out \<user\> from all devices. |                                     Successful non-instantaneous revocation.
Sorry, something went wrong and we couldn't sign out \<user\> from any device. |                       The cmdlet did not successfully execute.
The cmdlet will be available in the future, but it isn't ready for use in your organization yet. |   The cmdlet has been disabled for the tenant.

## EXAMPLES

### EXAMPLE 1

```powershell
Revoke-SPOUserSession -User user1@contoso.com
```

This example signs out user1 in the Contoso tenancy from all devices.

### EXAMPLE 2

```powershell
Revoke-SPOUserSession -User user1@contoso.com -Confirm:$false
```

This example signs out user1 in the Contoso tenancy from all devices without prompting for confirmation.

## PARAMETERS

### -User

> Applicable: SharePoint Online

Specifies a user name. For example, user1@contoso.com

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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
