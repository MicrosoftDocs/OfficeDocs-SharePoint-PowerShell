---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spositearchivestate
applicable: SharePoint Online
title: Set-SPOSiteArchiveState
schema: 2.0.0
author: AdiGanMSFT
ms.author: adigan
ms.reviewer:
---

# Set-SPOSiteArchiveState

## SYNOPSIS

Sets the archived state of the site. Can be used to archive and reactivate sites.

## SYNTAX

```
Set-SPOSiteArchiveState [-Identity] <SpoSitePipeBind> [-ArchiveState] <SPOArchiveState> [-NoWait] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to change the archive status of the site. You must be at least a SharePoint Online administrator and be a site collection administrator to run the cmdlet.
Microsoft 365 Archive needs to be enabled for the organization to be able to use the feature.

## EXAMPLES

### Example 1

```powershell
Set-SPOSiteArchiveState https://contoso.sharepoint.com/sites/Marketing -ArchiveState Archived
```

This example marks the site as Archived. For seven days after the operation, the site will remain in a "RecentlyArchived" state, where any reactivations will be free and instantaneous. If a site is reactivated after seven days, any reactivations will be charged and will take time.

### Example 2

```powershell
Set-SPOSiteArchiveState https://contoso.sharepoint.com/sites/Marketing -ArchiveState Active
```

This example triggers the reactivation of a site. If the site is reactivated from the "RecentlyArchived" state, it will become available instantaneously. If the site is reactivated from the "FullyArchived" state, it may take time for it to be reactivated.

## PARAMETERS

### -ArchiveState

Sets the archived state of the site. Valid values are Archived, Active.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOArchiveState
Parameter Sets: (All)
Aliases:
Accepted values: Archived, Active
Applicable: SharePoint Online

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
{{ Fill Force Description }}

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
{{ Fill Identity Description }}

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
{{ Fill NoWait Description }}

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

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
