---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Start-SPODataAccessGovernanceInsight

## SYNOPSIS

This command generates various reports which are meant to provide insights into potential oversharing of sensitive data in SharePoint and/or OneDrive for Business. These insights are powered by Data Access Governance (DAG) module, available in SharePoint Admin Center. SharePoint Advanced Management (SAM) license is required to run this command.

## SYNTAX

### EEEUParameterSet
```
Start-SPODataAccessGovernanceInsight -ReportEntity <ReportEntityEnum> -Workload <WorkloadEnum>
 -ReportType <ReportTypeEnum> -Name <String>
 [-Template <System.Collections.Generic.List`1[Microsoft.Online.SharePoint.TenantAdministration.TemplateEnum]>]
 [-Privacy <PrivacyEnum>] [-SiteSensitivityLabelGUID <System.Collections.Generic.List`1[System.Guid]>]
 [<CommonParameters>]
```

### SharingLinkParameterSet
```
Start-SPODataAccessGovernanceInsight -ReportEntity <ReportEntityEnum> -Workload <WorkloadEnum>
 -ReportType <ReportTypeEnum> [<CommonParameters>]
```

### LabelParameterSet
```
Start-SPODataAccessGovernanceInsight -ReportEntity <ReportEntityEnum> -Workload <WorkloadEnum>
 -ReportType <ReportTypeEnum> [-FileSensitivityLabelName <String>] -FileSensitivityLabelGUID <Guid>
 [<CommonParameters>]
```

### SitePermissionsParameterSet
```
Start-SPODataAccessGovernanceInsight -ReportEntity <ReportEntityEnum> -Workload <WorkloadEnum>
 -ReportType <ReportTypeEnum> -Name <String>
 [-Template <System.Collections.Generic.List`1[Microsoft.Online.SharePoint.TenantAdministration.TemplateEnum]>]
 [-Privacy <PrivacyEnum>] [-SiteSensitivityLabelGUID <System.Collections.Generic.List`1[System.Guid]>]
 -CountOfUsersMoreThan <Int32> [<CommonParameters>]
```

## DESCRIPTION

This command is used to generate reports, in Data Access Governance (DAG) module, regarding potential oversharing of sensitive data. Reports are currently available for:

- Sharing links created in last 28 days (Anyone, People-in-your-org, Specific people shared externally).
- Content shared with Everyone except external users (EEEU) in last 28 days.
- List of sites having labelled files, as of report generation time.
- List of sites having 'too-many-users', as of report generation time, to setup an oversharing baseline.

## EXAMPLES

### Example 1

```powershell
PS C:\> Start-SPODataAccessGovernanceInsight -ReportEntity PermissionedUsers -Workload SharePoint -ReportType Snapshot -Name "OversharingBaselineReport" -CountOfUsersMoreThan 1000
```

The above command generates a list of SharePoint sites which can be accessed by more than 1000 users, as of the report generation day.

## PARAMETERS

### -CountOfUsersMoreThan

Specifies the threshold of oversharing as defined by the number of users that can access the site. The number of users that can access the site are determined by expanding all users, groups across all permissions (at site level and at the level of any item with unqiue permissions), deduplicate and arrive at a unique number. Minumum value is 100.

```yaml
Type: Int32
Parameter Sets: SitePermissionsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileSensitivityLabelGUID

Specifies the GUID for the sensitivity label for the file.

```yaml
Type: Guid
Parameter Sets: LabelParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileSensitivityLabelName

Specifies the name of the sensitivity label for the file.

```yaml
Type: String
Parameter Sets: LabelParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies the name to be given to the generated report.

```yaml
Type: String
Parameter Sets: EEEUParameterSet, SitePermissionsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Privacy

Specifies the privacy setting of the 0365 group. Relevant in case of filtering the report for group connected sites.

```yaml
Type: PrivacyEnum
Parameter Sets: EEEUParameterSet, SitePermissionsParameterSet
Aliases:
Accepted values: All, Private, Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportEntity

Specifies the 'potential oversharing' scenario that should be captured by the DAG report.

```yaml
Type: ReportEntityEnum
Parameter Sets: (All)
Aliases:
Accepted values: SharingLinks_Anyone, SharingLinks_PeopleInYourOrg, SharingLinks_Guests, SensitivityLabelForFiles, EveryoneExceptExternalUsersAtSite, EveryoneExceptExternalUsersForItems, PermissionedUsers

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportType

Specifies the time period of data based on which DAG report is generated. A 'Snapshot' report will have the latest data as of the report generation time. A 'RecentActivity' report will be based on data in the last 'X' days.

```yaml
Type: ReportTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: Snapshot, RecentActivity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSensitivityLabelGUID

Specifies the GUID of the sensitivity label applied to the site.

```yaml
Type: System.Collections.Generic.List`1[System.Guid]
Parameter Sets: EEEUParameterSet, SitePermissionsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Template

Specifies the template of the site. Relevant in case a report should be generated for that particular template.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Online.SharePoint.TenantAdministration.TemplateEnum]
Parameter Sets: EEEUParameterSet, SitePermissionsParameterSet
Aliases:
Accepted values: AllSites, ClassicSites, CommunicationSites, TeamSites, OtherSites

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Workload

Specifies whether the report is for SharePoint sites or OneDrive accounts.

```yaml
Type: WorkloadEnum
Parameter Sets: (All)
Aliases:
Accepted values: SharePoint, OneDriveForBusiness

Required: True
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

[Data Access Governance reports for SharePoint admins](/sharepoint/data-access-governance-reports)
