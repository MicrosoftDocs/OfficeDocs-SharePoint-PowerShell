---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/export-spocontainerdataaccessgovernancejob
applicable: SharePoint Online
title: Export-SPOContainerDataAccessGovernanceJob
schema: 2.0.0
---

# Export-SPOContainerDataAccessGovernanceJob

## SYNOPSIS

Downloads a completed SharePoint Embedded Data Access Governance report.

## SYNTAX

```
Export-SPOContainerDataAccessGovernanceJob -ReportID <Guid> [-DownloadPath <String>] [<CommonParameters>]
```

## DESCRIPTION

The `Export-SPOContainerDataAccessGovernanceJob` cmdlet downloads a completed report to a local folder. Use `Get-SPOContainerDataAccessGovernanceJob` to confirm that the report status is `Completed`.

The cmdlet checks that the report belongs to SharePoint Embedded and is completed before downloading its content. SharePoint and OneDrive report IDs aren't accepted.

Specify a folder, not a file name, for `DownloadPath`. The file name is derived from the report metadata. If you omit the path, the cmdlet uses the current user's Downloads folder, which must exist. A specified folder is created if it doesn't exist. An existing file with the same name isn't overwritten.

Connect to the tenant administration endpoint with `Connect-SPOService` before running this cmdlet. The service must support SharePoint Embedded Data Access Governance reports, and the signed-in account must be authorized to download them.

## EXAMPLES

### Example 1

```powershell
Export-SPOContainerDataAccessGovernanceJob -ReportID 28f4c550-215a-472b-a123-c11e5fa8804c -DownloadPath "C:\Reports" -ErrorAction Stop
```

This example downloads a completed report to `C:\Reports`. Replace the example ID with the ID of your report.

### Example 2

```powershell
Export-SPOContainerDataAccessGovernanceJob -ReportID 28f4c550-215a-472b-a123-c11e5fa8804c
```

This example downloads the report to the current user's Downloads folder.

## PARAMETERS

### -DownloadPath

Specifies the destination folder for the downloaded report. If omitted, the current user's Downloads folder is used.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportID

Specifies the ID of a completed SharePoint Embedded report.

```yaml
Type: System.Guid
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

### System.String

A success message containing the downloaded file path.

## NOTES

## RELATED LINKS

[Connect-SPOService](./Connect-SPOService.md)

[Start-SPOContainerDataAccessGovernanceJob](./Start-SPOContainerDataAccessGovernanceJob.md)

[Get-SPOContainerDataAccessGovernanceJob](./Get-SPOContainerDataAccessGovernanceJob.md)

[Remove-SPOContainerDataAccessGovernanceJob](./Remove-SPOContainerDataAccessGovernanceJob.md)
