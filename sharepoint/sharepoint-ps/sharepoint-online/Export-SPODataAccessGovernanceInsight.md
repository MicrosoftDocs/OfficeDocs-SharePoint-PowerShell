---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/export-spodataaccessgovernanceinsight
applicable: SharePoint Online
title: Export-SPODataAccessGovernanceInsight
schema: 2.0.0
author: pvrk
ms.author: pullabhk
manager: 
ms.reviewer:
---

# Export-SPODataAccessGovernanceInsight

## SYNOPSIS

This cmdlet downloads the Data Access Governance (DAG) reports to the specified path. The default is the "Downloads" folder.

## SYNTAX

```
Export-SPODataAccessGovernanceInsight -ReportID <Guid> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet exports or downloads the DAG report, specified by the `ReportID`, to the path as specified with `DownloadPath`. If not specified, the commands downloads the report to the "Downloads" folder. The `ReportID` is shown in the output of the [Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md) command. It can also be fetched from the output of the [Get-SPODataAccessGovernanceInsight](./Get-SPODataAccessGovernanceInsight.md) command.

## EXAMPLES

### Example 1

```powershell
Export-SPODataAccessGovernanceInsight -ReportID 28f4c550-215a-472b-a123-c11e5fa8804c
```

The above example downloads the report of the given ID to the current working directory.

## PARAMETERS

### -ReportID

Specifies the ID of the DAG report to be downloaded.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DownloadPath

Specifies the path to which the report should be downloaded. The default path is the "Downloads" folder.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

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

[Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md)

[Get-SPODataAccessGovernanceInsight](./Get-SPODataAccessGovernanceInsight.md)

[Remove-SPODataAccessGovernanceInsight](./Remove-SPODataAccessGovernanceInsight.md)

[Start-SPOSiteReview](./Start-SPOSiteReview.md)

[Get-SPOSiteReview](./Get-SPOSiteReview.md)
