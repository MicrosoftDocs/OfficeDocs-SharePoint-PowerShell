---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spotenanttaxonomyreplicationparameters
applicable: SharePoint Online
title: Set-SPOTenantTaxonomyReplicationParameters
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Set-SPOTenantTaxonomyReplicationParameters

## SYNOPSIS

Select groups for replication

## SYNTAX

### ReplicateSelectedGroups (Default)
```
Set-SPOTenantTaxonomyReplicationParameters -ReplicatedGroups <String[]> [<CommonParameters>]
```

### ReplicateAllGroups
```
Set-SPOTenantTaxonomyReplicationParameters [-ReplicateAllGroups] [<CommonParameters>]
```

## DESCRIPTION

Before using this cmdlet, make sure you connect to SharePoint Online using [Connect-SPOService](Connect-SPOService.md) and the desirable satellite location URL as the -Url parameter.

By default, all global groups except system/search/people/sitecollection in primary location will be replicated to
satellite.

## EXAMPLES

### EXAMPLE 1

```powershell
Set-SPOTenantTaxonomyReplicationParameters -ReplicatedGroups "group1","group2"
```

Tenant admin can use this cmdlet to select some groups only for replicating to overwrite default settings.

### EXAMPLE 2

```powershell
Set-SPOTenantTaxonomyReplicationParameters -ReplicateAllGroups
```

Tenant admin can also reset to replicate all the groups.

## PARAMETERS

### -ReplicateAllGroups

> Applicable: SharePoint Online

This parameter specifies whether all groups should be replicated.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReplicateAllGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicatedGroups

> Applicable: SharePoint Online

Specifies a comma-separated list of groups that should be replicated.

```yaml
Type: System.String[]
Parameter Sets: ReplicateSelectedGroups
Aliases:

Required: True
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

[Introduction to the SharePoint Online management shell](https://support.office.com/en-us/article/introduction-to-the-sharepoint-online-management-shell-c16941c3-19b4-4710-8056-34c034493429)

[SharePoint Online Management Shell Download](https://www.microsoft.com/en-US/download/details.aspx?id=35588)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Get-SPOTenantTaxonomyReplicationParameters](Get-SPOTenantTaxonomyReplicationParameters.md)

[Get-SPOTenantContentTypeReplicationParameters](Get-SPOTenantContentTypeReplicationParameters.md)

[Set-SPOTenantContentTypeReplicationParameters](Set-SPOTenantContentTypeReplicationParameters.md)
