---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spocontenteventemailaddresses
applicable: SharePoint Online
title: Get-SPOContentEventEmailAddresses
schema: 1.0.0
author: mshabaz
ms.author: mshabaz
ms.reviewer:
manager: miabhish
---

# Get-SPOContentEventEmailAddresses

## SYNOPSIS

Retrieves email addresses associated with a specific content event category. If no category is specified by the user, email addresses for all categories of content events will be provided.

## SYNTAX

```
Get-SPOContentEventEmailAddresses [[-Category] <ContentEventCategory>] [<CommonParameters>]
```

## DESCRIPTION

Retrieves email addresses associated with a specific content event category. If no category is specified by the user, email addresses for all categories of content events will be provided.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOContentEventEmailAddresses -Category Ransomware
```

In Example 1, the system will display the email addresses categorized under ransomware that the admin had previously entered.

## PARAMETERS

### -Category

> Applicable: SharePoint Online

Specifies the content event category.

```yaml
Type: Microsoft.SharePoint.Administration.TenantAdmin.ContentEventCategory
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Ransomware, HighVolumeDownload, HighVolumeDelete, HighVolumeShare

Required: False
Position: 0
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

[Remove-SPOContentEventEmailAddresses](Remove-SPOContentEventEmailAddresses.md)

[Set-SPOContentEventEmailAddresses](Set-SPOContentEventEmailAddresses.md)
