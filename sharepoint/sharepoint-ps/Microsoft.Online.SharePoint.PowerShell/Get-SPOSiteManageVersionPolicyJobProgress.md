---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spositemanageversionpolicyjobprogress
applicable: SharePoint Online
title: Get-SPOSiteManageVersionPolicyJobProgress
schema: 2.0.0
author: blarrywangmsft
ms.author: blarrywang
ms.reviewer:
---

# Get-SPOSiteManageVersionPolicyJobProgress

## SYNOPSIS
Gets the status and progress for a background job started by `New-SPOSiteManageVersionPolicyJob`.
> [!NOTE]
> This feature is currently in preview and may not be available in your tenant.

## SYNTAX

```
Get-SPOSiteManageVersionPolicyJobProgress [-Identity] <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION
Gets the status and progress for a background job started by `New-SPOSiteManageVersionPolicyJob`.

## EXAMPLES

### Example 1

```
Get-SPOSiteManageVersionPolicyJobProgress https://contoso.sharepoint.com/sites/site1
```

Gets the progress of the site manage version policy job for the given site.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the URL of the site collection.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-SPOSiteManageVersionPolicyJob](New-SPOSiteManageVersionPolicyJob.md)

[Remove-SPOSiteManageVersionPolicyJob](Remove-SPOSiteManageVersionPolicyJob.md)
