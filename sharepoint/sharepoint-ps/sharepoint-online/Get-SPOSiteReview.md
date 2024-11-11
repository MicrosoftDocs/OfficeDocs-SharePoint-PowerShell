---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
author: MachelleTranMSFT
ms.author: mactra
ms.reviewer: pullabhk
---

# Get-SPOSiteReview

## SYNOPSIS

This command retrieves the site review report.

## SYNTAX

```powershell
Get-SPOSiteReview [-SiteReviewID <Guid>] [-Status <SiteReviewStatus>]
 [-ReportEntity <SiteAccessReportEntityEnum>] [-SiteID <Guid>] [<CommonParameters>]
```

## DESCRIPTION

{{ Fill in the Description }}

## EXAMPLES

### Example 1

```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -ReportEntity

{{ Fill ReportEntity Description }}

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

{{ Fill SiteID Description }}

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

{{ Fill SiteReviewID Description }}

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

{{ Fill Status Description }}

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
