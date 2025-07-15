---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spouser
applicable: SharePoint Online
title: Set-SPOUser
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Set-SPOUser

## SYNOPSIS

Configures properties on an existing user.

## SYNTAX

```
Set-SPOUser -Site <SpoSitePipeBind> -LoginName <String> [-IsSiteCollectionAdmin <Boolean>]
 [-UpdateUserTypeFromAzureAD] [<CommonParameters>]
```

## DESCRIPTION

Use the `Set-SPOUser` cmdlet to configure properties of an existing user.
That is, to add or remove a user as a SharePoint Online site collection administrator.

You must be at least a SharePoint administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

This cmdlet is not supported for use with granular delegated admin privileges (GDAP).

## EXAMPLES

### Example 1

```powershell
Set-SPOUser -Site https://contoso.sharepoint.com/sites/marketing -LoginName melissa.kerr@contoso.com -IsSiteCollectionAdmin $true
```

This example makes melissa.kerr@contoso.com a SharePoint Online site collection administrator on <https://contoso.sharepoint.com/sites/marketing>.

### Example 2

```powershell
Set-SPOUser -Site https://contoso.sharepoint.com/sites/benefits -LoginName adelev_fabrikam.onmicrosoft.com#ext#@contoso.onmicrosoft.com -IsSiteCollectionAdmin $true
```

This example makes guest user adelev_fabrikam.onmicrosoft.com a SharePoint Online site collection administrator on <https://contoso.sharepoint.com/sites/benefits>.

## PARAMETERS

### -IsSiteCollectionAdmin

Specifies whether the user is a site collection administrator.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoginName

Specifies the user name.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site

Specifies the full URL of the site collection. It must be in a valid managed path in the company's site.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateUserTypeFromAzureAD
If the UserType property of an existing user is changed in Microsoft Entra ID from Member to Guest or vice-versa, this parameter can be used to update it in SharePoint Online.
For more information, see [Convert UserType](/azure/active-directory/b2b/user-properties#convert-usertype).

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOUser](Get-SPOUser.md)
