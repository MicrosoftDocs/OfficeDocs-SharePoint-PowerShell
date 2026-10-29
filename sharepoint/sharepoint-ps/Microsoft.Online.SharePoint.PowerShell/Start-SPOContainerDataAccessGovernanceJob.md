---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/start-spocontainerdataaccessgovernancejob
applicable: SharePoint Online
title: Start-SPOContainerDataAccessGovernanceJob
schema: 2.0.0
---

# Start-SPOContainerDataAccessGovernanceJob

## SYNOPSIS

Requests a Data Access Governance report for SharePoint Embedded containers.

## SYNTAX

```
Start-SPOContainerDataAccessGovernanceJob -JobType <String> -Name <String> [<CommonParameters>]
```

## DESCRIPTION

The `Start-SPOContainerDataAccessGovernanceJob` cmdlet submits a report request and returns metadata that includes the report ID and status. Report generation is asynchronous. Use `Get-SPOContainerDataAccessGovernanceJob` to check the status before downloading the completed report with `Export-SPOContainerDataAccessGovernanceJob`.

The supported job type is `SitePermissions`. This cmdlet targets SharePoint Embedded; it doesn't accept a workload parameter. To request reports for SharePoint sites or OneDrive accounts, use `Start-SPODataAccessGovernanceInsight`.

Connect to the tenant administration endpoint with `Connect-SPOService` before running this cmdlet. The service must support SharePoint Embedded Data Access Governance reports, and the signed-in account must be authorized to request them.

## EXAMPLES

### Example 1

```powershell
$job = Start-SPOContainerDataAccessGovernanceJob -JobType SitePermissions -Name "Container permissions review" -ErrorAction Stop
Get-SPOContainerDataAccessGovernanceJob -ReportID $job.ReportId
```

This example requests a report and checks its status. Returning a report ID doesn't mean report generation has completed.

## PARAMETERS

### -JobType

Specifies the report job to request. The only supported value is `SitePermissions`.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SitePermissions

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies a name for the report. The name can't be empty or contain only whitespace.

```yaml
Type: System.String
Parameter Sets: (All)
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

### Microsoft.Online.SharePoint.PowerShell.SPDataGovernanceInsightMetadata

Report metadata with `ReportId` and `Status` properties.

## NOTES

## RELATED LINKS

[Connect-SPOService](./Connect-SPOService.md)

[Get-SPOContainerDataAccessGovernanceJob](./Get-SPOContainerDataAccessGovernanceJob.md)

[Export-SPOContainerDataAccessGovernanceJob](./Export-SPOContainerDataAccessGovernanceJob.md)

[Remove-SPOContainerDataAccessGovernanceJob](./Remove-SPOContainerDataAccessGovernanceJob.md)

[Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md)
