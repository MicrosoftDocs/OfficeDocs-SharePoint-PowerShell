---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spocontainerdataaccessgovernancejob
applicable: SharePoint Online
title: Get-SPOContainerDataAccessGovernanceJob
schema: 2.0.0
---

# Get-SPOContainerDataAccessGovernanceJob

## SYNOPSIS

Lists SharePoint Embedded Data Access Governance reports or gets a report by ID.

## SYNTAX

### ListParameterSet (Default)

```
Get-SPOContainerDataAccessGovernanceJob -JobType <String> [<CommonParameters>]
```

### ReportIdParameterSet

```
Get-SPOContainerDataAccessGovernanceJob -ReportID <Guid> [<CommonParameters>]
```

## DESCRIPTION

Use `Get-SPOContainerDataAccessGovernanceJob` to list full-detail SharePoint Embedded Site Permissions reports or retrieve a specific SharePoint Embedded report. Specify either `JobType` or `ReportID`, not both.

The output includes the report ID, report name, workload, and status. Wait until the status is `Completed` before exporting the report. This cmdlet retrieves report metadata, not the report's CSV content.

A report ID belonging to SharePoint or OneDrive isn't accepted. Use `Get-SPODataAccessGovernanceInsight` for those reports.

Connect to the tenant administration endpoint with `Connect-SPOService` before running this cmdlet. The service must support SharePoint Embedded Data Access Governance reports, and the signed-in account must be authorized to access them.

## EXAMPLES

### Example 1

```powershell
Get-SPOContainerDataAccessGovernanceJob -JobType SitePermissions
```

This example lists full-detail Site Permissions reports for SharePoint Embedded.

### Example 2

```powershell
Get-SPOContainerDataAccessGovernanceJob -ReportID 28f4c550-215a-472b-a123-c11e5fa8804c
```

This example gets the metadata and status of a report. Replace the example ID with an ID returned by `Start-SPOContainerDataAccessGovernanceJob` or a previous list operation.

## PARAMETERS

### -JobType

Specifies the report job type to list. The only supported value is `SitePermissions`.

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:
Accepted values: SitePermissions

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportID

Specifies the ID of a SharePoint Embedded report.

```yaml
Type: System.Guid
Parameter Sets: ReportIdParameterSet
Aliases:

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

### Microsoft.Online.SharePoint.PowerShell.SPDataGovernanceInsightSitePermissionsResponse

Report metadata objects. A list operation can return no reports.

## NOTES

## RELATED LINKS

[Connect-SPOService](./Connect-SPOService.md)

[Start-SPOContainerDataAccessGovernanceJob](./Start-SPOContainerDataAccessGovernanceJob.md)

[Export-SPOContainerDataAccessGovernanceJob](./Export-SPOContainerDataAccessGovernanceJob.md)

[Remove-SPOContainerDataAccessGovernanceJob](./Remove-SPOContainerDataAccessGovernanceJob.md)

[Get-SPODataAccessGovernanceInsight](./Get-SPODataAccessGovernanceInsight.md)
