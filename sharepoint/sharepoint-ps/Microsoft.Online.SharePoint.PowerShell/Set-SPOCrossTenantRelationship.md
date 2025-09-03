---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spocrosstenantrelationship
applicable: SharePoint Online
title: Set-SPOCrossTenantRelationship
schema: 2.0.0
author: trent-green
ms.author: speedta
ms.reviewer:
---

# Set-SPOCrossTenantRelationship

## SYNOPSIS

This cmdlet sends a trust request to the tenant with whom you want to establish trust.

## SYNTAX

```
Set-SPOCrossTenantRelationship [-Scenario] <OrgRelationScenario> [-PartnerRole] <OrgRelationRole>
 [-PartnerCrossTenantHostUrl] <String> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to send a trust request to the tenant with whom you want to establish trust.

## EXAMPLES

### Example 1

```powershell
Set-SPOCrossTenantRelationship -Scenario MnA -PartnerRole Target -PartnerCrossTenantHostUrl https://contoso-my.sharepoint.com
```

This cmdlet sends a trust request to the Contoso tenant.

## PARAMETERS

### -PartnerCrossTenantHostUrl

> Applicable: SharePoint Online
The cross-tenant URL of the partner tenant. The partner tenant can determine this for you by running `Get-SPOCrossTenantHostUrl` on each of the tenants.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerRole

> Applicable: SharePoint Online
Roles of the partner tenant you're establishing trust with. Use *source* if the partner tenant is the source of the OneDrive migrations, and *target* if the partner tenant is the destination.

```yaml
Type: Microsoft.SharePoint.Client.Administration.OrgRelationRole
Parameter Sets: (All)
Aliases:
Accepted values: None, Source, Target

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scenario

> Applicable: SharePoint Online

```yaml
Type: Microsoft.SharePoint.Client.Administration.OrgRelationScenario
Parameter Sets: (All)
Aliases:
Accepted values: None, MnA

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
