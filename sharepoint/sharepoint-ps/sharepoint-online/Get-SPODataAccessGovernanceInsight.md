---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spodataaccessgovernanceinsight
applicable: SharePoint Online
title: Get-SPODataAccessGovernanceInsight
schema: 2.0.0
author: pvrk
ms.author: pullabhk
manager: 
ms.reviewer:
---

# Get-SPODataAccessGovernanceInsight

## SYNOPSIS

Lists various 'Data Access Governance' (DAG) reports in SharePoint admin center.

## SYNTAX

### GetAllReportsParameterSet
```
Get-SPODataAccessGovernanceInsight -ReportEntity <ReportEntityEnum> [-WorkLoad <WorkloadEnum>] [-ReportType <ReportTypeEnum>] [<CommonParameters>]
```

### GetReportParameterSet
```
Get-SPODataAccessGovernanceInsight -ReportID <Guid> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet fetches details of various DAG reports available in SharePoint admin center.

## EXAMPLES

### Example 1

```powershell
Get-SPODataAccessGovernanceInsight -ReportEntity EveryoneExceptExternalUsersForItems
```

The above cmdlet fetches all DAG reports about 'Everyone except external users' attached to an item i.e., to a file, folder, or list in the last 28 days. The output consists of important parameters such as Status, ReportID, number of sites in the report and other user provided values during report generation.

## PARAMETERS

### -ReportEntity

Specifies the entity that could cause oversharing and hence tracked by these reports.

```yaml
Type: ReportEntityEnum
Parameter Sets: GetAllReportsParameterSet
Aliases:
Accepted values: SharingLinks_Anyone, SharingLinks_PeopleInYourOrg, SharingLinks_Guests, SensitivityLabelForFiles, EveryoneExceptExternalUsersAtSite, EveryoneExceptExternalUsersForItems, PermissionedUsers, PermissionsReport (Preview)

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportID

Specifies the ID of the particular report to be fetched.

```yaml
Type: Guid
Parameter Sets: GetReportParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportType

Specifies the time period of data of the reports to be fetched. A 'Snapshot' report will have the latest data as of the report generation time. A 'RecentActivity' report will be based on data in the last 28 days.

```yaml
Type: ReportTypeEnum
Parameter Sets: GetAllReportsParameterSet
Aliases:
Accepted values: Snapshot, RecentActivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkLoad

Specifies the datasource of the reports to be fetched i.e., reports for SharePoint sites or for OneDrive accounts.

```yaml
Type: WorkloadEnum
Parameter Sets: GetAllReportsParameterSet
Aliases:
Accepted values: SharePoint, OneDriveForBusiness

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

[Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md)

[Export-SPODataAccessGovernanceInsight](./Export-SPODataAccessGovernanceInsight.md)

[Remove-SPODataAccessGovernanceInsight](./Remove-SPODataAccessGovernanceInsight.md)

[Start-SPOSiteReview](./Start-SPOSiteReview.md)

[Get-SPOSiteReview](./Get-SPOSiteReview.md)
