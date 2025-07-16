---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spweb
applicable: SharePoint Server Subscription Edition
title: New-SPWeb
schema: 2.0.0
---

# New-SPWeb

## SYNOPSIS
Creates a new site in an existing site collection.

## SYNTAX

```
New-SPWeb [-Url] <String> [-Language <UInt32>] [-Template <SPWebTemplatePipeBind>] [-Name <String>]
 [-Description <String>] [-AddToQuickLaunch] [-UniquePermissions] [-AddToTopNav] [-UseParentTopNav]
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The `New-SPWeb` cmdlet creates a new site in the existing site collection specified by the Url parameter.
You can create a site with a specific default language by specifying the Language parameter.
If no language is specified, the site is created with the same language that was specified when the product was installed.
You can create a site from a specific template by specifying the Template parameter.
If no template is specified, the site is created and the template can be provided later or by the first user to log on.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
New-SPWeb https://somesite/subweb1 -Template "STS#0"
```

This example creates a new subsite by using the Team Site template at the provided URL (https://somesite/subweb1).
The Team Site template is a value referenced as the variable STS#0 for the Template parameter.

## PARAMETERS

### -Url

> Applicable: SharePoint Server Subscription Edition

Specifies the URL where the new site is to be created.
The URL must be inside an existing site collection.
The URL must be a valid URL, in the form https://server_name/site1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Language

> Applicable: SharePoint Server Subscription Edition

Specifies the language template identifier for the new site.
If no language is specified, the site is created with the same language that was specified when the product was installed.

The type must be a valid language identifier (LCID).

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Template

> Applicable: SharePoint Server Subscription Edition

Specifies the Web template for the new site.
The template must already exist.
If no template is specified, no template is applied and a template can be selected later.

```yaml
Type: SPWebTemplatePipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the title of the new site.
If no title is specified, the default title is applied.
The default title is configured for each template.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

> Applicable: SharePoint Server Subscription Edition

Describes the new site.
If no description is specified, the entry is left blank.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddToQuickLaunch

> Applicable: SharePoint Server Subscription Edition

Adds this site to the Quick Launch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UniquePermissions

> Applicable: SharePoint Server Subscription Edition

Specifies that this site is to be created with unique permissions.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddToTopNav

> Applicable: SharePoint Server Subscription Edition

Adds this site to the top-level navigation bar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseParentTopNav

> Applicable: SharePoint Server Subscription Edition

Specifies that the same top-level navigation bar as the parent site is to be used for this site.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the `Stop-SPAssignment` command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server Subscription Edition

Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
