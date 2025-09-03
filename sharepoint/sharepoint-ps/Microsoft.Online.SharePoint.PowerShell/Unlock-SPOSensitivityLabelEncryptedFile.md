---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Unlock-SPOSensitivityLabelEncryptedFile
applicable: SharePoint Online
title: Unlock-SPOSensitivityLabelEncryptedFile
schema: 2.0.0
author: SanjoyanM
ms.author: samust
ms.reviewer:
ms.date: 07/16/2025
---

# Unlock-SPOSensitivityLabelEncryptedFile

## SYNOPSIS

It removes encryption on a Sensitivity label encrypted file in SharePoint Online. No need to download the file.

## SYNTAX

```
Unlock-SPOSensitivityLabelEncryptedFile [-FileUrl] <String> [-JustificationText] <String> [<CommonParameters>]
```

## DESCRIPTION

The `Unlock-SPOSensitivityLabelEncryptedFile` cmdlet runs on a single office online file that is encrypted via sensitivity label. It decrypts the file and removes the label from the file.

You must be at least a SharePoint Online administrator to run the `Unlock-SPOSensitivityLabelEncryptedFile` cmdlet. This cmdlet doesn't work on files that have double key encryption or files that have encryption but are not processed by SharePoint. These files don't show the name of the label in the Sensitivity column, and you can't edit these files in Office Online.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
 Unlock-SPOSensitivityLabelEncryptedFile -FileUrl "https://contoso.com/sites/Marketing/Shared Documents/Doc1.docx" -JustificationText "Need to recover this file"
```

This example will remove a regular label with admin defined encryption from the file Doc1.docx and also make an entry in audit logs.

## PARAMETERS

### -FileUrl

> Applicable: SharePoint Online

Full URL for the file.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JustificationText

> Applicable: SharePoint Online

Text that explains the reason to run this cmdlet on the given file.

```yaml
Type: System.String
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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)
