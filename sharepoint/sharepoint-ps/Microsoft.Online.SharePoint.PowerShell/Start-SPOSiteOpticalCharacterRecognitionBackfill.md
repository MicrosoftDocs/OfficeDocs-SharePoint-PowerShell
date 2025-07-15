---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
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
> Optical Character Recognition (OCR) is a pay-as-you-go feature. Running this cmdlet will incur cost for your organization.

Initiates a job to trigger the OCR process for all files for the selected site.

## SYNTAX

```
Start-SPOSiteOpticalCharacterRecognitionBackfill -Site <SpoSitePipeBind> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet starts a job to trigger the OCR process for files that have either never been OCR processed or have been modified since the last OCR process. This ensures all relevant content in the site is recognized and indexed for improved searchability and accessibility.

OCR backfill can only be run on OCR-enabled sites. If OCR is disabled for the site, please enable OCR before proceeding with OCR backfilling. Refer to this [article](/microsoft-365/syntex/ocr) for instructions on enabling OCR on the selected site.

> [!Note]
> Backfilling cancellation is currently under development. Once the cmdlet is triggered, the backfilling process cannot be stopped. Disabling OCR on the selected site will not cancel the ongoing backfilling session.

## EXAMPLES

### EXAMPLE 1

```powershell

Start-SPOSiteOpticalCharacterRecognitionBackfill -Site https://contosoenergy.sharepoint.com/sites/hr
```

Starts OCR process for all content that hasn't been processed before in the selected site.

## PARAMETERS

### -Site

> Applicable: SharePoint Online

Specifies the site where OCR process should be enabled on.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:


Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Overview of optical character recognition in SharePoint](/microsoft-365/syntex/ocr-overview)

[Learn about optical character recognition in Microsoft Purview](/purview/ocr-learn-about?tabs=purview)
