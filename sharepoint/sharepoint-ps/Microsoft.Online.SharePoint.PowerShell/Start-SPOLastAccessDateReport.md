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
manager: johmar
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

The `Start-SPOLastAccessDateReport` cmdlet submits a request and returns its `RunId`. Use `Get-SPOLastAccessDateReportStatus` to track progress and `Export-SPOLastAccessDateReport` to download the results.

The `Sampling` mode supports up to 1,000 sites per request and up to 1,000 files per site. It doesn't select files by age or access date. The sample isn't a complete inventory or a list of files eligible for archiving.

Processing runs asynchronously. The service packages reports after site processing finishes. The service retains requests for 30 days.

If another request already processes a site, this cmdlet skips that site and returns a warning with the existing `RunId`. The `SitesAlreadyInProgress` property also identifies skipped sites.

If every site is already being processed, the cmdlet returns `AlreadyInProgress` and queues no new sites. The returned `RunId` belongs to the existing request for the first skipped site. Review `SitesAlreadyInProgress` because other sites might belong to different requests.

Use an account with the SharePoint Advanced Management Administrator role. The Global Administrator and SharePoint Administrator roles alone don't grant permission to run this cmdlet.

Your tenant and SharePoint Online Management Shell version must support this cmdlet. An unsupported tenant returns an experimental-feature error.

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

This cmdlet supports the common parameters. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

This cmdlet doesn't accept pipeline input.

## OUTPUTS

### Microsoft.Online.SharePoint.PowerShell.SPOLastAccessDateReportRequest

The returned object contains these properties:

| Property | Description |
|---|---|
| `RunId` | Identifies the request to use with the status and export cmdlets. |
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
