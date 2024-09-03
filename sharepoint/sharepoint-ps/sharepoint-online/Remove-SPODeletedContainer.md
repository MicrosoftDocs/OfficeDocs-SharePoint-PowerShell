---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spodeletedcontainer
applicable: SharePoint Online
title: Remove-SPODeletedContainer
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# Remove-SPODeletedContainer

## SYNOPSIS

Permanently deletes the specified Container from the Recycle Bin. This action cannot be undone.

## SYNTAX



### ParamSet1

```powershell
Remove-SPODeletedContainer [-Identity <ContainerId>] [<CommonParameters>]
```

## DESCRIPTION

The `Remove-SPODeletedContainer` cmdlet permanently removes a deleted File Storage Container from the Recycle Bin. A permanently deleted Container cannot be recovered. You must be at least a SharePoint Online administrator to run the cmdlet.

> [!IMPORTANT]
> We do not generally recommend that you permanently delete Containers.

 


For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).

## EXAMPLES

### Example 1

```powershell
Remove-SPODeletedContainer -Identity b66f5b2e-4cbd-4754-9ad3-8291c2c81ade
```

This example removes a deleted Container with the `ContainerId` `b66f5b2e-4cbd-4754-9ad3-8291c2c81ade` from the Recycle Bin and deletes it permanently.



## PARAMETERS

### -Identity

Specifies the `<ContainerId>` of the Container to be permanently deleted.
 
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

## INPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Remove-SPOContainer](./Remove-SPOContainer.md)

