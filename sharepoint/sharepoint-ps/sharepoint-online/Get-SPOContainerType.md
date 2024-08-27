---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainertype
applicable: SharePoint Online
title: Get-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: ShreyasSar26
ms.reviewer:
---

# Get-SPOContainerType

## SYNOPSIS

Returns one or more container types created in the tenant. 

## SYNTAX

### ParamSet1

```powershell
Get-SPOContainerType 
```
### ParamSet2
```powershell
Get-SPOContainerType [-ContainerTypeId <ContainerTypeId>] 
```

## DESCRIPTION

The Get-SPOContainerType cmdlet returns all the container types present in the tenant or details of a specific container type when paired with the containertype Id parameter. 

You must be a SharePoint Embedded administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the online documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).

## EXAMPLES

### Example 1

```powershell
Get-SPOContainerType 
```

Example output of the Get-SPOContainerType cmdlet 

```powershell
ContainerTypeId     : 40f7cbcf-5db4-46a6-c99b-acdae53d1ce1 

ContainerTypeName   : Contoso_Payroll 

OwningApplicationId : 27e1e2e5-eb75-4909-9c52-65f9fe9a51e0 

Classification      : Standard 

AzureSubscriptionId : f4fce63c-3b6f-4ced-97c6-f96734c3674b 

ResourceGroup       : prod-resources 

 

ContainerTypeId     : 36a2cb87-e16e-5595-b368-66c740e4c95b 

ContainerTypeName   : Contoso_HR 

OwningApplicationId : aa3d7440-3eaf-76a9-8c5a-4fae28b6316f 

Classification      : Standard 

AzureSubscriptionId : f4fce63c-3b6f-4ced-97c6-f69734c3674a 

ResourceGroup       : prod-resources 

 

ContainerTypeId     : 4f0af585-8dcc-0000-223d-661eb2c604e4 

ContainerTypeName   : ContosoLegal 

OwningApplicationId : a735e4af-b86e-0000-93ba-1faded6c39e1 

Classification      : Standard 

AzureSubscriptionId : 564e9025-f7f5-xxx9-9ddd-4cdxxxx1755 

ResourceGroup       : prod-resources 
```

### Example 2

```powershell
Get-SPOContainerType -ContainerTypeId 4f0af585-8dcc-0000-223d-661eb2c604e4 
```
Example output of the Get-SPOContainerType cmdlet 

```powershell
ContainerTypeId     : 4f0af585-8dcc-0000-223d-661eb2c604e4 

ContainerTypeName   : ContosoLegal 

OwningApplicationId : a735e4af-b86e-0000-93ba-1faded6c39e1 

AzureSubscriptionId : 564e9025-f7f5-xxx9-9ddd-4cdxxxx1755 

ResourceGroup       : prod-resources 

Region              : EastUS 

Classification      : Standard 

CreationDate           : 7/2/2024 

ExpiryDate             :  
```

## PARAMETERS

### -ContainerTypeId
 
This parameter specifies the ID of the containertype corresponding to the SharePoint Embedded application.
```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
