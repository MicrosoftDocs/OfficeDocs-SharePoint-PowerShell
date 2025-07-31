---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spohomesite
applicable: SharePoint Online
title: Set-SPOHomeSite
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Set-SPOHomeSite

## SYNOPSIS

Sets a SharePoint Site as a Home Site.

## SYNTAX

```
Set-SPOHomeSite -HomeSiteUrl <String> [-VivaConnectionsDefaultStart <Boolean>] [-Force] [-DraftMode <Boolean>]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to set a SharePoint Site as a Home Site. A home site is a communication site that you create and set as the top landing page for all users in your intranet. For more information, see [Set up a home site for your organization](/SharePoint/home-site)

## EXAMPLES

### Example 1

```powershell
Set-SPOHomeSite -HomeSiteUrl "https://contoso.sharepoint.com/sites/homesite"
This example set the site collection at *<https://contoso.sharepoint.com/sites/homesite>* as SharePoint Online Home Site.
```

### Example 2

```powershell
Set-SPOHomeSite -HomeSiteUrl "https://contoso.sharepoint.com/sites/homesite" -VivaConnectionsDefaultStart:$true
Sets the home site to the provided site collection url and keeps the Viva Connections landing experience to the SharePoint home site.
```

## PARAMETERS

### -DraftMode

> Applicable: SharePoint Online

Whether to set the home site to draft mode.

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

### -Force

> Applicable: SharePoint Online

Whether to set the home site without prompting for confirmation.

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

### -HomeSiteUrl

Sets the URL of the site collection to be the home site.

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

### -VivaConnectionsDefaultStart

When set to $true, the VivaConnectionsDefaultStart parameter will keep the Viva Connections landing experience to the SharePoint home site for the desktop experience. If set to $false, the Viva Connections home experience will be used. This command doesn't impact the mobile experience.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
