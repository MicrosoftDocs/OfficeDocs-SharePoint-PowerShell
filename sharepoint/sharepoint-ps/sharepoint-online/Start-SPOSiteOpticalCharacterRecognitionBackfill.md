---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Start-SPOSiteOpticalCharacterRecognitionBackfill
applicable: SharePoint Online
title: Start-SPOSiteOpticalCharacterRecognitionBackfill
schema: 2.0.0
author: FarreltinF
ms.author: fanyi
ms.reviewer:
---

# Start-SPOSiteOpticalCharacterRecognitionBackfill

## SYNOPSIS

> [!NOTE]
> This feature - Optical Character Recognition (OCR) is a pay-as-you-go feature, triggering this cmdlet will incur cost for your organization

Initiates a job to trigger the Optical Character Recognition (OCR) process for all files for the selected site.

## SYNTAX

```Powershell

Start-SPOSiteBackfillOCR [-Site] <string> 
```

## DESCRIPTION

This command starts a job to trigger the Optical Character Recognition (OCR) process for files that have either never been OCR processed or have been modified since the last OCR process. This ensures all relevant content in the site is recognized and indexed for improved searchability and accessibility. 

OCR backfill can only be run on OCR-enabled sites. If OCR is disabled for the site, please enable OCR before proceeding with OCR backfilling. Refer to this [article](https://learn.microsoft.com/en-us/microsoft-365/syntex/ocr) for instructions on enabling OCR on the selected site.

## EXAMPLES

### EXAMPLE 1

```powershell

Start-SPOSiteBackfillOCR -Site https://contosoenergy.sharepoint.com/sites/hr
```

Starts OCR process for all content hasn't been processed before in the selected site.

### EXAMPLE 2

```powershell

$site = Get-SPOSIte -Identity https://contosoenergy.sharepoint.com/sites/hr
Start-SPOSiteBackfillOCR -Site $site 
```

Start OCR process for all content hasn't been processed before in the selected site.

## PARAMETERS

### -Site

Specifies the site URL where OCR process should be enabled on.

```yaml
Type: String
Parameter Sets: Default
Aliases:
Applicable: SharePoint Online

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Overview of optical character recognition in SharePoint](https://learn.microsoft.com/en-us/microsoft-365/syntex/ocr-overview)

[Learn about optical character recognition in Microsoft Purview](https://learn.microsoft.com/en-us/purview/ocr-learn-about?tabs=purview)
