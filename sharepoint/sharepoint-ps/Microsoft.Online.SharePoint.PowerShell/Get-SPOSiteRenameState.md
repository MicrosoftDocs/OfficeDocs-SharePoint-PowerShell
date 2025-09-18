---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/get-spositerenamestate
applicable: SharePoint Online
title: Get-SPOSiteRenameState
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Get-SPOSiteRenameState

## SYNOPSIS

Returns the current rename job state of a SharePoint Online Site.

## SYNTAX

### SourceSiteUrl (Default)
```
Get-SPOSiteRenameState -Identity <SpoSitePipeBind> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ParentId
```
Get-SPOSiteRenameState -ParentOperationId <Guid> [-State <RenameState>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RenameReport
```
Get-SPOSiteRenameState [-State <RenameState>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to return the current rename job state of a SharePoint Online Site.

## EXAMPLES

### Example 1

```powershell
Get-SPOSiteRenameState -Identity https://contoso.sharepoint.com/sites/ContosoWeb1
```

This example returns the rename job state of ContosoWeb1 Site.

### Example 2

```powershell
Get-SPOSiteRenameState -State InProgress
```

This example returns rename jobs that are in InProgress state.

### Example 3

```powershell
$tenantRenameJobId = (Get-SPOTenantRenameStatus).RenameJobId
Get-SPOSiteRenameState -ParentOperationId $tenantRenameJobId
```

This example returns rename jobs that were initiated by a tenant rename.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

The urls of the site to be renamed.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: SourceSiteUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentOperationId

> Applicable: SharePoint Online

The parent operation id that initiated the site to be renamed. For example, the tenant rename job id.

```yaml
Type: System.Guid
Parameter Sets: ParentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State

> Applicable: SharePoint Online

The state of the rename job, possible values are

- Queued
- InProgress
- Success
- Failed
- Suspended

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.RenameState
Parameter Sets: ParentId, RenameReport
Aliases:
Accepted values: Queued, InProgress, Success, Failed, Suspended, Canceling, Canceled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

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

Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: `get-help about_commonparameters`

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
