---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: 
applicable: SharePoint Online
title: Start-SPOEnterpriseAppInsightsReport
schema: 
author: sumikumar
ms.author: sumikumar
ms.reviewer:
manager: hikakar
---

# Get-SPOEnterpriseAppInsightsReport

## SYNOPSIS

This cmdlet enables the admin to check status of all active & available reports when no report ID is present and to View a Report if report ID is present.

## SYNTAX

```powershell
Get-SPOEnterpriseAppInsightsReport [-ReportId<Guid>] [-Action<enum>]
```

## Description

After this cmdlet is executed, the report of last N days will be displayed with the following properties:
| Property             | Description                              |
| :------------------- | :--------------------------------------- |
| SiteName | The name of the SharePoint Site.                    |
| SiteURL               | The URL of the SharePoint Site.                   |
| SiteSensitivity | The Sensitivity Label of the SharePoint Site.               |
| AppID | The AppID of the 3P App.       |
| AppPermissions| The Permissions granted to the 3P App. |
| RequestVoulme | The number of times the 3P accessed the given SharePoint Site.          |
  
## Example

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPOEnterpriseAppInsightsReport
```

Example 1 enables admin to view latest reportID and corresponding status for each duration and adhering to any retention timeline as per DAG.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Get-SPOEnterpriseAppInsightsReport – ReportId 9d946216-afe7-49f5-8267-7b662435c70b
```

Example 2 enables admin to view the app insights report of ReportId: 9d946216-afe7-49f5-8267-7b662435c70b

### -----------------------EXAMPLE 3-----------------------------

```powershell
Get-SPOEnterpriseAppInsightsReport – ReportId 9d946216-afe7-49f5-8267-7b662435c70b -Action Download
```

Example 3 enables admin to download the app insights report of ReportId: 9d946216-afe7-49f5-8267-7b662435c70b

## PARAMETERS

### - ReportId

It is an optional parameter, and it specifies the unique Id of the report to be viewed/downloaded.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - Action

It is an optional parameter, and it specifies whether to view or download a specific report.

```yaml
Type: enum
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## CommonParameters

## Related Links
