---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/set-spappautoprovisionconnection
applicable: SharePoint Server Subscription Edition
title: Set-SPAppAutoProvisionConnection
schema: 2.0.0
---

# Set-SPAppAutoProvisionConnection

## SYNOPSIS
Sets provision connection settings for an app.

## SYNTAX

### WebHostEndPoint
```
Set-SPAppAutoProvisionConnection -ConnectionType <ConnectionTypes> -EndPoint <String>
 [-AssignmentCollection <SPAssignmentCollection>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]
 [<CommonParameters>]
```

### WebHostSetup
```
Set-SPAppAutoProvisionConnection -ConnectionType <ConnectionTypes> -EndPoint <String> -Password <String>
 -Username <String> [-AssignmentCollection <SPAssignmentCollection>]
 [-SiteSubscription <SPSiteSubscriptionPipeBind>] [<CommonParameters>]
```

### WebHostCredential
```
Set-SPAppAutoProvisionConnection -ConnectionType <ConnectionTypes> -Password <String> -Username <String>
 [-AssignmentCollection <SPAssignmentCollection>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]
 [<CommonParameters>]
```

### Remove
```
Set-SPAppAutoProvisionConnection [-Remove] [-AssignmentCollection <SPAssignmentCollection>]
 [-SiteSubscription <SPSiteSubscriptionPipeBind>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

Use the `Set-SPAppAutoProvisionConnection` cmdlet to set provision connection settings for a specified app.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Set-SpAppAutoProvisionConnection -ConnectionType RemoteWebHost -EndPoint https://SPremotewebhost -Password passname -Username <username>
```

This example configures remote web host to be used provision apps that use this functionality for the default site subscription server on https://SPremotewebhost.

### EXAMPLE 2
```powershell
$subscription = Get-SPSiteSubscription https://Contoso.com
Set-SPAppAutoProvisionConnection -ConnectionType RemoteWebHost -EndPoint https://SPremotewebhost -Password passname -Username <username> -SiteSubscription $subscription
```

This example configures remote web host to be used provision apps that use this functionality for the site subscription of Contoso.com site to server on https://SPremotewebhost.

### EXAMPLE 3
```powershell
Set-SPAppAutoProvisionConnection -ConnectionType RemoteWebHost -EndPoint https://SPremotewebhost
```

This example updates the endpoint of the already configured remote web host server https://SPRemotewebhost for the default site subscription.

### EXAMPLE 4
```powershell
Set-SPAppAutoProvisionConnection -ConnectionType RemoteWebHost -Remove
```

This example removes the remote web host configuration for the default site subscription.

## PARAMETERS

### -ConnectionType

> Applicable: SharePoint Server Subscription Edition

Specifies the connection type to provision.

```yaml
Type: ConnectionTypes
Parameter Sets: WebHostEndPoint, WebHostSetup, WebHostCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndPoint

> Applicable: SharePoint Server Subscription Edition

Specifies the end point of the provision connection.

```yaml
Type: String
Parameter Sets: WebHostEndPoint, WebHostSetup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password

> Applicable: SharePoint Server Subscription Edition

Specifies the password for the provision connection.

```yaml
Type: String
Parameter Sets: WebHostSetup, WebHostCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Remove

> Applicable: SharePoint Server Subscription Edition

Removes the auto provision connection of the app.

```yaml
Type: SwitchParameter
Parameter Sets: Remove
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username

> Applicable: SharePoint Server Subscription Edition

Specifies the user name of the connection.

```yaml
Type: String
Parameter Sets: WebHostSetup, WebHostCredential
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

### -SiteSubscription

> Applicable: SharePoint Server Subscription Edition

Specifies the site collection for which the provision connection is to be associated.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-SPAppAutoProvisionConnection](Get-SPAppAutoProvisionConnection.md)
