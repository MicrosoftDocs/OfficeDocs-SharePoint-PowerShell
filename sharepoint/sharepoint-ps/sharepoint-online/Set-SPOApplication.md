---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Set-SPOApplication
Applicable: SharePoint Embedded
title: Set-SPOApplication
schema: 2.0.0
author: ShreyasSar26
ms.author: shssaravanan
ms.reviewer:
---

# Set-SPOApplication

## SYNOPSIS

Sets or updates one or more configuration of a SharePoint Embedded application.

## SYNTAX

```
Set-SPOApplication [-OwningApplicationId] <Guid> [[-SharingCapability] <SharingCapabilities>]
 [-OverrideTenantSharingCapability] <Boolean> [-CopilotEmbeddedChatHosts] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ParamSet1

```powershell
Set-SPOApplication 
[[-OwningApplicationId] <Guid>] 
[[–SharingCapability] <SharingCapability>] 
[[-OverrideTenantSharingCapability] <Boolean>]
[[-CopilotEmbeddedChatHosts] <String>]
```

## DESCRIPTION

`Set-SPOApplication` cmdlet is used to set the configuration properties of a specific application, determined by the `OwningApplicationId`.

You must be a SharePoint Embedded Administrator to run the cmdlet.

> [!NOTE]   
> The OwningApplicationId for Microsoft Loop is `a187e399-0c36-4b98-8f04-1edc167a0996`.
> The OwningApplicationId for Microsoft Designer is `5e2795e3-ce8c-4cfb-b302-35fe5cd01597`.

To invite people outside your organization, please make sure [Microsoft Entra B2B](/sharepoint/sharepoint-azureb2b-integration) is enabled. 

## EXAMPLES

### Example 1

```powershell
Set-SPOApplication -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 -OverrideTenantSharingCapability $false
```

This example disables the override sharing capability, aligning this SharePoint Embedded application's sharing settings with sharing capability of the SharePoint Online.

### Example 2

```powershell
Set-SPOApplication -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 -OverrideTenantSharingCapability $true -SharingCapability -Disabled
```

This example enables the override, restricting file sharing within the SharePoint Embedded application to internal company users only, regardless of the broader SharePoint Online tenant settings.

### Example 3

```powershell
Set-SPOTenant -EnableAzureADB2BIntegration $true
Set-SPOApplication -OwningApplicationId 423poi45-jikl-9bnm-b302-1234ghy56789 -OverrideTenantSharingCapability $true -SharingCapability -ExternalUserandGuestSharing
```
This example demonstrates how to enable file sharing within the SharePoint Embedded application for external users. Note that B2B integration must be enabled to allow guest invitations to SharePoint Embedded apps.

### Example 4

```powershell
Set-SPOApplication -OwningApplicationId 423poi45 -CopilotEmbeddedChatHosts "http://localhost:3000 https://prepspo.spgrid.com https://pemdevtenant.myownsite.com" 
```
This example sets the host URLs for the application with Id 423poi45.

## PARAMETERS

### -OwningApplicationId

This parameter specifies the ID of the SharePoint Embedded application.

  
```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### -SharingCapability

Determines what level of sharing is available for the SharePoint Embedded Application.

The valid values are:  

- ExternalUserAndGuestSharing (default) - External user sharing (share by email) and guest link sharing are both enabled.
- Disabled - External user sharing (share by email) and guest link sharing are both disabled.
- ExternalUserSharingOnly - External user sharing (share by email) is enabled, but guest link sharing is disabled.
- ExistingExternalUserSharingOnly - Only guests already in your organization's directory.

The default setting is None, meaning the application follows the SharePoint Online tenant-level sharing settings. Use the `Get-SPOTenant` cmdlet to view these settings.

```yaml
Type: SharingCapabilities
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Embedded
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideTenantSharingCapability

This setting allows the application to independently set its sharing capabilities, overriding the tenant-level settings of SharePoint Online. Options:

- False (default) - The application follows the tenant-level sharing capability
- True - The application's sharing settings are independent of the tenant level sharing capability

```yaml
Type: Boolean
Applicable: SharePoint Embedded
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```
### -CopilotEmbeddedChatHosts

This parameter is used to add host URLs responsible for driving the Copilot embedded chat functionality in the SharePoint Embedded application.

```yaml
Type: String
Applicable: SharePoint Embedded
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgressAction
Determines how PowerShell responds to progress updates generated by a script, cmdlet, or provider, such as the progress bars generated by the [Write-Progress](https://learn.microsoft.com/powershell/module/microsoft.powershell.utility/write-progress?view=powershell-7.5) cmdlet. 

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: proga

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Get-SPOApplication](Get-SPOApplication.md)

[Set-SPOTenant](set-spotenant.md)
