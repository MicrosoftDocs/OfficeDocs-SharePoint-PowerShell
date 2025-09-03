---
external help file: Microsoft.Office.Server.UserProfiles.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/add-spprofileleader
applicable: SharePoint Server Subscription Edition
title: Add-SPProfileLeader
schema: 2.0.0
ms.date: 08/26/2025
---

# Add-SPProfileLeader

## SYNOPSIS
Adds a company leader.

## SYNTAX

```
Add-SPProfileLeader [-ProfileServiceApplicationProxy] <SPServiceApplicationProxyPipeBind>
 [-Name] <SPProfileLeaderPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet was introduced in SharePoint Server 2010 Service Pack 1 (SP1).

Use the `Add-SPProfileLeader` cmdlet to add a user as the company leader in the User Profile Service Application.

For additional information about SPProfileLeader cmdlets, see the \*-SPProfileLeader Windows PowerShell cmdlets in SharePoint Server https://go.microsoft.com/fwlink/p/?LinkId=226295.

After you use the `Add-SPProfileLeader` cmdlet to add a company leader, you have to complete a full crawl of your content sources for the changes to take effect.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at https://go.microsoft.com/fwlink/p/?LinkId=251831.

## EXAMPLES

### EXAMPLE
```powershell
$upaProxy = Get-SPServiceApplicationProxy | where {$_.TypeName -eq 'User Profile Service Application Proxy'}
Add-SPProfileLeader -ProfileServiceApplicationProxy $upaProxy -Name "contoso\janedoe"
```

This example adds a company leader named Jane Doe.

## PARAMETERS

### -ProfileServiceApplicationProxy

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the User Profile Service Application Proxy to use.

```yaml
Type: SPServiceApplicationProxyPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the account name to be added as a leader for the new User Profile Service application.
For example, contoso\janedoe.

```yaml
Type: SPProfileLeaderPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
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

### -SiteSubscription

> Applicable: SharePoint Server Subscription Edition

Specifies the account under which this service should run.
This parameter is mandatory in a hosted-environment and optional in a non-hosted environment.

```yaml
Type: SPSiteSubscriptionPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
