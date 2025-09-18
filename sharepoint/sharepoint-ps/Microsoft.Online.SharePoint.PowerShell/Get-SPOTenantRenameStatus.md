---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/get-spotenantrenamestatus
applicable: SharePoint Online
title: Get-SPOTenantRenameStatus
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Get-SPOTenantRenameStatus

## SYNOPSIS

> [!IMPORTANT]
> This feature is currently available to organizations that have no more than 10,000 total SharePoint sites and OneDrive accounts combined.

Get the status of the job to change the SharePoint domain name for your organization in Microsoft 365.

## SYNTAX

```
Get-SPOTenantRenameStatus [<CommonParameters>]
```

## DESCRIPTION

This command gets the status of the job to rename the SharePoint domain name for your organization.

> [!NOTE]
> If you receive AccessDenied exceptions after the rename operation has started, try connecting to the new domain in PowerShell and try again.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantRenameStatus
```

Gets the status of the job to rename your SharePoint domain name.

## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Rename your SharePoint domain](https://aka.ms/SPOTenantRename)

[Start-SPOTenantRename](Start-SPOTenantRename.md)

[Stop-SPOTenantRename](Stop-SPOTenantRename.md)

[Get-SPOSiteRenameState](Get-SPOSiteRenameState.md)
