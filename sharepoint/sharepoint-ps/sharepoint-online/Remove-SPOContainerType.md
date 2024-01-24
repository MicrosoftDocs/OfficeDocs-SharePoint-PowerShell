---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainertype
applicable: SharePoint Online
title: Remove-SPOContainerType
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# Remove-SPOContainerType

## SYNOPSIS
Removes a ContainerType <!-- TODO -->

## SYNTAX

### ParamSet1

```powershell
Remove-SPOContainerType [-Identity <ContainerTypeId>] [<CommonParameters>] 
```
<!-- TODO -->

## DESCRIPTION

The `Remove-SPOContainerType` cmdlet deletes....



You must be a SharePoint Online Administrator or Global Administrator to run this cmdlet.

## EXAMPLES

### Example 1

```powershell
Remove-SPOContainer -Identity 423poi45-jikl-9bnm-b302-1234ghy56789
```

Example 1 places the Container with the `ContainerId` `423poi45-jikl-9bnm-b302-1234ghy56789` into the Recycle Bin. The Container will be permanently deleted from the Recycle Bin after 93 days unless the deleted Container is [restored](./Restore-SPODeletedContainer.md) before permanent deletion. 

## PARAMETERS

### -Identity

Use this parameter to provide the `ContainerId` of the Container to be deleted.
 
```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## NOTES

## RELATED LINKS
  