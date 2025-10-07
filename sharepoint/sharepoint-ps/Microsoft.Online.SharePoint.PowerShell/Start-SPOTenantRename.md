---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/start-spotenantrename
applicable: SharePoint Online
title: Start-SPOTenantRename
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Start-SPOTenantRename

## SYNOPSIS

> [!IMPORTANT]
> This feature is currently available to organizations that have no more than 10,000 total SharePoint sites and OneDrive accounts combined.  Additionally, tenant renaming capability is not available for GCC, GCC High, and DoD.

Starts a job to change the SharePoint domain name for your organization in Microsoft 365. For example, if the name of your organization changes from "Contoso" to "Fabrikam," you can change contoso.sharepoint.com to fabrikam.sharepoint.com.

> [!WARNING]
> Changing your SharePoint domain name might take several hours to days depending on the number of sites and OneDrive users that you have. We strongly recommend that you make this change during a period of low usage (like a weekend) and tell users to avoid accessing SharePoint and OneDrive content during the change. In addition, any actions that create new OneDrives and sites (such as creating a new team or private channel in Microsoft Teams) will be temporarily blocked during the rename.

## SYNTAX

```
Start-SPOTenantRename -DomainName <String> -ScheduledDateTime <DateTime> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

This command schedules a rename of the SharePoint domain name for your organization.

## EXAMPLES

### EXAMPLE 1

```powershell
Start-SPOTenantRename -DomainName "fabrikam" -ScheduledDateTime "2021-12-31T10:25:00"
```

Starts the rename of the SharePoint domain name to Fabrikam which is scheduled for December 31, 2021, at 10:25:00 am.

## PARAMETERS

### -DomainName

> Applicable: SharePoint Online

Specifies the domain name that the current SharePoint domain name will be renamed to. This is the part before "sharepoint.com" or "onmicrosoft.com".

> [!NOTE]
> The domain name must already have been successfully added to Microsoft Entra ID as per the instructions at [Step 1: Add the new domain name](https://aka.ms/SPOTenantRename#step-1-add-the-new-domain-name). If the domain name does not exist or was not successfully added, then this cmdlet will return an error.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScheduledDateTime

> Applicable: SharePoint Online

Specifies the date-time that the job will be started. This should be at least 24 hours in the future, but no more than 30 days.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Online
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

> Applicable: SharePoint Online
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

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Rename your SharePoint domain](https://aka.ms/SPOTenantRename)

[Get-SPOTenantRenameStatus](Get-SPOTenantRenameStatus.md)

[Stop-SPOTenantRename](Stop-SPOTenantRename.md)

[Get-SPOSiteRenameState](Get-SPOSiteRenameState.md)
