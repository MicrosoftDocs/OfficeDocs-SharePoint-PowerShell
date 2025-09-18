---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/remove-spocontainer
applicable: SharePoint Online
title: Remove-SPOContainer
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# Remove-SPOContainer

## SYNOPSIS

Sends a Container to the Recycle Bin.

## SYNTAX

```
Remove-SPOContainer [-Identity] <SPOContainerPipeBind> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The `Remove-SPOContainer` cmdlet deletes a File Storage Container and puts it in the Recycle Bin. A Container that is deleted will no longer be retrieved by the [`Get-SPOContainer`](./Get-SPOContainer.md) cmdlet.

When admins delete a Container, it is moved into the Recycle Bin. A deleted Container can be [restored](./Restore-SPODeletedContainer.md) from the Recycle Bin within 93 days. If a Container is deleted from the Recycle Bin, or it exceeds the 93-day retention period, it is permanently deleted. Deleting a Container deletes everything within it, including all documents and files. You can view all deleted Containers in the Recycle Bin with the [`Get-SPODeletedContainer`](./Get-SPODeletedContainer.md) cmdlet.

You must be at least a SharePoint Online administrator to run the cmdlet.

## EXAMPLES

### Example 1

```powershell
Remove-SPOContainer -Identity 423poi45-jikl-9bnm-b302-1234ghy56789
```

Example 1 places the Container with the `ContainerId` `423poi45-jikl-9bnm-b302-1234ghy56789` into the Recycle Bin. The Container will be permanently deleted from the Recycle Bin after 93 days unless the deleted Container is [restored](./Restore-SPODeletedContainer.md) before permanent deletion.

## PARAMETERS

### -Force

> Applicable: SharePoint Online

Whether to remove the container without prompting for confirmation.

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

Use this parameter to provide the `ContainerId` of the Container to be deleted.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOContainerPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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

[Get-SPODeletedContainer](./Get-SPODeletedContainer.md)

[Restore-SPODeletedContainer](./Restore-SPODeletedContainer.md)

[Remove-SPODeletedContainer](./Remove-SPODeletedContainer.md)
