---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spoapplication
applicable: SharePoint
title: Get-SPOApplication
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Get-SPOApplication

## SYNOPSIS

Returns a list of SharePoint Embedded applications in the specified tenant.

## SYNTAX

### ParamSet1

```powershell
Get-SPOApplication []
```
### ParamSet2

```powershell
Get-SPOApplication [[-OwningApplicationId] <OwningApplicationid>] [<CommonParameters>]
```

### ParamSet3

```powershell
Get-SPOApplication [[-OwningApplicationId] <OwningApplicationid>] [[-ApplicationId] <ApplicationId>]
``` 

## DESCRIPTION

The `Get-SPOApplication` cmdlet retrieves and returns SharePoint Embedded applications of all publishers registered in a tenant or a particular application when paired with the `OwningApplicationId` parameter. 

You must be a SharePoint Embedded Administrator to run the cmdlet. 


## EXAMPLES

### Example 1

```powershell
Get-SPOApplication
```

Example 1 returns all SharePoint Embedded applications registered in the specified tenant by their `OwningApplicationId` and `OwningApplicationName`.

### Example 2

```powershell
Get-SPOApplication -OwningApplicationId <OwningApplicationId>
```

Example 2 provides details about the application corresponding to the “Owning Application Id” in the specified tenant. It also returns configuration details of the application such as:
1)	**Applications** that  lists all the guest application IDs with permissions to the owning application.
2)	**SharingCapability** settings and the “OverrideTenantSharingCapability” status. 
3)	**CopilotEmbeddedChatHosts** that lists the host URLs driving the Copilot embedded chat capability on the SharePoint Embedded application.


### Example 3

```powershell
Get-SPOApplication -OwningApplicationId <OwningApplicationId> -ApplicationId <ApplicationId>
```

Example 3 enumerates app-only permissions of the guest application specified in `ApplicationId`.

### Example 4

```powershell
$r = Get-SPOApplication -OwningApplicationId <OwningApplicationId>
$r.CopilotEmbeddedChatHosts
```

Example 4 enumerates the entire list of the host URLs driving the Copilot embedded chat capability on the SharePoint Embedded application.

## PARAMETERS

### -OwningApplicationId

Use this parameter to get details about applications registered in the specified tenant.

The following details are returned:

- OwningApplicationId

- OwningApplicationName

- Applications (by id)

- SharingCapability

- OverrideTenantSharingCapability
  
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

### -ApplicationId

Use this parameter to enumerate app-only permissions of the guest application id with access to the specified owning application.

```yaml
Type: String
Parameter Sets: ParamSet2
Aliases:
Applicable: SharePoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
 
### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).


## RELATED LINKS

[Get-SPOContainer](./Get-SPOContainer.md)
[Set-SPOApplication](./Set-SPOApplication.md)
