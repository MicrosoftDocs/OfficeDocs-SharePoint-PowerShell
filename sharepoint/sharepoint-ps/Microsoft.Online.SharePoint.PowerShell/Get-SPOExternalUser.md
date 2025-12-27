---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/get-spoexternaluser
applicable: SharePoint Online
title: Get-SPOExternalUser
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Get-SPOExternalUser

## SYNOPSIS

Returns external users in the tenant.

## SYNTAX

```
Get-SPOExternalUser [[-Position] <Int32>] [[-PageSize] <Int32>] [[-Filter] <String>] [[-SortOrder] <SortOrder>]
 [[-SiteUrl] <String>] [-ShowOnlyUsersWithAcceptingAccountNotMatchInvitedAccount <Boolean>]
 [<CommonParameters>]
```

## DESCRIPTION

The `Get-SPOExternalUser` cmdlet returns external users that are located in the tenant based on specified criteria.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/).

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOExternalUser -Position 0 -PageSize 2
```

Example 1 returns the first two external users in the collection.

### EXAMPLE 2

```powershell
Get-SPOExternalUser -Position 2 -PageSize 2
```

Example 2 returns two external users from the third page of the collection.

### EXAMPLE 3

```powershell
Get-SPOExternalUser -Position 0 -PageSize 30 -SiteUrl https://contoso.sharepoint.com
```

Example 3 returns the first 30 users that match the SiteUrl <https://contoso.sharepoint.com>.

## PARAMETERS

### -Filter

> Applicable: SharePoint Online

Limits the results to only those users whose first name, last name, or email address begins with the text in the string using a case-insensitive comparison.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PageSize

> Applicable: SharePoint Online

Specifies the maximum number of users to be returned in the collection.

The value must be less than or equal to 50.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Position

> Applicable: SharePoint Online

Use to specify the zero-based index of the position in the sorted collection of the first result to be returned.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowOnlyUsersWithAcceptingAccountNotMatchInvitedAccount

> Applicable: SharePoint Online

Shows users who have accepted an invite but not using the account the invite was sent to.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteUrl

> Applicable: SharePoint Online

Specifies the site to retrieve external users for.

If no site is specified, the external users for all sites are returned.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SortOrder

> Applicable: SharePoint Online

Specifies the sort results in Ascending or Descending order on the SPOUser.Email property should occur.

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SortOrder
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Remove-SPOExternalUser](Remove-SPOExternalUser.md)
