---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Get-SPODataAccessGovernanceInsight

## SYNOPSIS

Lists various reports available in 'Data Access Governance' module (DAG) in SharePoint Admin Center.

## SYNTAX

### GetAllReportsParameterSet
```
Get-SPODataAccessGovernanceInsight -ReportEntity <ReportEntityEnum> [-WorkLoad <WorkloadEnum>]
 [-ReportType <ReportTypeEnum>] [<CommonParameters>]
```

### GetReportParameterSet
```
Get-SPODataAccessGovernanceInsight -ReportID <Guid> [<CommonParameters>]
```

## DESCRIPTION

Fetch details of various reports available in 'Data Access Governance' module (DAG) in SharePoint Admin Center

## EXAMPLES

### Example 1

```powershell
PS C:\> Get-SPODataAccessGovernanceInsight -ReportEntity EveryoneExceptExternalUsersForItems
```

This command fetches all DAG reports about 'Everyone except external users' attached to a item i.e., file/folder/list. The output consists of important parameters such as Status, ReportID, number of sites in the report and other user provided values during report generation.

## PARAMETERS

### -ReportEntity

Specifies the 'potential oversharing' scenario as captured by DAG report given during the report creation.

```yaml
Type: ReportEntityEnum
Parameter Sets: GetAllReportsParameterSet
Aliases:
Accepted values: SharingLinks_Anyone, SharingLinks_PeopleInYourOrg, SharingLinks_Guests, SensitivityLabelForFiles, EveryoneExceptExternalUsersAtSite, EveryoneExceptExternalUsersForItems, PermissionedUsers

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

Specifies the time period of data of the reports to be fetched i.e., fetch 'Snapshot' reports or 'RecentActivity' reports

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
