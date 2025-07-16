---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/new-sposite
applicable: SharePoint Online
title: New-SPOSite
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# New-SPOSite

## SYNOPSIS

Creates a new SharePoint Online site collection for the current company.

## SYNTAX

```
New-SPOSite -Url <UrlCmdletPipeBind> -Owner <String> -StorageQuota <Int64> [-Title <String>]
 [-Template <String>] [-LocaleId <UInt32>] [-CompatibilityLevel <Int32>] [-ResourceQuota <Double>]
 [-TimeZoneId <Int32>] [-NoWait] [-EnableAgreementsSolution] [<CommonParameters>]
```

## DESCRIPTION

The `New-SPOSite` cmdlet creates a new site collection for the current company.
However, creating a new SharePoint Online site collection fails if a deleted site with the same URL exists in the Recycle Bin.

You must be at least a SharePoint Online administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at <https://go.microsoft.com/fwlink/p/?LinkId=251832>.

## EXAMPLES

### EXAMPLE 1

```powershell
New-SPOSite -Url https://contoso.sharepoint.com/sites/mynewsite -Owner joe.healy@contoso.com -StorageQuota 1000 -Title "My new site collection"
```

Example 1 creates a new site collection for the current company with specified site URL, title and owner. The storage quota is set to 1000 megabytes.

### EXAMPLE 2

```powershell
New-SPOSite -Url https://contoso.sharepoint.com/sites/mynewsite -Owner joe.healy@contoso.com -StorageQuota 1000 -CompatibilityLevel 15 -LocaleID 1033 -ResourceQuota 300 -Template "STS#0" -TimeZoneId 13 -Title "My new site collection"
```

Example 2 creates a new site collection for the current company with specified site URL, title, owner and template. The storage quota is set to 1000 megabytes and the resource quota is set to 300 megabytes. The template compatibility level is set to 15 which means that the site collection only supports the SharePoint 2013 template. The language is set to English - United States (LocaleID = 1033) and the time zone is set to (GMT-08:00) Pacific Time (US and Canada) (TimeZone = 13).

### EXAMPLE 3

```powershell
New-SPOSite -Url https://contoso.sharepoint.com/sites/accounting -Owner admin@contoso.com -StorageQuota 100 -NoWait -ResourceQuota 50 -Template STS#0
```

Example 3 creates a new site collection for the current company with specified site URL, owner and template. The storage quota is set to 100 megabytes and the resource quota is set to 50 megabytes. This cmdlet is executed immediately without delay.

## PARAMETERS

### -CompatibilityLevel

> Applicable: SharePoint Online

This parameter no longer has any effect and only accepts a value of '15'.

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

### -EnableAgreementsSolution
{{ Fill EnableAgreementsSolution Description }}

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

### -LocaleId

> Applicable: SharePoint Online

Specifies the language of this site collection. For more information, see Locale IDs Assigned by Microsoft (<https://go.microsoft.com/fwlink/p/?LinkId=242911>). The Template and LocaleId parameters must be a valid combination as returned from the `Get-SPOWebTemplate` cmdlet.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait

> Applicable: SharePoint Online

Specifies to continue executing script immediately.

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

### -Owner

> Applicable: SharePoint Online

Specifies the user name of the site collection's primary owner. The owner must be a email-enabled user instead of a security group or an email-enabled security group.

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

### -ResourceQuota

> Applicable: SharePoint Online

Specifies the quota for this site collection in Sandboxed Solutions units. This value must not exceed the company's aggregate available Sandboxed Solutions quota. The default value is 0. For more information, see [Resource Usage Limits on Sandboxed Solutions in SharePoint](/previous-versions/office/developer/sharepoint-2010/gg615462(v=office.14)). Note that this parameter is now obsolete and has been deprecated.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuota

> Applicable: SharePoint Online

Specifies the storage quota for this site collection in megabytes. This value must not exceed the company's available quota.

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Template

> Applicable: SharePoint Online

Specifies the site collection template type. Use the `Get-SPOWebTemplate` cmdlet to get the list of valid templates. If no template is specified, one can be added later. The Template and LocaleId parameters must be a valid combination as returned from the `Get-SPOWebTemplate` cmdlet.

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

### -TimeZoneId

> Applicable: SharePoint Online

Specifies the time zone of the site collection. For more information, see [RegionalSettings.TimeZones property](/previous-versions/office/sharepoint-csom/jj171282(v=office.15)).

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

### -Title

> Applicable: SharePoint Online

Specifies the title of the site collection.

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

### -Url

> Applicable: SharePoint Online

Specifies the full URL of the new site collection. It must be in a valid managed path in the company's site. For example, for company contoso, valid managed paths are <https://contoso.sharepoint.com/sites> and <https://contoso.sharepoint.com/teams.>

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.UrlCmdletPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOSite](Get-SPOSite.md)

[Set-SPOSite](Set-SPOSite.md)
