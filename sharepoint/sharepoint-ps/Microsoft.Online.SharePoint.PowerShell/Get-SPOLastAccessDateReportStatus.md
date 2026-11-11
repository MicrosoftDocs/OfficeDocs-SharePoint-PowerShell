---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spolastaccessdatereportstatus
applicable: SharePoint Online
title: Get-SPOLastAccessDateReportStatus
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
manager: brgussin
ai-usage: ai-generated
---

# Get-SPOLastAccessDateReportStatus

## SYNOPSIS

Gets the overall or per-site progress of a file last access date report request.

## SYNTAX

```
Get-SPOLastAccessDateReportStatus [-RunId] <Guid> [-Site <SpoSitePipeBind[]>]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet gets the status of a report request created by `Start-SPOLastAccessDateReport`.

By default, it returns a request summary and the number of sites in each processing state. Use `-Site` to get the status of specific sites. Review failures before exporting the report.

You need the SharePoint Advanced Management Administrator role to run this cmdlet. App-only authentication requires `Sites.FullControl.All`.

Report requests remain available for 15 days after submission.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOLastAccessDateReportStatus -RunId $report.RunId
```

This example gets the overall progress for a request returned by `Start-SPOLastAccessDateReport`.

### EXAMPLE 2

```powershell
Get-SPOLastAccessDateReportStatus -RunId $report.RunId -Site "https://contoso.sharepoint.com/sites/marketing"
```

This example gets the request's status for one site, including its attempt count and failure reason.

### EXAMPLE 3

```powershell
Get-SPOSite -Filter "Url -like '*marketing*'" | Get-SPOLastAccessDateReportStatus -RunId $report.RunId
```

This example gets per-site status for the sites returned by `Get-SPOSite`. A site outside this request returns `NotFound`.

## PARAMETERS

### -RunId

> Applicable: SharePoint Online

Specifies the request identifier returned by `Start-SPOLastAccessDateReport`. The identifier must not be an empty GUID.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site

> Applicable: SharePoint Online

Specifies site collections by URL, site ID, `SPOSite` object, or `SPODeletedSite` object.

Omit this parameter to get the overall request summary.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind[]

You can pipe site objects to this cmdlet.

## OUTPUTS

### Microsoft.Online.SharePoint.PowerShell.SPOLastAccessDateReportRequestStatus

Without `-Site`, the cmdlet returns these summary properties:

| Property | Description |
|---|---|
| `RunId` | Identifies the request. |
| `Mode` | Identifies the processing mode. |
| `RequestedUtc` | Records when the request was submitted, in UTC. |
| `TotalSites` | Counts the sites in the request. |
| `NotStarted` | Counts sites waiting for processing. |
| `InProgress` | Counts sites currently being processed. |
| `Retrying` | Counts sites awaiting another processing attempt after a transient failure. |
| `Completed` | Counts sites with completed reports. |
| `Failed` | Counts sites without usable reports. |
| `PackageState` | Reports `RunNotFinished`, `NotRequested`, `Packaging`, `Ready`, or `Failed`. |
| `PackageUrl` | Identifies the package location when ready. Use the export cmdlet to download it. |

`PackageState = Ready` means the package is available. It doesn't mean every requested site produced a report.

| PackageState | Description |
|---|---|
| `RunNotFinished` | Sites are still queued, processing, or retrying. Wait before exporting. |
| `NotRequested` | Run `Export-SPOLastAccessDateReport` to prepare the download. |
| `Packaging` | The service is building the ZIP. Wait before exporting. |
| `Ready` | The package is available. Use Export to download the ZIP and index. |
| `Failed` | Run `Export-SPOLastAccessDateReport` to try preparing the download again. |

### Microsoft.Online.SharePoint.PowerShell.SPOLastAccessDateReportStatusInfo

With `-Site`, the cmdlet returns `RunId`, `SiteUrl`, `SiteId`, `Status`, `AttemptCount`, and `FailureReason`.

| Status | Description |
|---|---|
| `Queued` | The site is waiting for processing. |
| `InProgress` | The service is processing the site. |
| `Retrying` | The service is retrying after a transient failure. Review `FailureReason`. |
| `Completed` | The service produced the site's report. |
| `Failed` | The service didn't produce a usable report. Review `FailureReason`. |
| `NotFound` | The request doesn't contain the site, or the request is no longer available. |

## NOTES

Processing runs asynchronously. Allow time between status checks rather than repeatedly submitting new report requests.

## RELATED LINKS

[Generate a file last access date report](/microsoft-365/archive/file-last-access-date-report)

[Start-SPOLastAccessDateReport](Start-SPOLastAccessDateReport.md)

[Export-SPOLastAccessDateReport](Export-SPOLastAccessDateReport.md)
