---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainertype
applicable: SharePoint Online
title: Get-SPOContainerType
schema: 2.0.0
author: cindylay
ms.author: cindylay
ms.reviewer:
---

# Get-SPOContainerType

## SYNOPSIS

Gets the Container Types and corresponding applications created in a SharePoint Embedded tenant. 
<!-- TODO -->

## SYNTAX

### ParamSet1

```powershell
Get-SPOContainerType [<CommonParameters>]
```

### ParamSet2
```powershell
Get-SPOContainerType -ContainerTypeId [<ContainerTypeId>]
```


## DESCRIPTION

The `Get-SPOContainerType` cmdlet...Get-SPOContainerType -ContainerTypeId <ContainerTypeId>Get-SPOContainerType -ContainerTypeId <ContainerTypeId>

This command is available only in SharePoint Online Management Shell version 16.0.24211.12000 or higher to run this cmdlet.
You must be a SharePoint Online Administrator or Global Administrator to run this cmdlet.


## EXAMPLES

### Example 1

```powershell
Get-SPOContainerType  #TODO
```

Example 1 returns... 


### Example 2

```powershell
Get-SPOContainerType -ContainerTypeId <ContainerTypeId> 
```

Example 2 returns Container Types and the corresponding applications created in their tenant

 
## PARAMETERS

### -ContainerTypeId

This parameter specifies the ContainerTypeId use to create one or more containers in the SharePoint Embedded application.
 
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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

