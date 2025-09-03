---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spositeoffice365group
applicable: SharePoint Online
title: Set-SPOSiteOffice365Group
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Set-SPOSiteOffice365Group

## SYNOPSIS

Connects a top-level SPO site collection to a new Microsoft 365 Group.

## SYNTAX

```
Set-SPOSiteOffice365Group [-Site] <SpoSitePipeBind> [-DisplayName] <String> [-Alias] <String> [-IsPublic]
 [[-Description] <String>] [[-Classification] <String>] [-KeepOldHomepage] [<CommonParameters>]
```

## DESCRIPTION

Connects a top-level SPO site collection to a new Microsoft 365 Group. You must be at least a SharePoint Online administrator to run the cmdlet and be a site collection administrator of the site.

If the site doesn't exist, this cmdlet returns a "File not found" error.

## EXAMPLES

### Example 1

This example creates a new Microsoft 365 Group named "site1group" and connects site collection <https://contoso.sharepoint.com/sites/site1> to it.  The group will have its privacy set to "Private" and Classification set to "Highly Confidential".

```powershell
Set-SPOSiteOffice365Group -Site https://contoso.sharepoint.com/sites/site1 -DisplayName "site1group" -Alias "site1group" -Classification "Highly Confidential"
```

### Example 2

This example creates a new Office 365 Group named "classicsite" and connects site collection <https://contoso.sharepoint.com/sites/classicsite> to it. It will keep the old home page from the classic site.

```powershell
Set-SPOSiteOffice365Group -Site https://contoso.sharepoint.com/sites/classicsite -DisplayName "Classic Site" -Alias "classicsite" -KeepOldHomepage
```

## PARAMETERS

### -Alias

> Applicable: SharePoint Online

Specifies the email alias for the new Microsoft 365 Group that will be created.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Classification

> Applicable: SharePoint Online

Specifies the classification value, if classifications are set for the organization. If no value is provided, the default classification will be set, if one is configured.

See [Microsoft Entra cmdlets for configuring group settings](https://go.microsoft.com/fwlink/?LinkID=827484) and follow the steps in the Create settings at the directory level to define the classification for Office 365 groups.

See [Manage Office 365 Groups with PowerShell](https://support.office.com/en-us/article/Manage-Office-365-Groups-with-PowerShell-aeb669aa-1770-4537-9de2-a82ac11b0540) for more information.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

> Applicable: SharePoint Online

Specifies the group's description.

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

### -DisplayName

> Applicable: SharePoint Online

Specifies the name of the new Microsoft 365 Group that will be created.

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

### -IsPublic

> Applicable: SharePoint Online

Determines the Microsoft 365 Group's privacy setting.  If switch is included, the group will be public, otherwise it will be private.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeepOldHomepage

> Applicable: SharePoint Online

For sites that already have a modern page set as homepage, you can specify whether you want to keep it as the homepage.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site

The site collection being connected to new Office 365 Group.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
