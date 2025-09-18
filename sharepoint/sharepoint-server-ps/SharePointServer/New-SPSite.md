---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/new-spsite
applicable: SharePoint Server Subscription Edition
title: New-SPSite
schema: 2.0.0
---

# New-SPSite

## SYNOPSIS
Creates a new site collection at the specified URL.

## SYNTAX

```
New-SPSite [-Url] <String> -OwnerAlias <SPUserPipeBind> [-AdministrationSiteType <SPAdministrationSiteType>]
 [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <Int32>] [-Confirm]
 [-ContentDatabase <SPContentDatabasePipeBind>] [-Description <String>]
 [-HostHeaderWebApplication <SPWebApplicationPipeBind>] [-Language <UInt32>] [-Name <String>]
 [-OverrideCompatibilityRestriction] [-OwnerEmail <String>] [-QuotaTemplate <SPQuotaTemplatePipeBind>]
 [-SecondaryEmail <String>] [-SecondaryOwnerAlias <SPUserPipeBind>]
 [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-Template <SPWebTemplatePipeBind>] [-WhatIf]
 [-CreateFromSiteMaster] [<CommonParameters>]
```

## DESCRIPTION
The `New-SPSite` cmdlet creates a new site collection with the URL and owner that the Url and OwnerAlias parameters.
This cmdlet can create site collections in either the SharePoint Server mode which uses the legacy versions of templates and features, or can be created in SharePoint Server mode which uses the new versions of templates and features.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
New-SPSite https://webApp/sites/test -OwnerAlias "DOMAIN\JDoe" -Language 1033 -Template STS#0
```

This example creates an English site collection at https://\<site name\>/sites/test that is owned by user DOMAIN\Jdow.

### EXAMPLE 2
```powershell
$w = Get-SPWebApplication https://webApp
New-SPSite https://www.contoso.com -OwnerAlias "DOMAIN\jdow" -HostHeaderWebApplication $w -Name "Contoso" -Template STS#0
```

This example creates a host-named site collection.
Because the template is provided, the root web of this site collection will be created.

### EXAMPLE 3
```powershell
Get-SPWebTemplate | Where{ $_.Title -eq "Team Site" } | ForEach-Object{ New-SPSite https://<site name</sites/test -OwnerAlias DOMAIN\jdow -Template $_ }
```

This example creates a site collection by using the "Team Site" Web template.

### EXAMPLE 4
```powershell
New-SPSite -URL https://webApp/sites/testsite -OwnerAlias "DOMAIN\JDow" -Language 1033 -CompatibilityLevel 14 -Template STS#0
```

This example creates an English 14 mode site collection by using the Team site template at https://\<site name\>/sites/testsite that is owned by user DOMAIN\Jdow

## PARAMETERS

### -Url

> Applicable: SharePoint Server Subscription Edition

Specifies the URL that the new site collection uses.

If the URL is not a host header site, the URL must start with the web application URL.

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

### -OwnerAlias

> Applicable: SharePoint Server Subscription Edition

Specifies the user login name of the site owner.

The type must be a valid user alias, in the form, Domain\username.

```yaml
Type: SPUserPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministrationSiteType

> Applicable: SharePoint Server Subscription Edition

Specifies the site type.

Valid values are None or TentantAdministration.

```yaml
Type: SPAdministrationSiteType
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

### -CompatibilityLevel

> Applicable: SharePoint Server Subscription Edition

Specifies the version of templates to use when creating a new SPSite object.

This value sets the initial CompatibilityLevel value for the site collection.

When this parameter is not specified, the CompatibilityLevel will default to the highest possible version for the web application depending on the SiteCreationMode setting.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ContentDatabase

> Applicable: SharePoint Server Subscription Edition

Specifies the name or GUID of the content database in which to create the new site. If no content database is specified, the site collection is selected automatically.

The type must be a valid database name in the form, SiteContent1212, or a GUID in the form, 1234-5678-9807.

```yaml
Type: SPContentDatabasePipeBind
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

If no value is specified, the value is left blank.

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

### -HostHeaderWebApplication

> Applicable: SharePoint Server Subscription Edition

Specifies that if the URL provided is to be a host-named site collection, the HostHeaderWebApplication parameter must be the name, URL, GUID, or SPWebApplication object for the web application in which this site collection is created.

If no value is specified, the value is left blank.

The type must be a valid name in one of the following forms:

--A WebApplication

--A URL (for example, https://server_name)

--A GUID (for example, 1234-5678-9876-0987)

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Language

> Applicable: SharePoint Server Subscription Edition

Specifies the language ID for the new site collection.

If no language is specified, the site collection is created with the same language that was specified when the product was installed.

This must be a valid language identifier (LCID).

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

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the title of the new site collection.

If no name is specified, the default name is applied.

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

### -OverrideCompatibilityRestriction

> Applicable: SharePoint Server Subscription Edition

Specifies whether to use compatibility restriction for site.

The valid values are True or False.

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

### -OwnerEmail

> Applicable: SharePoint Server Subscription Edition

Specifies the email address of site owner.
If no value is specified, the value is left blank.

The type must be a email address in the form, someone@example.com.

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

### -QuotaTemplate

> Applicable: SharePoint Server Subscription Edition

Specifies the quota template for the new site.The template must exist already.

If no template is specified, no quota is applied.

```yaml
Type: SPQuotaTemplatePipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecondaryEmail

> Applicable: SharePoint Server Subscription Edition

Specifies the email address of the secondary site owner. If no value is specified, the value is left blank.

The type must be a email address, in the form, someone@example.com.

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

### -SecondaryOwnerAlias

> Applicable: SharePoint Server Subscription Edition

Specifies the user login credentials of the secondary site owner.

If no value is specified, the value is left blank.

The type must be a valid user alias, in the form, Domain\username.

```yaml
Type: SPUserPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSubscription

> Applicable: SharePoint Server Subscription Edition

Specifies the Site Group to get site collections.

```yaml
Type: SPSiteSubscriptionPipeBind
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

Specifies the Web template for the root web of the new site collection.

The template must be already installed.

If no template is specified, no template is provisioned.

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

### -CreateFromSiteMaster

> Applicable: SharePoint Server Subscription Edition

Specifies whether to create a new site using the Site Master.

The valid values are True or False.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
