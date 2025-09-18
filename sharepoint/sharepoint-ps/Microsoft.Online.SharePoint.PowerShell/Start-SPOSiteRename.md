---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/start-spositerename
applicable: SharePoint Online
title: Start-SPOSiteRename
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Start-SPOSiteRename

## SYNOPSIS

> [!NOTE]
> This Feature is part of the Admin Center Preview. If your tenant is not part of the Admin Center Preview, you will get an error when trying to run this cmdlet.

Starts a job to rename a site. You can change the URL, and optionally the site title along with changing the URL, of a site on a SharePoint Online collection.

## SYNTAX

```
Start-SPOSiteRename -Identity <SpoSitePipeBind> -NewSiteUrl <String> [-NewSiteTitle <String>]
 [-SuppressMarketplaceAppCheck] [-SuppressWorkflow2013Check] [-SuppressAllWarnings] [-SuppressBcsCheck]
 [-ValidationOnly] [-Reserved <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This command starts a rename of a site on a SharePoint Online site. You can change the URL, and optionally the site title along with changing the URL. Also allows you to simulate the run using the -WhatIf parameter as well as -SuppressWorkflow2013Check and SuppressMarketplaceAppCheck switch parameters.

## EXAMPLES

### EXAMPLE 1

```powershell
$url="https://<tenant>.sharepoint.com/sites/samplesite"
$NewSiteUrl="https://<tenant>.sharepoint.com/sites/renamed"
Start-SPOSiteRename -Identity $url -NewSiteUrl $NewSiteUrl
```

Starts the rename of the SPO site with name "samplesite" to "renamed" without modifying the title.

### EXAMPLE 2

```powershell
$url="https://<tenant>.sharepoint.com/sites/samplesite"
$NewSiteUrl="https://<tenant>.sharepoint.com/sites/renamed"
$newTitle="New Title"
Start-SPOSiteRename -Identity $url -NewSiteUrl $NewSiteUrl -NewSiteTitle $newTitle
```

Starts the rename of the SPO site with name "samplesite" to "renamed" modifying the title of the site to "New Title"

### EXAMPLE 3

```powershell
$url="https://<tenant>.sharepoint.com/sites/samplesite"
$NewSiteUrl="https://<tenant>.sharepoint.com/sites/renamed"
$newTitle="New Title"
Start-SPOSiteRename -Identity $url -NewSiteUrl $NewSiteUrl -NewSiteTitle $newTitle -SuppressMarketplaceAppCheck -SuppressWorkflow2013Check -WhatIf
```

Starts the **simulation** rename of the SPO site with name "samplesite" to "renamed" modifying the title of the site to "New Title" without MarketPlaceAppCheck and without WorkFlow2013Check

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the original URL of the site collection.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewSiteTitle

> Applicable: SharePoint Online

Specifies the new Title of the site.

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

### -NewSiteUrl

> Applicable: SharePoint Online

Specifies the new desired URL.

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

### -Reserved

> Applicable: SharePoint Online

Reserved for Microsoft internal use.

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

### -SuppressAllWarnings

> Applicable: SharePoint Online

Whether to suppress all warning messages.

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

### -SuppressBcsCheck

> Applicable: SharePoint Online

Whether to surpress checking whether tenant is using Business Connectivity Service (BCS) feature.

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

### -SuppressMarketplaceAppCheck

> Applicable: SharePoint Online

Suppress checking compatibility of marketplace SharePoint Add-ins deployed to the associated site.

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

### -SuppressWorkflow2013Check

> Applicable: SharePoint Online

Suppress checking compatibility of SharePoint 2013 Workflows deployed to the associated site.

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

### -ValidationOnly

> Applicable: SharePoint Online

Verifies that the site address can be changed.

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

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Online

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Start-SPOUserAndContentMove](Start-SPOUserAndContentMove.md)

[Stop-SPOUserAndContentMove](Stop-SPOUserAndContentMove.md)

[Get-SPOUserAndContentMoveState](Get-SPOUserAndContentMoveState.md)
