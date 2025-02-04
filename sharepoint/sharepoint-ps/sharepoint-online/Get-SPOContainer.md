---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainer
applicable: SharePoint Online
title: Get-SPOContainer
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Get-SPOContainer

## SYNOPSIS

Returns one or more containers in a SharePoint Embedded application. 

## SYNTAX

### ParamSet1

```powershell
Get-SPOContainer -Identity <ContainerId> [<CommonParameters>]
```

### ParamSet2

```powershell
Get-SPOContainer -OwningApplicationId <OwningApplicationId> [<CommonParameters>]
```

### ParamSet3
```powershell
Get-SPOContainer -OwningApplicationId <OwningApplicationId> [-Paged] [<CommonParameters>]
```

### ParamSet4
```powershell
Get-SPOContainer -OwningApplicationId <OwningApplicationId> [-Paged] [-PagingToken <TokenString>] [<CommonParameters>]
```

### ParamSet5

```powershell
Get-SPOContainer -OwningApplicationId <OwningApplicationId> [-SortByStorage <Ascending | Descending>] [<CommonParameters>]
```

### ParamSet6

```powershell
Get-SPOContainer -OwningApplicationId <OwningApplicationId> [-SortByStorage <Ascending | Descending>] [-Paged] [<CommonParameters>]
```
### ParamSet7

```powershell
Get-SPOContainer -OwningApplicationId <OwningApplicationId> [-SortByStorage <Ascending | Descending>] [-Paged] [-PagingToken <TokenString>] [<CommonParameters>]
```

## DESCRIPTION

The `Get-SPOContainer` cmdlet retrieves and returns the details of an individual container when paired with `Identity` parameter, where the container ID needs to be mentioned. The cmdlet returns the list of containers belonging to a SharePoint Embedded application when paired with the `OwningApplicationId` parameter. 

You must be a SharePoint Embedded Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).


> [!NOTE]  
> Containers in the Recycle Bin will not be retrieved by using the `Get-SPOContainer` cmdlet. 
> The OwningApplicationId for Microsoft Loop is `a187e399-0c36-4b98-8f04-1edc167a0996`.
> The OwningApplicationId for Microsoft Designer is `5e2795e3-ce8c-4cfb-b302-35fe5cd01597`.

## EXAMPLES

### Example 1

```powershell
Get-SPOContainer -Identity b66f5b2e
```

Example 1 returns the detailed properties of the Container with associated Container ID b66f5b2e.

### Example 2

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 | ft 
```
Example 2 returns a tabular list of Containers created under the SharePoint Embedded application with the `OwningApplicationId` of  `423poi45`.

 
### Example 3

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 -Paged | ft
```
Example 3 uses the `-Paged` command to retrieve a paging token.

### Example 4

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 -Paged -PagingToken <zacad> | ft 
```

Example 4 uses the `-PagingToken` parameter along with the `-Paged` parameter to view more containers that were not displayed in Example 3.

### Example 5

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 -SortByStorage Ascending
```

Example 5 displays the containers belonging to the application, sorted in ascending order of storage.

### Example 6

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 -SortByStorage Ascending -Paged
```

Example 6 displays a paged view of the the containers belonging to the application, sorted in ascending order of storage.

### Example 7

```powershell
Get-SPOContainer -OwningApplicationId 423poi45-as -SortByStorage Ascending -Paged -PagingToken <zacad>
```

Example 7 displays the next list of paged view of containers belonging to the application, sorted in ascending order of storage.


## PARAMETERS

### -OwningApplicationId

This parameter specifies the ID of the SharePoint Embedded application. Use the `Get-SPOApplication` command to retrieve the OwningApplicationId.
 
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

### -Identity

Use this parameter to specify the Container ID.
 
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

### -Paged

This parameter can be used when there are more than 200 Containers in a given SharePoint Embedded application. Using `-Paged` will provide a paging token that will display the next 200 Containers.

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


### -PagingToken

Use this parameter to provide the paging token provided to view the remaining Containers as shown in Example 4. If there are no more Containers to display, the cmdlet output will return the message `End of containers view.` Otherwise, use the given paging token to retrieve the next batch of up to 200 Containers.

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

### -SortByStorage

This parameter can be used when you need to see the list of containers, sorted by storage. 

```yaml
Type: String
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
## RELATED LINKS

[Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)

[Get-SPOApplication](./Get-SPOApplication.md)

[Set-SPOContainer](./Set-SPOContainer.md)

[Get-SPODeletedContainer](./Get-SPODeletedContainer.md)

[Remove-SPOContainer](./Remove-SPOContainer.md)

[Remove-SPODeletedContainer](./Remove-SPODeletedContainer.md)

[Restore-SPODeletedContainer](./Restore-SPODeletedContainer.md)


