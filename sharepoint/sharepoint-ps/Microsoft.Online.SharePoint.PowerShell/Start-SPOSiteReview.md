---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/start-spositereview
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
SharePoint Administrators can delegate access governance of sites to corresponding site owners or site collection administrators through 'site access review'. The 'access review' is under the context of oversharing as specified in the Data Access Governance (DAG) reports. Read all about site access review [here](/sharepoint/site-access-review).

## SYNTAX

```
Start-SPOSiteReview -ReportID <Guid> -SiteID <Guid> [-Comment <String>]
 [-DeliveryMode <SiteReviewEmailDeliveryMode>]
 [-RecipientRole <SiteReviewRecipientRoleParameter>] [<CommonParameters>]
```

## DESCRIPTION
Initiates a 'site access review' request under the context of the DAG report. By default, the request is sent via email to all site owners. Use `-RecipientRole` to send the request to site owners, site collection administrators, or both. Comments provided by the SharePoint Administrator are included with the request.

## EXAMPLES

### Example 1

```powershell
PS C:\> Start-SPOSiteReview -ReportID 03327d1c-38c5-4c32-9dad-85753a682d65 -SiteID a10f1997-71f2-4ef2-825e-2439400fc601 -comment "check for EEEU access"
```

The above cmdlet initiates site access review for the given site as per oversharing criteria mentioned in the given DAG report.

### Example 2

```powershell
PS C:\> Start-SPOSiteReview -ReportID 03327d1c-38c5-4c32-9dad-85753a682d65 -SiteID a10f1997-71f2-4ef2-825e-2439400fc601 -DeliveryMode SingleEmail
```

The above cmdlet initiates site access review and notifies the reviewers with a single grouped email instead of one email per reviewer. Reviewers are grouped by their notification language, so one email is sent for each language used by the reviewers.

### Example 3

```powershell
PS C:\> Start-SPOSiteReview -ReportID 03327d1c-38c5-4c32-9dad-85753a682d65 -SiteID a10f1997-71f2-4ef2-825e-2439400fc601 -RecipientRole All
```

The above cmdlet initiates site access review and sends the request to both the site owners and site collection administrators. A person who belongs to both groups is included only once.

## PARAMETERS

### -Comment
SharePoint Administrator to add comments to provide more context to the reviewers regarding the purpose of the review.

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
Specifies the ID of the particular report which contains sites for which site access review should be initiated.

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

### -SiteID
Specifies the ID of the site for which site access review should be initiated.

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

### -DeliveryMode
Specifies how the reviewers are notified for this site access review.

The acceptable values for this parameter are:

- Individual: Each reviewer receives a separate email. This is the behavior when the parameter is omitted.
- SingleEmail: The reviewers receive a single grouped email instead of one email each. Reviewers are grouped by their notification language, so one email is sent for each language used by the reviewers.

If a custom email template is configured for site access reviews in your organization, the grouping setting on that template determines how the reviewers are notified, and it takes precedence over this parameter.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SiteReviewEmailDeliveryMode
Parameter Sets: (All)
Aliases:
Accepted values: Individual, SingleEmail

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecipientRole
Specifies who receives the site access review request.

The acceptable values for this parameter are:

- SiteOwners: Sends the request to members of the site's owner group. This is the default behavior when the parameter is omitted and no recipient role is configured on the email template.
- SiteAdmins: Sends the request to the site collection administrators.
- All: Sends the request to both the site owners and site collection administrators. A person who is both an owner and an administrator is included only once.

If a custom email template is configured for site access reviews in your organization, the recipient role on that template determines who receives the request and takes precedence over this parameter.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SiteReviewRecipientRoleParameter
Parameter Sets: (All)
Aliases:
Accepted values: SiteOwners, SiteAdmins, All

Required: False
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

### System.Object

## NOTES

## RELATED LINKS

[Site access review for DAG reports](/sharepoint/site-access-review)

[Get-SPOSiteReview](./Get-SPOSiteReview.md)

[Start-SPODataAccessGovernanceInsight](./Start-SPODataAccessGovernanceInsight.md)

[Export-SPODataAccessGovernanceInsight](./Export-SPODataAccessGovernanceInsight.md)

[Get-SPODataAccessGovernanceInsight](./Get-SPODataAccessGovernanceInsight.md)

[Remove-SPODataAccessGovernanceInsight](./Remove-SPODataAccessGovernanceInsight.md)
