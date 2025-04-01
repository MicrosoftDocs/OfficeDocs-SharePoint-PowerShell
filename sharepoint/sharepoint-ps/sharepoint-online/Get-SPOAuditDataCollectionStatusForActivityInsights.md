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

Lists the current status of audit data collection for reports based on activities within the last 28 days, from SharePoint Admin Center.

## SYNTAX

```
Get-SPOAuditDataCollectionStatusForActivityInsights [-ReportEntity <OptInReportEntityEnum>]
 [<CommonParameters>]
```

## DESCRIPTION

SharePoint administrators can generate reports based on activities within the last 28 days such as Sharing link reports, content shared with Everyone except external users etc from SharePoint admin center. These reports require audit data to be collected after approved by SharePoint admin. This command gives the current status of the relevant audit data collection.

## EXAMPLES

### Example 1

```powershell
PS C:\> Get-SPOAuditDataCollectionStatusForActivityInsights -ReportEntity SharingLinks_Anyone
```

This command fetches the current status of audit data collection for the report on sites with most number of "Anyone" sharing links generated in the last 28 days.

## PARAMETERS

### -ReportEntity

Specifies the entity for which the corresponding audit data collection status should be shown

```yaml
Type: OptInReportEntityEnum
Parameter Sets: (All)
Aliases:
Accepted values: SharingLinks_Anyone, SharingLinks_PeopleInYourOrg, SharingLinks_Guests, EveryoneExceptExternalUsersAtSite, EveryoneExceptExternalUsersForItems, CopilotAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Start-SPOAuditDataCollectionForActivityInsights](./Start-SPOAuditDataCollectionForActivityInsights.md)
[Stop-SPOAuditDataCollectionForActivityInsights](./Stop-SPOAuditDataCollectionForActivityInsights.md)
[Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md)
