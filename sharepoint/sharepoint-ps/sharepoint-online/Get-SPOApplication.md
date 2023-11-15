---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: 
applicable: SharePoint Online
title: Get-SPOApplication
schema: 2.0.0
author: akanksha-rakesh, cindy-lay
ms.author: arakesh, cindylay
ms.reviewer:
---

# Get-SPOApplication

## SYNOPSIS

Returns a list of SharePoint repository services applications in the specified tenant.

## SYNTAX

### ParamSet1

```powershell
Get-SPOApplication [[-OwningApplicationId] <OwningApplicationid>] [<CommonParameters>]
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

Example 1 returns all applications registered in the specified tenant.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Get-SPOApplication -OwningApplicationId <OwningApplicationId>
```

Example 2 lists the details of the owning applications "registered" in the specified tenant.

### -----------------------EXAMPLE 3-----------------------------

```powershell
Get-SPOApplication -OwningApplicationId <OwningApplicationId> -ApplicationId <ApplicationId>
```

Example 3 enumerates permissions of the owning applications registered in the specified tenant.

 

## PARAMETERS

### -OwningApplicationId

Use this parameter to get details about apps registered in the specified tenant

The following details are returned:

- OwningApplicationId

- OwningApplicationName

- Storage

- Applications (by id)

  
```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId

Use this parameter to enumerate permissions of the "owning" applications registered in the specified tenant.

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


## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](https://learn.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[Get-SPOContainer](./Get-SPOContainer.md)
