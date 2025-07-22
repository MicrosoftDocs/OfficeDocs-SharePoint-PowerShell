---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/find-spocrosstenantlongfilepathsforsiterename
schema: 2.0.0
author: vgaddam-pm
ms.author: vgaddam
ms.reviewer: jmcdowe
---

# Find-SPOCrossTenantLongFilePathsForSiteRename

## SYNOPSIS

Finds sites that exceed the 400 character limit for Cross Tenant User Migration moves.

## SYNTAX

```
Find-SPOCrossTenantLongFilePathsForSiteRename
  [-OldSiteUrl <String>]
  [-NewSiteUrl <String>]
  [<CommonParameters>]
```

## DESCRIPTION
SharePoint Cross Tenant User Migration has a restriction where the source tenant site's file path should not exceed 400 characters in length after merging to the target side. This cmdlet finds sites that exceed the 400 character limit.

## EXAMPLES

### Example 1
```powershell
PS C:\Users\vmadministrator> $SourceSiteUrl = "https://prepspo.spgrid.com/sites/CommTest1"
PS C:\Users\vmadministrator> $TargetSiteUrl = "https://Tenanta24a16f05d204f3bafbfd10ceb259ab9.spgrid.com/sites/CommTest1_longerUrlFor400CharsLimitation"
PS C:\Users\vmadministrator> Find-SPOCrossTenantLongFilePathsForSiteRename -OldSiteUrl $SourceSiteUrl -NewSiteUrl $TargetSiteUrl
```
Output:

List of internal components with too long paths for Cross-tenant migration of the source site [https://prepspo.spgrid.com/sites/CommTest1]
into the target relative url [/sites/CommTest1_longerUrlFor400CharsLimitation] with the relative delta [31]:

1) - sites/CommTest1/Shared Documents/Level1LongFolderNameFor400CharLimitValidationTesting/Level2LongFolderNameFor400CharLimitValidationTesting/Level3LongFolderNameFor400CharLimitValidationTesting/Level4LongFolderNameFor400CharLimitValidationTesting/Level5LongFolderNameFor400CharLimitValidationTesting/Level6LongFolderNameFor400CharLimitValidationTesting/Level7LongFolderNameFor400CharLimit/a.txt
2) - sites/CommTest1/Shared Documents/Level1LongFolderNameFor400CharLimitValidationTesting/Level2LongFolderNameFor400CharLimitValidationTesting/Level3LongFolderNameFor400CharLimitValidationTesting/Level4LongFolderNameFor400CharLimitValidationTesting/Level5LongFolderNameFor400CharLimitValidationTesting/Level6LongFolderNameFor400CharLimitValidationTesting/Level7LongFolderNameFor400CharLimit

### Example 2

```powershell
PS C:\Users\vmadministrator> $SourceSiteUrl = "https://prepspo.spgrid.com/sites/CommTest1"
PS C:\Users\vmadministrator> $TargetSiteUrl = "https://Tenanta24a16f05d204f3bafbfd10ceb259ab9.spgrid.com/sites/CommTest1_longer"
PS C:\Users\vmadministrator> Find-SPOCrossTenantLongFilePathsForSiteRename -OldSiteUrl $SourceSiteUrl -NewSiteUrl $TargetSiteUrl
```
Output:

List of internal components with too long paths for Cross-tenant migration of the source site [https://prepspo.spgrid.com/sites/CommTest1]
into the target relative url [/sites/CommTest1_longer] with the relative delta [7]:
  
No problem found

## PARAMETERS

### -NewSiteUrl
This parameter includes the source site URL

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OldSiteUrl
This parameter includes the target site URL

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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
