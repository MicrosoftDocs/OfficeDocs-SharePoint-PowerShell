---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/request-spoupgradeevaluationsite
applicable: SharePoint Online
title: Request-SPOUpgradeEvaluationSite
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Request-SPOUpgradeEvaluationSite

## SYNOPSIS

Requests to create a copy of an existing site collection for the purposes of validating the effects of upgrade without affecting the original site.

## SYNTAX

```
Request-SPOUpgradeEvaluationSite -Identity <SpoSitePipeBind> [-NoUpgrade] [-NoEmail] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The `Request-SPOUpgradeEvaluationSite` cmdlet lets the SharePoint Online administrator request a copy of an existing site collection for the purposes of validating the effects of upgrade without affecting the original site.

A request for an upgrade evaluation site is not automatically processed.
Instead, it is scheduled to occur in the background when it causes the least effect on the service.

You must be at least a SharePoint administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
Request-SPOUpgradeEvaluationSite https://contoso.sharepoint.com/sites/marketing
```

Example 1 requests a site upgrade evaluation for the marketing site <https://contoso.sharepoint.com/sites/marketing> using the default options of sending an email message and automatically trying to upgrade the evaluation site.

### EXAMPLE 2

```powershell
Request-SPOUpgradeEvaluationSite https://contoso.sharepoint.com/sites/marketing -NoEmail $true -NoUpgrade $true
```

This example requests a site upgrade evaluation for the marketing site <https://contoso.sharepoint.com/sites/marketing.> It specifies to not send email messages and not automatically try upgrade of the evaluation site. By using the cmdlet in this way, a SharePoint Online administrator or above can make changes to the upgrade evaluation site before starting the actual upgrade.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the SharePoint Online site collection for which you want to request a copy for the new Upgrade or Evaluation site collection.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:


Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoEmail

> Applicable: SharePoint Online

Specifies that the system not send the requester and site collection administrators an email message at the end of the upgrade evaluation site creation process.

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

### -NoUpgrade

> Applicable: SharePoint Online

Specifies that the system not perform an upgrade as part of the evaluation site creation process.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Upgrade-SPOSite](Upgrade-SPOSite.md)
