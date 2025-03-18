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

> [!important]
> Optical Character Recognition (OCR) is a pay-as-you-go feature, triggering this cmdlet will incur cost for your organization

Initiates a job to trigger the Optical Character Recognition (OCR) process for all files for the selected site.

## SYNTAX

```Powershell

Start-SPOSiteOpticalCharacterRecognitionBackfill [-Site] <string> 
```

## DESCRIPTION

This cmdlet starts a job to trigger the OCR process for files that have either never been OCR processed or have been modified since the last OCR process. This ensures all relevant content in the site is recognized and indexed for improved searchability and accessibility. 

OCR backfill can only be run on OCR-enabled sites. If OCR is disabled for the site, please enable OCR before proceeding with OCR backfilling. Refer to this [article](/en-us/microsoft-365/syntex/ocr) for instructions on enabling OCR on the selected site.

## EXAMPLES

### EXAMPLE 1

```powershell

Start-SPOSiteOpticalCharacterRecognitionBackfill -Site https://contosoenergy.sharepoint.com/sites/hr
```

Starts OCR process for all content that hasn't been processed before in the selected site.

## PARAMETERS

### -Site

Specifies the site URL where OCR process should be enabled on.

```yaml
Type: SpoSitePipeBind
Parameter Sets: Default
Aliases:
Applicable: SharePoint Online

Required: True
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Overview of optical character recognition in SharePoint](/en-us/microsoft-365/syntex/ocr-overview)

[Learn about optical character recognition in Microsoft Purview](/en-us/purview/ocr-learn-about?tabs=purview)
