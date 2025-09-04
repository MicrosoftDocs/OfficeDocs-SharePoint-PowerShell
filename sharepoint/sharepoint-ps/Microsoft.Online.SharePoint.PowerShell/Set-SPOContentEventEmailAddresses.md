---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spocontenteventemailaddresses
applicable: SharePoint Online
title: Set-SPOContentEventEmailAddresses
schema: 1.0.0
author: mshabaz
ms.author: mshabaz
ms.reviewer:
manager: miabhish
---

# Set-SPOContentEventEmailAddresses

## SYNOPSIS

Adds the email addresses to the specified category of content event. Consequently, notification emails will be sent to these addresses.

## SYNTAX

```
Set-SPOContentEventEmailAddresses [-Category] <ContentEventCategory> [-EmailAddresses] <String[]>
 [<CommonParameters>]
```

## DESCRIPTION

Adds the email addresses to specified category of content event.

## EXAMPLES

### EXAMPLE 1

```powershell
Set-SPOContentEventEmailAddresses -Category Ransomware -EmailAddresses "Joe.Doe@contoso.com", "John.Dow@contoso.com"
```

In Example 1, the email addresses joe.doe@contoso.com and john.dow@contoso.com has been added to the ransomware category within the content event. As a result, notification emails of ransomware events will be dispatched to these two addresses.

## PARAMETERS

### -Category

> Applicable: SharePoint Online

Specifies the content event category.

```yaml
Type: Microsoft.SharePoint.Administration.TenantAdmin.ContentEventCategory
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Ransomware, HighVolumeDownload, HighVolumeDelete, HighVolumeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailAddresses

List of comma seperated email addresses

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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

[Get-SPOContentEventEmailAddresses](Get-SPOContentEventEmailAddresses.md)

[Remove-SPOContentEventEmailAddresses](Remove-SPOContentEventEmailAddresses.md)
