---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spappsitesubscriptionname
applicable: SharePoint Server Subscription Edition
title: Set-SPAppSiteSubscriptionName
schema: 2.0.0
---

# Set-SPAppSiteSubscriptionName

## SYNOPSIS
Sets or changes the name for the specified site subscription.

## SYNTAX

```
Set-SPAppSiteSubscriptionName -Name <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-Force] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the `Set-SPAppSiteSubscriptionName` cmdlet to set or change the name for a specified site subscription by using the Name parameter.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Set-SPAppSiteSubscriptionName -Name Contoso
```

This example sets the name of the default site subscription to "Contoso".

### EXAMPLE 2
```powershell
Set-SPAppSiteSubscriptionName -Name Contoso -SiteSubscription https://www.contoso.com
```

This example changes the name of the site subscription for SPSite from https://www.contoso.com to "Contoso".

## PARAMETERS

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the name for the site subscription.

Each site subscription must have a unique name.
The name is used in part to determine the domain that apps for SharePoint are installed in for each site subscription.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### -Force

> Applicable: SharePoint Server Subscription Edition

The site subscription name is recorded in other databases in the SharePoint farm.
In cases such as disaster recovery or restore of the SharePoint farm, the Force parameter can be specified to ensure that the site subscription name has been propagated appropriately throughout the SharePoint farm.

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

### -SiteSubscription

> Applicable: SharePoint Server Subscription Edition

Specifies the SPSiteSubscription object or the SPSiteSubscription Id or the URL of an SPSite.
If this parameter is not specified, then the default site subscription is used.
All SharePoint SPSites are members of the default site subscription if they have not been specifically assigned a site subscription.

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

[Get-SPAppSiteSubscriptionName](Get-SPAppSiteSubscriptionName.md)
