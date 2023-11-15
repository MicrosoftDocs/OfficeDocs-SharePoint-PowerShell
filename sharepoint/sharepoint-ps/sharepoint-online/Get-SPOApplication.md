---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: # https://learn.microsoft.com/powershell/module/sharepoint-online/get-sposite
applicable: SharePoint Online
title: Get-SPOApplication
schema: 2.0.0git 
author: cindy-lay
ms.author: cindylay
ms.reviewer:
---

# Get-SPOApplication

## SYNOPSIS

Returns a list of applications in the logged in tenant.

## SYNTAX

### ParamSet1

```powershell
Get-SPOApplication [[-OwningApplicationId] <OwningApplicationid>]
```

### ParamSet2

```powershell
Get-SPOApplication [[-OwningApplicationId] <OwningApplicationid>] [[-ApplicationId] <ApplicationId>]
``` 

## DESCRIPTION

The `Get-SPOApplication` cmdlet retrieves and returns all third party applications registered on a tenant site that match the given criteria. You need to be a SharePoint Online administrator or Global Administrator to run the cmdlet. For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps). 


## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Get-SPOApplication
```

Example 1 returns all applications associated with the logged in tenant

### -----------------------EXAMPLE 2-----------------------------

```powershell
Get-SPOApplication -OwningApplicationId <OwningApplicationId>
```

Example 2 lists the owning app details "registered" in their tenant

### -----------------------EXAMPLE 3-----------------------------

```powershell
Get-SPOApplication -OwningApplicationId <OwningApplicationId> -ApplicationId <ApplicationId>
```

Example 3 enumerates permissions that "owning" applications registered in the specified tenant have

 

## PARAMETERS

### -OwningApplicationId

Use this parameter to get details about apps registered in the specific tenant

The following details are returned:

- OwningApplicationId

- OwningApplicationName

- Storage

- Applications (by id)

  
```yaml
Type: String
Parameter Sets: ParamSet1
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId

Enumerate permissions that "owning" applications registered in the logged in tenant have.

```yaml
Type: String
Parameter Sets: ParamSet2
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
 

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
