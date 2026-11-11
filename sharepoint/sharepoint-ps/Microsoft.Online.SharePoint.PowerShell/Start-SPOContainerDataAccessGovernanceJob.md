---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/start-spocontainerdataaccessgovernancejob
applicable: SharePoint Online
title: Start-SPOContainerDataAccessGovernanceJob
schema: 2.0.0
author: niksvij
ms.author: nikhilvijay
manager:
ms.reviewer:
---

# Start-SPOContainerDataAccessGovernanceJob

## SYNOPSIS

This cmdlet requests a Data Access Governance report for SharePoint Embedded containers.

## SYNTAX

```
Start-SPOContainerDataAccessGovernanceJob -JobType <String> -Name <String> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet submits a report request and returns metadata that includes the report ID and status. Report generation is asynchronous. Use `Get-SPOContainerDataAccessGovernanceJob` to check the status before downloading the completed report with `Export-SPOContainerDataAccessGovernanceJob`.

The supported job type is `SitePermissions`. This cmdlet targets SharePoint Embedded; it doesn't accept a workload parameter. To request reports for SharePoint sites or OneDrive accounts, use `Start-SPODataAccessGovernanceInsight`.

You must be a SharePoint Embedded Administrator or Global Administrator to run this cmdlet. SharePoint Embedded Administrator is the least-privileged role for this operation. For role information, see [Consuming tenant admin](/sharepoint/dev/embedded/admin/consuming-tenant-admin).

The service must support SharePoint Embedded Data Access Governance reports. Report operations fail in environments where the required backend support hasn't been deployed.

**Report scope**

A `SitePermissions` job captures a permissions snapshot across all eligible SharePoint Embedded containers in the connected consuming tenant, including all applications and container types. It doesn't include regular SharePoint sites or OneDrive accounts. The cmdlet doesn't accept application, container-type, or container filters.

Containers in a `NoAccess` lock state and archived containers are excluded. Unlocked containers and containers in a `ReadOnly` lock state are included.

**Licensing and supported environments**

The report has the same licensing requirements and supported-cloud scope as the existing [Site Permissions report](/sharepoint/data-access-governance-site-permissions-report). The licensing requirements in [Prerequisites for SharePoint Advanced Management](/sharepoint/sharepoint-advanced-management-prerequisites) apply.

As with existing [Data access governance reports](/sharepoint/data-access-governance-reports), the report isn't available for Microsoft 365 operated by 21Vianet, even with the required licenses. In supported environments, SharePoint Embedded reporting backend support must also be deployed.

**Service limits**

The report uses the same generation, retention, frequency, export, and concurrent-job policies as the existing [Site Permissions report](/sharepoint/data-access-governance-site-permissions-report):

- The first report takes up to 5 days to complete.
- Subsequent reports complete within 24 hours.
- Report data can be up to 48 hours old.
- Reports can be run again every 30 days.
- The downloaded CSV can contain up to 1 million containers.

Report retention and concurrent-job limits are controlled by the reporting service. This cmdlet doesn't provide parameters to change those policies.

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

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### Microsoft.Online.SharePoint.PowerShell.SPDataGovernanceInsightMetadata

Report metadata with `ReportId` and `Status` properties.

## NOTES

## RELATED LINKS

[Get-SPOContainerDataAccessGovernanceJob](./Get-SPOContainerDataAccessGovernanceJob.md)

[Export-SPOContainerDataAccessGovernanceJob](./Export-SPOContainerDataAccessGovernanceJob.md)

[Remove-SPOContainerDataAccessGovernanceJob](./Remove-SPOContainerDataAccessGovernanceJob.md)

[Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md)
