---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/update-usertype
applicable: SharePoint Online
title: Update-UserType
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Update-UserType

## SYNOPSIS

Updates the specified user's UserType value from Microsoft Entra ID.

## SYNTAX

```
Update-UserType [-LoginName] <String> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet retrieves the UserType value of the specified user and updates the UserType across all SharePoint Online sites in the Office 365 tenant. This can be used, for example, to convert a Guest user to a standard (Member) user if the user's UserType was previously updated in Microsoft Entra ID.

## EXAMPLES

### Example 1

```powershell
Update-UserType -LoginName jdoe@contoso.com
```

Updates the jdoe@contoso.com's UserType on all SharePoint Online sites in the tenant based on the UserType value in Microsoft Entra ID.

## PARAMETERS

### -LoginName

> Applicable: SharePoint Online

The login name of the target user to update across SharePoint Online.

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

[Properties of a Microsoft Entra B2B collaboration user](/azure/active-directory/b2b/user-properties)
