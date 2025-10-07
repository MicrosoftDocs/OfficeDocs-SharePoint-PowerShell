---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/get-spsiteupgradesessioninfo
applicable: SharePoint Server Subscription Edition
title: Get-SPSiteUpgradeSessionInfo
schema: 2.0.0
---

# Get-SPSiteUpgradeSessionInfo

## SYNOPSIS

Manage or report site upgrade.


## SYNTAX

### ContentDB
```
Get-SPSiteUpgradeSessionInfo -ContentDatabase <SPContentDatabasePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-HideWaiting] [-ShowCompleted] [-ShowFailed]
 [-ShowInProgress] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [<CommonParameters>]
```

### Site
```
Get-SPSiteUpgradeSessionInfo -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

Use the Get-SPSiteUpgradeSessionInfo cmdlet to manage or report site upgrade of the farm.

This cmdlet has two modes, get upgrade information for a specific SPSite object or for a given content database.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
$db = Get-SPContentDatabase -Identity wss_content
Get-SPSiteUpgradeSessionInfo -ContentDatabase $db
```

This example returns siteupgradeinfo for every SPContentDatabase returned from Get-SPContentDatabase cmdlet.

### EXAMPLE 2
```powershell
$site=Get-SPSite -Identity https://localhost
Get-SPSiteUpgradeSessionInfo -Site $site
```

This example returns siteupgradeinfo for every SPSite object returned from Get-SPSite cmdlet.

## PARAMETERS

### -ContentDatabase

> Applicable: SharePoint Server Subscription Edition

Specifies the GUID of the content database from which to list site collections.The type must be a valid database name, in the form  SPContentDB01, or a valid GUID (for example, 12345678-90ab-cdef-1234-567890bcdefgh).

```yaml
Type: SPContentDatabasePipeBind
Parameter Sets: ContentDB
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Site

> Applicable: SharePoint Server Subscription Edition

```yaml
Type: SPSitePipeBind
Parameter Sets: Site
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
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -HideWaiting

> Applicable: SharePoint Server Subscription Edition

Specifies to hide site collections that upgrade has not started.

```yaml
Type: SwitchParameter
Parameter Sets: ContentDB
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowCompleted

> Applicable: SharePoint Server Subscription Edition

Specifies to show site collections that has completed upgrade.

```yaml
Type: SwitchParameter
Parameter Sets: ContentDB
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowFailed

> Applicable: SharePoint Server Subscription Edition

Specifies to show site collections that have failed upgrade.

```yaml
Type: SwitchParameter
Parameter Sets: ContentDB
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowInProgress

> Applicable: SharePoint Server Subscription Edition

Displays site collections that are in the process of being upgraded.

```yaml
Type: SwitchParameter
Parameter Sets: ContentDB
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSubscription

> Applicable: SharePoint Server Subscription Edition

Specifies to limit the result to site collections within the site subscription.

```yaml
Type: SPSiteSubscriptionPipeBind
Parameter Sets: ContentDB
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

[Remove-SPSiteUpgradeSessionInfo](Remove-SPSiteUpgradeSessionInfo.md)
