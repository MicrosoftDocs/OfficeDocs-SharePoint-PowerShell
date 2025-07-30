---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spouserprofile
applicable: SharePoint Online
title: Remove-SPOUserProfile
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
ms.custom: has-azure-ad-ps-ref
---

# Remove-SPOUserProfile

## SYNOPSIS

Remove user profile from the tenant.

## SYNTAX

```
Remove-SPOUserProfile -LoginName <String> [-UserId <String>] [<CommonParameters>]
```

## DESCRIPTION

Can be used to remove the SharePoint user profile from the tenant.

> [!NOTE]
> The User must be first be deleted from Microsoft Entra ID before the user profile can be deleted. You can use the Microsoft Entra cmdlet Remove-AzureADUser for this action

## EXAMPLES

### Example 1

```powershell
Remove-SPOUserProfile -LoginName joe.healy@contoso.com
```

Example 1 removes a user who has the e-mail address joe.healy@contoso.com from the SharePoint Online User Profiles of the particular tenant.

## PARAMETERS

### -LoginName

> Applicable: SharePoint Online

Specifies the login name of the user profile to be deleted.

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

### -UserId

> Applicable: SharePoint Online

Specifies the ID of the user profile to be deleted.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

[Remove-SPOUserInfo](Remove-SPOUserInfo.md)
