---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/remove-spodeletedsite
applicable: SharePoint Online
title: Remove-SPODeletedSite
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Remove-SPODeletedSite

## SYNOPSIS

Removes a SharePoint Online deleted site collection from the Recycle Bin.

## SYNTAX

```
Remove-SPODeletedSite -Identity <SpoSitePipeBind> [-NoWait] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The `Remove-SPODeletedSite` cmdlet permanently removes a SharePoint Online deleted site collection from the Recycle Bin.

You must be at least a SharePoint administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

**Note**: As of today, the modern admin center UI does not allow permanent deletion of group connected site. The use of this cmdlet does allow the deletion, but when this occurs it does not delete the associated group, just the site.

## EXAMPLES

### EXAMPLE

```powershell
Remove-SPODeletedSite -Identity https://contoso.sharepoint.com/sites/sitetoremove
```

This example removes a SharePoint Online deleted site collection named <https://contoso.sharepoint.com/sites/sitetoremove> from the Recycle Bin and deletes it permanently.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the URL of the site collection to remove.

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

### -NoWait

> Applicable: SharePoint Online

Continues without the status being polled. Polling the action can slow its progress.

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

[Remove-SPOSite](Remove-SPOSite.md)

[Get-SPODeletedSite](Get-SPODeletedSite.md)
