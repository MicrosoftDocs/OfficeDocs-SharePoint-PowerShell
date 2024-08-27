---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontenteventemailaddresses
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

```powershell
Get-SPOContentEventEmailAddresses [-Category] <ContentEventCategory>
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

Specifies the content event category.

```yaml
Type: ContentEventCategory
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters


## RELATED LINKS

[Remove-SPOContentEventEmailAddresses](Remove-SPOContentEventEmailAddresses.md)

[Set-SPOContentEventEmailAddresses](Set-SPOContentEventEmailAddresses.md)