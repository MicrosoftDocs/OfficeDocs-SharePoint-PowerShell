---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spocontenteventemailaddresses
applicable: SharePoint Online
title: Remove-SPOContentEventEmailAddresses
schema: 1.0.0
author: mshabaz
ms.author: mshabaz
ms.reviewer:
manager: miabhish
---

# Remove-SPOContentEventEmailAddresses

## SYNOPSIS

Removes the email addresses associated with the specified category of content event if they exist. Consequently, notification emails will no longer be sent to these addresses.

## SYNTAX

```powershell
Remove-SPOContentEventEmailAddresses [-Category] <ContentEventCategory> [-EmailAddresses] <string[]>
```

## DESCRIPTION

Removes the email addresses associated with the specified category of content event if they exist.

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOContentEventEmailAddresses -Category Ransomware -EmailAddresses "Joe.Doe@contoso.com", "John.Dow@contoso.com"
```

In Example 1, the email addresses joe.doe@contoso.com and john.dow@contoso.com have been excluded from the ransomware category within the content event. As a result, notification emails will not be dispatched to these two addresses.

## PARAMETERS

### -Category

Specifies the content event category.

```yaml
Type: ContentEventCategory
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailAddresses

List of comma seperated email addresses

```yaml
Type: strings
Parameter Sets: (All)

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters


## RELATED LINKS

[Get-SPOContentEventEmailAddresses](Get-SPOContentEventEmailAddresses.md)

[Set-SPOContentEventEmailAddresses](Set-SPOContentEventEmailAddresses.md)