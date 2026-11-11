---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/start-spolastaccessdatereport
applicable: SharePoint Online
title: Start-SPOLastAccessDateReport
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
manager: brgussin
ai-usage: ai-generated
---

# Start-SPOLastAccessDateReport

## SYNOPSIS

Requests a sample of file last access dates for one or more SharePoint site collections.

## SYNTAX

```
Start-SPOLastAccessDateReport [-Site] <SpoSitePipeBind[]> [-Mode <LastAccessDateReportMode>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet starts a last access date report for the specified SharePoint sites and returns a `RunId`. Use `Get-SPOLastAccessDateReportStatus` to check progress and `Export-SPOLastAccessDateReport` to download the results.

`Sampling` supports up to 1,000 sites per request and samples up to 1,000 files per site. The sample isn't a complete file inventory. Don't use it to identify files eligible for archiving.

Processing can take up to 15 days. Export reports within 15 days of submitting the request.

The cmdlet skips sites already included in an active request. Review `SitesAlreadyInProgress` for skipped sites and their existing requests.

You need the SharePoint Advanced Management Administrator role to run this cmdlet. App-only authentication requires `Sites.FullControl.All`.

## EXAMPLES

### EXAMPLE 1

```powershell
$report = Start-SPOLastAccessDateReport -Site "https://contoso.sharepoint.com/sites/marketing"
$report
```

This example requests a report for one site. The cmdlet prompts for confirmation before submitting the request.

### EXAMPLE 2

```powershell
$sites = @(
    "https://contoso.sharepoint.com/sites/marketing"
    "https://contoso.sharepoint.com/sites/finance"
)
$report = Start-SPOLastAccessDateReport -Site $sites
Get-SPOLastAccessDateReportStatus -RunId $report.RunId
```

This example submits two sites in one request and checks the overall progress. Sites already being processed aren't added again.

### EXAMPLE 3

```powershell
$site = Get-SPOSite -Identity "https://contoso.sharepoint.com/sites/marketing"
Start-SPOLastAccessDateReport -Site $site -WhatIf
```

This example previews a request without submitting it. Pass site objects through `-Site`; this cmdlet doesn't accept pipeline input.

## PARAMETERS

### -Site

> Applicable: SharePoint Online

Specifies one or more site collections by URL, site ID, `SPOSite` object, or `SPODeletedSite` object.

All sites must belong to the connected tenant. A request can contain up to 1,000 sites.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mode

> Applicable: SharePoint Online

Specifies the processing mode. `Sampling` is the only supported value and the default.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.LastAccessDateReportMode
Parameter Sets: (All)
Aliases:
Accepted values: Sampling

Required: False
Position: Named
Default value: Sampling
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Online

Shows what would happen without submitting a report request.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Online

Prompts for confirmation before submitting the request. This high-impact cmdlet prompts by default with the standard confirmation preference.

Use `-Confirm:$false` only when you intend to suppress the prompt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

This cmdlet doesn't accept pipeline input.

## OUTPUTS

### Microsoft.Online.SharePoint.PowerShell.SPOLastAccessDateReportRequest

The returned object contains these properties:

| Property | Description |
|---|---|
| `RunId` | Identifies the request. If all sites are already being processed, identifies the existing request for the first skipped site. |
| `Mode` | Identifies the processing mode. |
| `SiteCount` | Counts the sites queued by this request. |
| `Status` | Returns `Accepted` when sites were queued, or `AlreadyInProgress` when no new sites were queued. |
| `SitesAlreadyInProgress` | Lists skipped sites with their `SiteUrl`, `SiteId`, and existing `RunId`. |

## NOTES

Connect to your tenant's SharePoint admin endpoint with `Connect-SPOService` before running this cmdlet.

## RELATED LINKS

[Generate a file last access date report](/microsoft-365/archive/file-last-access-date-report)

[Get-SPOLastAccessDateReportStatus](Get-SPOLastAccessDateReportStatus.md)

[Export-SPOLastAccessDateReport](Export-SPOLastAccessDateReport.md)

[Connect-SPOService](Connect-SPOService.md)
