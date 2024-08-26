---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainer
applicable: SharePoint Online
title: Set-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: ShreyasSar26
ms.reviewer:
---
 
# Set-SPOContainerType
 
## SYNOPSIS
 
Sets or updates one or more property values of a trial or standard container type.
 
## SYNTAX
 
### ParamSet1
 
```powershell
Set-SPOContainerType -ContainerTypeId <ContainerTypeId> -OwningApplicationId <OwningApplicationId> -ContainerTypeName <ContainerTypeName>
```
### ParamSet2
```powershell
Set-SPOContainerType -ContainerTypeId <ContainerTypeId> -AzureSubscriptionId <AzureSubscriptionId> -ResourceGroup <ResourceGroup>
```
 
## DESCRIPTION
The Set-SPOContainertype cmdlet is used to reset the parameters associated with a container type - both trial and standard. The cmdlet can be used to change the container type name or the associated billing profile of the contianer type.
## EXAMPLES
 
### Example 1
 
```powershell
Set-SPOContainerType -ContainerTypeId DA1D89B3-B4CF-4C0A-8E1C-0D131C57544F -OwningApplicationId 12A9D93C-18D7-46A0-B43E-28D20ADDD56A - ContainerTypeName “Red Container Type“ 
```
 
Example 1 sets the container type name as "Red Container Type"
```powershell
Are you sure you want to perform this action?​

Performing the operation "Set-SPOContainerType".​

[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): Y​

Success ​

ContainerTypeId     : DA1D89B3-B4CF-4C0A-8E1C-0D131C57544F​

OwningApplicationId	: 994B9586-253E-4A77-B51​

ContainerTypeName   : Red Container Type​ 
```
 
### Example 2
 
```powershell
Set-SPOContainerType -ContainerTypeId DA1D89B3-B4CF-4C0A-8E1C-0D131C57544F –Azure Subscription 01F62754-0873-4EC6-AB4A-3EED48BA8BE7 -ResourceGroup RG200
```
 
In this example, the billing profile of the container type is updated with the latest information.
```powershell
​
Are you sure you want to perform this action?​

Performing the operation "Set-SPOContainerType".​

[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): Y​
​

​ContainerTypeId     : DA1D89B3-B4CF-4C0A-8E1C-0D131C57544F​

Azure Subscription  : 01F62754-0873-4EC6-AB4A-3EED48BA8BE7​

Resource Group	: RG200
```
### Example 3
 
```powershell
Set-SPOContainerType -ContainerTypeId 01F62754-0873-4EC6-AB4A-3EED48BA8BE7 -OwningApplicationId 994B9586-253E-4A77-B51 - ContainerTypeName “Blue Container Type“ 
```
In this example, the trial container type details are changed as follows:

```powershell
Are you sure you want to perform this action?​

Performing the operation "Set-SPOContainerType".​

[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): Y​
​
Success ​


ContainerTypeId     : 01F62754-0873-4EC6-AB4A-3EED48BA8BE7​

OwningApplicationId	: 994B9586-253E-4A77-B51 ​

ContainerTypeName   : Blue Container Type
```

 
## PARAMETERS
 

### -ContainerTypeName

This parameter names your ContainerType for your SharePoint Embedded Application

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

### -OwningApplicationId

Use this parameter to specify the Container in the given OwningApplicationId.

```yaml
Type: String
Parameter Sets: ParamSet4, ParamSet5
Aliases:
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureSubscriptionId

This parameter can be used when there are more than 5,000 Containers in a given SharePoint Embedded application. Using `-Paged` will provide a `<Paging Token>` that will display the next 5,000 Containers.

```yaml
Type: String
Parameter Sets: ParamSet2, ParamSet3
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### -ResourceGroup

Use this parameter to provide the `<Paging Token>` provided to view the remaining Containers as shown in Example 5. If there are no more Containers to display, the commandlet output will return the message `End of Containers view.` Otherwise, use the given `<Paging Token>` to retrieve the next batch of up to 5,000 ontainers.

```yaml
Type: String
Parameter Sets: ParamSet2, ParamSet3
Aliases:
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
