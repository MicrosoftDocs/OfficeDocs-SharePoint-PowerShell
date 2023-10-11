---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spocrosstenantrelationship
applicable: SharePoint Online
title: Set-SPOCrossTenantRelationship
schema: 2.0.0
author: 
ms.author: 
ms.reviewer:
---

# Set-SPOCrossTenantRelationship

## SYNOPSIS

This cmdlet sends a trust request to the tenant with whom you want to establish trust.

## SYNTAX

```powershell
Set-SPOCrossTenantRelationship -PartnerCrossTenantHostUrl <String> -PartnerRole <OrgRelationRole> -Scenario <OrgRelationScenario>  [<CommonParameters>]
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
The cross-tenant URL of the partner tenant. The partner tenant can determine this for you by running `Get-SPOCrossTenantHostUrl` on each of the tenants.

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

### -PartnerRole
Roles of the partner tenant you're establishing trust with. Use *source* if partner tenant is the source of the OneDrive migrations, and *target* if the partner tenant is the Destination.

```yaml
Type: OrgRelationRole
Parameter Sets: (All)
Aliases:
Accepted values: Target, Source
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scenario

```yaml
Type: OrgRelationScenario
Parameter Sets: (All)
Aliases:
Accepted values: MnA, None
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)
