---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spositeversionpolicyjob
applicable: SharePoint Online
title: Remove-SPOSiteVersionPolicyJob
schema: 2.0.0
author: msjennywu
ms.author: jennywu
ms.reviewer:
manager: seanmc
---

# Remove-SPOSiteVersionPolicyJob

## SYNOPSIS

Cancels further processing of version settings update on existing document libraries on the site collection.

## SYNTAX
```powershell
Remove-SPOSiteVersionPolicyJob [-Identity] <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION

`Set-SPOSite` cmdlet using `ApplyToExistingDocumentLibraries` will create a job to set version policy for existing document libraries on the site collection. This cmdlet removes the job, which stops updating the new version policy on existing libraries. The version policy already applied on existing libraries will not be reverted.

## EXAMPLES

### Example 1

```powershell
Remove-SPOSiteVersionPolicyJob -Identity https://contoso.sharepoint.com/sites/site1
```

Example 1 cancels further processing of the job that sets version policy for existing document libraries on the site collection.

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

[Get-SPOSiteVersionPolicyJobProgress](Get-SPOSiteVersionPolicyJobProgress.md)
