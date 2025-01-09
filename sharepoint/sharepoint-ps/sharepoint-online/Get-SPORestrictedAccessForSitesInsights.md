---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-sporestrictedaccessforsitesinsights
applicable: SharePoint Online
title: Get-SPORestrictedAccessForSitesInsights
schema: 2.0.0
author: ishwarit
ms.author: itambakhe
ms.reviewer:
manager:
---

# Get-SPORestrictedAccessForSitesInsights

## SYNOPSIS

This cmdlet enables the administrator to check status of all active and available reports about insights on sites protected and access denials by restricted access control.

## SYNTAX

```powershell
Get-SPORestrictedAccessForSitesInsights -RACProtectedSites [-ReportId <Guid>] [-FullDetails] [-Action <ActionType>] [-InsightsSummary <Boolean>]
```

## SYNTAX

```powershell
Get-SPORestrictedAccessForSitesInsights -ActionsBlockedByPolicy [-ReportId <Guid>] [-Content <ContentType>] [-Action <ActionType>]
```

## DESCRIPTION

If this cmdlet is executed with `-RACProtectedSites` as parameter, it displays the status of all the active and completed reports.

If this cmdlet is executed with `-RACProtectedSites` `-ReportId` as parameter, top 100 sites with the highest page views that are protected by restricted access control will be displayed.

If this cmdlet is executed with `-RACProtectedSites` `-ReportId` `-FullDetails` `-Action Download`, a CSV file containing list of up to 1 million sites protected by restricted access control will be downloaded.

If this cmdlet is executed with `-RACProtectedSites` `-ReportId` `-InsightsSummary` as parameter, the count of sites protected with restricted access control compared to total number of sites will be displayed.

If this cmdlet is executed with `-ActionsBlockedByPolicy` as parameter, it displays the status of all active and completed reports.
  
If this cmdlet is executed with `-ActionsBlockedByPolicy` `-ReportId` `-Content TopSites` as parameter, top 100 sites with the highest access denials by restricted access control will be displayed.

If this cmdlet is executed with `-ActionsBlockedByPolicy` `-ReportId` `-Content TopUsers` as parameter, top 10 users with the highest access denials by restricted access control will be displayed.

If this cmdlet is executed with `-ActionsBlockedByPolicy` `-ReportId` `-Content AllDenials` as parameter, most recent 100 access denials by restricted access control in the last 28 days will be displayed.

If this cmdlet is executed with `-ActionsBlockedByPolicy` `-ReportId` `-Content SiteDistribution` as parameter, distribution of access denials by restricted access control on different site types will be displayed.

> [!NOTE]
> All reports adhere to any retention timeline as per [Data Access Governance](/sharepoint/data-access-governance-reports).

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPORestrictedAccessForSitesInsights -RACProtectedSites
```

Example 1 enables administrator to view the status of all active and completed reports on list of sites protected with restricted access control.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Get-SPORestrictedAccessForSitesInsights –RACProtectedSites -ReportId 9d946216-afe7-49f5-8267-7b662435c70b
```

Example 2 enables administrator to view the report containing list of sites protected with restricted access control with ReportId: `9d946216-afe7-49f5-8267-7b662435c70b`

### -----------------------EXAMPLE 3-----------------------------

```powershell
Get-SPORestrictedAccessForSitesInsights -ActionsBlockedByPolicy -ReportId 9d946216-afe7-49f5-8267-7b662435c70b -Content TopSites
```

Example 3 enables administrator to view the report containing top sites with access denials due to restricted access control with ReportId: `9d946216-afe7-49f5-8267-7b662435c70b`.

## PARAMETERS

### -RACProtectedSites

It is an optional parameter, and it specifies the type of report to be viewed or downloaded.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActionsBlockedByPolicy

It is an optional parameter, and it specifies the type of report to be viewed or downloaded.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportId

It is an optional parameter, and it specifies the unique Id of the report to be viewed or downloaded.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InsightsSummary

It is an optional parameter, and it specifies the subtype of the report to be viewed or downloaded.

```yaml
Type: Bool
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -Content

It is an optional parameter, and it specifies the subtype of the report to be viewed or downloaded.

```yaml
Type: ContentType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Action

It is an optional parameter, and it specifies whether to view or download a specific report.

```yaml
Type: ActionType
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullDetails

It is an optional parameter and allows to download a CSV file containing up to 1 million records.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Start-SPORestrictedAccessForSitesInsights](./Start-SPORestrictedAccessForSitesInsights.md)
