---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/restore-spodeletedcontainer
applicable: SharePoint Online
title: Restore-SPODeletedContainer
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# Restore-SPODeletedContainer

## SYNOPSIS

Recovers a deleted Container from the Recycle Bin. 

## SYNTAX

### ParamSet1

```powershell
Restore-SPODeletedContainer [-Identity <ContainerId>] [<CommonParameters>]
```

## DESCRIPTION

The `Restore-SPODeletedContainer` cmdlet recovers a previously deleted File Storage Container from the Recycle Bin. Restored Containers will be retrieved by the [`Get-SPOContainer`](./Get-SPOContainer.md) cmdlet. You must be at least a SharePoint Online Administrator to run this cmdlet.



## EXAMPLES

### Example 1

```powershell
Restore-SPODeletedContainer -Identity b66f5b2e-4cbd-4754-9ad3-8291c2c81ade
```
Example 1 restores the Container with `ContainerId` `b66f5b2e-4cbd-4754-9ad3-8291c2c81ade` from the Recycle Bin.


## PARAMETERS



### -Identity

Use this parameter to specify the `ContainerId` of the deleted container to be restored.
 
```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: Yes
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).


## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Get-SPODeletedContainer](./Get-SPODeletedContainer.md)
