---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spomigrationjobstatus
applicable: SharePoint Online
title: Get-SPOMigrationJobStatus
schema: 2.0.0
author: trent-green
ms.author: speedta
ms.reviewer:
---

# Get-SPOMigrationJobStatus

## SYNOPSIS

**Note**: This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).

Use this cmdlet to monitor the status of a submitted SharePoint Online migration job.

## SYNTAX

```
Get-SPOMigrationJobStatus -TargetWebUrl <String> [-JobId <Guid>] -Credentials <CredentialCmdletPipeBind>
 [-NoLogFile] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet will check the status of a migration job.

## EXAMPLES

### EXAMPLE 1

```powershell
$targetWebUrl = "https://contoso.sharepoint.com/sites/migrationtest"
$credentials = Get-Credential
Get-SPOMigrationJobStatus -TargetWebUrl $targetWebUrl -Credentials $credentials -JobId "779c4b3b-ec24-4705-bb58-c38f4329418c"
```

Get the status of your SPO Migration Job.
You can obtain the Job id when submit package data to create new SPO migration job via the Invoke-SPOMigrationEncryptUploadSubmit cmdlet

## PARAMETERS

### -Credentials

> Applicable: SharePoint Online

The credentials of a site collection administrator to use to connect to the site collection. The credentials should supply the username in UPN format (e.g. user@company.onmicrosoft.com). If this property is not set, the current tenant admin credentials from the session's previous call to `Connect-SPOService` will be used to connect to the site collection.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.CredentialCmdletPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId

> Applicable: SharePoint Online

(optional) The ID of a migration job that exists on the target site collection.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoLogFile

> Applicable: SharePoint Online

(optional) Indicates to not create a log file. The default is to create a new DeleteMigrationJob log file within the current directory.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetWebUrl

> Applicable: SharePoint Online

The fully qualified target web URL where the package will be imported. This must include the same TargetWebUrl that was used during `ConvertTo-SPOMigrationTargetedPackage`.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

