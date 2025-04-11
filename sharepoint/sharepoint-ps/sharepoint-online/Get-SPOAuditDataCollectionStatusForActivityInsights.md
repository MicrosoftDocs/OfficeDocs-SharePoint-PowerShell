---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spoauditdatacollectionstatusforactivityinsights
applicable: SharePoint Online
title: Get-SPOAuditDataCollectionStatusForActivityInsights
schema: 2.0.0
author: pvrk
ms.author: pullabhk
manager: 
ms.reviewer:
---

# Get-SPOAuditDataCollectionStatusForActivityInsights

## SYNOPSIS

Lists the current status of audit data collection for reports on activities from the last 28 days in the SharePoint admin center.

## SYNTAX

```
Get-SPOAuditDataCollectionStatusForActivityInsights [-ReportEntity <OptInReportEntityEnum>]
 [<CommonParameters>]
```

## DESCRIPTION

SharePoint Administrators can generate reports on activities from the last 28 days, such as sharing link reports and content shared with everyone except external users, from the SharePoint admin center. These reports need audit data, which must be collected after approval by the SharePoint Administrator. This cmdlet shows the current status of the audit data collection.

## EXAMPLES

### Example 1

```powershell
Get-SPOAuditDataCollectionStatusForActivityInsights -ReportEntity SharingLinks_Anyone
```

This example fetches the current status of audit data collection for the report on sites with most number of "Anyone" sharing links generated in the last 28 days.

## PARAMETERS

### -ReportEntity

Specifies the entity for which the corresponding audit data collection status should be shown.

```yaml
Type: OptInReportEntityEnum
Parameter Sets: (All)
Aliases:
Accepted values: SharingLinksAnyone, SharingLinksPeopleInYourOrg, SharingLinksGuests, EveryoneExceptExternalUsersAtSite, EveryoneExceptExternalUsersForItems, CopilotAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Start-SPOAuditDataCollectionForActivityInsights](./Start-SPOAuditDataCollectionForActivityInsights.md)
[Stop-SPOAuditDataCollectionForActivityInsights](./Stop-SPOAuditDataCollectionForActivityInsights.md)
[Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md)
