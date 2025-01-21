---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/start-spositereview
applicable: SharePoint Online
title: Start-SPOSiteReview
schema: 2.0.0
author: pvrk
ms.author: pullabhk
manager: 
ms.reviewer:
---

# Start-SPOSiteReview

## SYNOPSIS
SharePoint Administrators can delegate access governance of sites to corresponding site owners through 'site access review'. The 'access review' is under the context of oversharing as specified in the Data Access Governance (DAG) reports. Read all about site access review [here](/sharepoint/site-access-review).

## SYNTAX

```
Start-SPOSiteReview -ReportID <Guid> -SiteID <Guid> [-Comment <String>] [<CommonParameters>]
```

## DESCRIPTION
Initiates a 'site access review' request to all the site owners under the context of the DAG report. The request is sent via email to all site owners with comments given by SharePoint Administrator.

## EXAMPLES

### Example 1

```powershell
PS C:\> Start-SPOSiteReview -ReportID 03327d1c-38c5-4c32-9dad-85753a682d65 -SiteID a10f1997-71f2-4ef2-825e-2439400fc601 -comment "check for EEEU access"
```

The above cmdlet initiates site access review for the given site as per oversharing criteria mentioned in the given DAG report.

## PARAMETERS

### -Comment
SharePoint Administrator to add comments to provide more context to the site owner regarding the purpose of the review.

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

### -ReportID
Specifies the ID of the particular report which contains sites for which site access review should be initiated.

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

### -SiteID
Specifies the ID of the site for which site access review should be initiated.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Site access review for DAG reports](/sharepoint/site-access-review)

[Get-SPOSiteReview](./Get-SPOSiteReview.md)

[Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md)

[Export-SPODataAccessGovernanceInsight](./Export-SPODataAccessGovernanceInsight.md)

[Get-SPODataAccessGovernanceInsight](./Get-SPODataAccessGovernanceInsight.md)

[Remove-SPODataAccessGovernanceInsight](./Remove-SPODataAccessGovernanceInsight.md)
