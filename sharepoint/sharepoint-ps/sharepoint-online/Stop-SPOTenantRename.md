---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/stop-spotenantrename
applicable: SharePoint Online
title: Stop-SPOTenantRename
schema: 2.0.0
author: WayneEwington
ms.author: waynewin
ms.reviewer:
---

# Stop-SPOTenantRename

## SYNOPSIS

> [!IMPORTANT]
> This feature is currently available to organizations that have no more than 10,000 total SharePoint sites and OneDrive accounts combined.

Cancels the scheduled job to change the SharePoint domain name for your organization in Microsoft 365. 

> [!NOTE]
> If the job to change the SharePoint domain name is already in progress, then it cannot be canceled or stopped.

## SYNTAX

```Powershell
Stop-SPOTenantRename -Reason <string> [-Comment <string>] [<CommonParameters>]
```

## DESCRIPTION

This command cancels a scheduled rename of the SharePoint domain name for your organization.

## EXAMPLES

### EXAMPLE 1

```powershell
Stop-SPOTenantRename -Reason "Rescheduling"
```

Cancels the rename of the SharePoint domain name with the reason "Rescheduling".

## PARAMETERS

### -Reason

Specifies the reason why the job is being canceled.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment

Specifies an additional comment why the job is being canceled.

```yaml
Type: String
Parameter Sets: (All)
Applicable: SharePoint Online

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Rename your SharePoint domain](https://aka.ms/SPOTenantRename)

[Get-SPOTenantRenameStatus](Get-SPOTenantRenameStatus.md)

[Start-SPOTenantRename](Start-SPOTenantRename.md)

[Get-SPOSiteRenameState](Get-SPOSiteRenameState.md)
