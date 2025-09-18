---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/unregister-spohubsite
applicable: SharePoint Online
title: Unregister-SPOHubSite
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Unregister-SPOHubSite

## SYNOPSIS

Disables the hub site feature on a site.

## SYNTAX

```
Unregister-SPOHubSite [-Identity] <SpoHubSitePipeBind> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Disables the hub site feature on a site so that it is no longer a hub site. Associated sites may still appear associated for up to an hour. If you want to speed up the process, use the Remove-SPOHubSiteAssociation cmdlet to remove the associated sites first.

> [!NOTE]
> If the site doesn't exist, this cmdlet returns a "File not found" error.

## EXAMPLES

### Example 1

```powershell
Unregister-SPOHubSite -Identity <guid>
```

This example removes a site from the hub site list based on unique hub identifier (\<guid\>).

### Example 2

```powershell
Unregister-SPOHubSite -Identity https://contoso.sharepoint.com/sites/Marketing
```

This example disables the hub feature on the marketing site.

## PARAMETERS

### -Force

> Applicable: SharePoint Online

Whether to disable the hub site feature without prompting for confirmation.

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

### -Identity

> Applicable: SharePoint Online

Guid based identifier or URL of the site to disable the hub site feature. If hub site has been already deleted, you will need to use a Guid based identifier to remove the site from the list of hub sites.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoHubSitePipeBind
Parameter Sets: (All)
Aliases: HubSite

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Online.SharePoint.PowerShell.SpoHubSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
