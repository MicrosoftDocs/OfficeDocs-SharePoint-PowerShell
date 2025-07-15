---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocrosstenantcompatibilitystatus
applicable: SharePoint Online
title: Get-SPOCrossTenantCompatibilityStatus
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOCrossTenantCompatibilityStatus

## SYNOPSIS

Determines the compatibility with the partner tenant.

## SYNTAX

```
Get-SPOCrossTenantCompatibilityStatus [-PartnerCrossTenantHostUrl] <String> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet allows you to determine the compatibility with the partner tenant before cross-tenant migration. You must be a SharePoint Administrator to run it.

> [!NOTE]
> You must run this command on the source tenant only.

## EXAMPLES

### Example 1

```powershell
Get-SPOCrossTenantCompatibilityStatus -PartnerCrossTenantHostUrl https://contoso-my.sharepoint.com
```

Gets the compatibility status with the partner tenant Contoso.

## PARAMETERS

### -PartnerCrossTenantHostUrl
The cross-tenant URL of the partner tenant. The partner tenant can determine this for you by running `Get-SPOCrossTenantHostUrl` on each of the tenants.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: 0
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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
