---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/export-spolastaccessdatereport
applicable: SharePoint Online
title: Export-SPOLastAccessDateReport
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
manager: johmar
ai-usage: ai-generated
---

# Export-SPOLastAccessDateReport

## SYNOPSIS

Downloads completed file last access date reports as a ZIP file and a JSON index.

## SYNTAX

```
Export-SPOLastAccessDateReport [-RunId] <Guid> [[-Path] <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The `Export-SPOLastAccessDateReport` cmdlet downloads reports for a request submitted by `Start-SPOLastAccessDateReport`.

The service packages reports after site processing finishes. Export requests packaging if it was never queued or previously failed.

When the package is ready, Export downloads `LastAccessDateReport_<RunId>.zip` and `LastAccessDateReport_<RunId>.index.json`. It verifies the ZIP's size and SHA-256 hash.

The ZIP contains a CSV report for each completed site. Failed sites aren't included in the ZIP. Review the JSON index for included sites, missing reports, and their reasons.

An interrupted ZIP download resumes on the next call. The index downloads again in full.

Export retries transient download errors separately for each file. Each file gets up to five attempts and five minutes of total waiting between attempts. If the server remains busy, run Export again later.

Export saves both files under temporary names, then moves them into place together. Use `-Force` if either destination file already exists.

With `-Force`, Export keeps previous files as `.bak` files until their replacements are in place. A warning lists any `.bak` files remaining from an earlier export.

Use an account with the SharePoint Advanced Management Administrator role. Global Administrator, SharePoint Administrator, and Global Reader roles alone don't grant permission to run this cmdlet.

App-only access requires `Sites.FullControl.All`. Export requires Update permission on Advanced Management reports because it can request packaging. Downloads through this cmdlet don't require separate permission on the report storage location.

Your tenant and SharePoint Online Management Shell version must support this cmdlet. An unsupported tenant returns an experimental-feature error.

## EXAMPLES

### EXAMPLE 1

```powershell
Export-SPOLastAccessDateReport -RunId $report.RunId
```

This example downloads the report package to the current folder when the package is ready.

If Export returns `Packaging`, wait before running it again. If it returns `RunNotFinished`, check site progress with `Get-SPOLastAccessDateReportStatus`.

### EXAMPLE 2

```powershell
Export-SPOLastAccessDateReport -RunId $report.RunId -Path "C:\Reports" -Force
```

This example downloads both files to the existing `C:\Reports` folder. It allows Export to replace an existing ZIP or index.

## PARAMETERS

### -RunId

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

### -Path

Specifies an existing local folder for the downloaded files. The default is the current file system folder.

This parameter specifies a folder, not a ZIP filename. Export doesn't create the folder.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: Current file system folder
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Allows Export to overwrite an existing local ZIP or JSON index for this request. Without this parameter, Export stops if either file exists.

Export keeps previous files as `.bak` files until both replacements are in place.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen without exporting the reports.

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

Prompts for confirmation before exporting the reports. This medium-impact cmdlet doesn't prompt by default with the standard confirmation preference.

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

### Microsoft.Online.SharePoint.PowerShell.SPOLastAccessDateReportExportResult

The returned object contains these properties:

| Property | Description |
|---|---|
| `RunId` | Identifies the request. |
| `State` | Reports whether processing, packaging, or download can complete. |
| `FilePath` | Identifies the local ZIP when the download succeeds. |
| `IndexFilePath` | Identifies the downloaded JSON index. |
| `SizeBytes` | Gives the package size. |
| `Sha256` | Gives the package's SHA-256 hash. |
| `SiteCount` | Counts the sites in the request. |
| `IncludedSiteCount` | Counts sites included in the package. |
| `MissingSiteCount` | Counts sites without included reports. |
| `Detail` | Provides additional status information. |

| State | Description |
|---|---|
| `RunNotFinished` | Sites are still queued, processing, or retrying. Check request status and wait. |
| `Packaging` | Packaging is underway, or this call requested it. Wait a few minutes before exporting again. |
| `Ready` | Export downloaded the ZIP and index and verified the ZIP's size and SHA-256 hash. Review the index for missing site reports. |
| `Failed` | Packaging failed, and this call already requested another attempt. Review the warning and `Detail`. Wait a few minutes before exporting again. |

## NOTES

The service retains request records for 15 days after submission. Export reports before the request expires.

Report data has a 30-day retention period, but the service doesn't currently delete report files automatically. Report files remain until manually removed.

Reports contain file names, URLs, and access dates. Protect downloaded files according to your organization's data-handling requirements.

Each completed site's CSV contains these columns:

| Column | Description |
|---|---|
| `FileId` | Identifies the file. |
| `FileName` | Gives the filename, including its extension. |
| `FileType` | Gives the file extension. |
| `FileUrl` | Gives the file's absolute URL. |
| `LastAccessDate` | Gives the effective recorded last access date. |
| `SDSLastAccessDate` | Gives the underlying SDS access-date signal. |
| `DocumentAnalyticsLastActivityTimestamp` | Gives the last activity timestamp from document analytics. |
| `FileModifiedTime` | Gives the last modified time. |

Dates use UTC. Unavailable dates are empty.

## RELATED LINKS

[Generate a file last access date report](/microsoft-365/archive/file-last-access-date-report)

[Start-SPOLastAccessDateReport](Start-SPOLastAccessDateReport.md)

[Get-SPOLastAccessDateReportStatus](Get-SPOLastAccessDateReportStatus.md)
