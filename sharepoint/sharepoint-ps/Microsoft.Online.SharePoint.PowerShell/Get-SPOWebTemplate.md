---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spowebtemplate
applicable: SharePoint Online
title: Get-SPOWebTemplate
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOWebTemplate

## SYNOPSIS

Displays all site templates that match the given identity.

## SYNTAX

```
Get-SPOWebTemplate [[-LocaleId] <UInt32>] [-CompatibilityLevel <Int32>] [-Name <String>] [-Title <String>]
 [<CommonParameters>]
```

## DESCRIPTION

The `Get-SPOWebTemplate` cmdlet displays all site templates that match the given identity and are available in SharePoint Online.

You must be at least a SharePoint Online administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOWebTemplate
```

Example 1 returns all the site templates in the language of the administrator site.

### EXAMPLE 2

```powershell
Get-SPOWebTemplate -LocaleID 1036
```

Example 2 returns a list of all the French site templates.

## PARAMETERS

### -CompatibilityLevel

> Applicable: SharePoint Online

Specifies the compatibility level of the site template.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:


Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocaleId

> Applicable: SharePoint Online

Specifies the Locale ID of the site template.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:


Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Online

Specifies the name of the site template.

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

### -Title

> Applicable: SharePoint Online

Specifies the Locale ID of the site template.

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
