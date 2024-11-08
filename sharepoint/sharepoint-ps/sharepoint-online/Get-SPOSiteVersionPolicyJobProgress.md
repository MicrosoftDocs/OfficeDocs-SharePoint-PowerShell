---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositeversionpolicyjobprogress
applicable: SharePoint Online
title: Get-SPOSiteVersionPolicyJobProgress
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Get-SPOSiteVersionPolicyJobProgress

## SYNOPSIS

Gets the progress of setting version policy for existing document libraries on the site collection.

## SYNTAX
```powershell
Get-SPOSiteVersionPolicyJobProgress [-Identity] <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

`Set-SPOSite` cmdlet using `ApplyToExistingDocumentLibraries` will create a job to set version policy for existing document libraries on the site collection. This cmdlet then gets the progress of the job.

## EXAMPLES

### Example 1

```powershell
Get-SPOSiteVersionPolicyJobProgress -Identity https://contoso.sharepoint.com/sites/site1
```

Example 1 gets the progress of setting version policy for existing document libraries on the site collection.

## PARAMETERS

### -Identity

Specifies the URL of the site collection.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Set-SPOSite](Set-SPOSite.md)
