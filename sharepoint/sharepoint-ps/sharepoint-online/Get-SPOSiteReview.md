---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositereview
applicable: SharePoint Online
title: Get-SPOSiteReview
schema: 2.0.0
author: pvrk
ms.author: pullabhk
manager: 
ms.reviewer:
---

# Get-SPOSiteReview

## SYNOPSIS
Track all site access reviews initiated from Data Access Governance (DAG) reports.

## SYNTAX

```
Get-SPOSiteReview [-SiteReviewID <Guid>] [-Status <SiteReviewStatus>] [-ReportEntity <SiteAccessReportEntityEnum>] [-SiteID <Guid>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet fetches details of a particular access review or a group of access reviews as per the filtering criteria.

## EXAMPLES

### Example 1
```powershell
Get-SPOSiteReview -ReportEntity PermissionedUsers
```

The above cmdlet retrieves all site access reviews raised under all 'Permissioned user' snapshot reports.

## PARAMETERS

### -ReportEntity
Specifies the entity that could cause oversharing and hence tracked by these reports.

```yaml
Type: SiteAccessReportEntityEnum
Parameter Sets: (All)
Aliases:
Accepted values: All, SharingLinks_Anyone, SharingLinks_PeopleInYourOrg, SharingLinks_Guests, SensitivityLabelForFiles, EveryoneExceptExternalUsersAtSite, EveryoneExceptExternalUsersForItems, PermissionedUsers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteID
Specifies the ID of the site for which access reviews were initiated.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteReviewID
Specifies the ID of the particular access review.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Specifies the current status of the site access review.

```yaml
Type: SiteReviewStatus
Parameter Sets: (All)
Aliases:
Accepted values: All, Pending, Failed, Completed

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

[Site access review for DAG reports](/sharepoint/site-access-review)

[Start-SPOSiteReview](./Start-SPOSiteReview.md)

[Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md)

[Get-SPODataAccessGovernanceInsight](./Get-SPODataAccessGovernanceInsight.md)

[Export-SPODataAccessGovernanceInsight](./Export-SPODataAccessGovernanceInsight.md)

[Remove-SPODataAccessGovernanceInsight](./Remove-SPODataAccessGovernanceInsight.md)
