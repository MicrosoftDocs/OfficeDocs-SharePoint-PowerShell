---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenant
applicable: SharePoint Online
title: Get-SPOTenant
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOTenant

## SYNOPSIS

Returns SharePoint Online organization properties.

## SYNTAX

```
Get-SPOTenant [-ShowDetails] [<CommonParameters>]
```

## DESCRIPTION

The `Get-SPOTenant` cmdlet returns organization-level site collection properties such as StorageQuota, StorageQuotaAllocated, ResourceQuota, ResourceQuotaAllocated and SiteCreationMode.

Currently, there are no parameters for this cmdlet.

You must be a SharePoint Online administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Get-SPOTenant
```

This example returns the organization-level site collection properties such as StorageQuota, StorageQuotaAllocated, ResourceQuota, ResourceQuotaAllocated, SiteCreationMode and OneDriveStorageQuota.

## PARAMETERS

### -ShowDetails

> Applicable: SharePoint Online

Whether to show the detailed properties for each setting.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)
