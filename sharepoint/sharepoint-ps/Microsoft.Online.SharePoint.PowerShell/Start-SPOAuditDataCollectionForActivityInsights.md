---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/start-spoauditdatacollectionforactivityinsights
applicable: SharePoint Online
title: Start-SPOAuditDataCollectionForActivityInsights
schema: 2.0.0
author: pvrk
ms.author: pullabhk
manager:
ms.reviewer:
ms.date: 07/15/2025
---

# Start-SPOAuditDataCollectionForActivityInsights

## SYNOPSIS

This cmdlet starts collecting audit data for reports on activities from the last 28 days, such as sharing link reports and content shared with everyone except external users, from the SharePoint admin center.

## SYNTAX

```
Start-SPOAuditDataCollectionForActivityInsights -ReportEntity <OptInReportEntityEnum> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet starts collecting audit data for reports on sharing and access activities from the last 28 days. Reports are available for the following scenarios:

- Sharing links created in the last 28 days (Anyone, People in Your Organization, Specific people shared externally).
- Content shared with Everyone except external users (EEEU) in the last 28 days.
- Copilot agents created in the last 28 days *(Private Preview)*.

## EXAMPLES

### Example 1

```powershell
Start-SPOAuditDataCollectionForActivityInsights -ReportEntity SharingLinks_Anyone
```

This example will start collecting audit data related to the generation of 'Anyone' sharing links from the moment the cmdlet is executed.

## PARAMETERS

### -ReportEntity

Specifies the entity for which the corresponding audit data should be collected.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.OptInReportEntityEnum
Parameter Sets: (All)
Aliases:
Accepted values: SharingLinksAnyone, SharingLinksPeopleInYourOrg, SharingLinksGuests, EveryoneExceptExternalUsersAtSite, EveryoneExceptExternalUsersForItems, CopilotAppInsights

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

[Stop-SPOAuditDataCollectionForActivityInsights](./Stop-SPOAuditDataCollectionForActivityInsights.md)
[Get-SPOAuditDataCollectionStatusForActivityInsights](./Get-SPOAuditDataCollectionStatusForActivityInsights.md)
[Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md)
