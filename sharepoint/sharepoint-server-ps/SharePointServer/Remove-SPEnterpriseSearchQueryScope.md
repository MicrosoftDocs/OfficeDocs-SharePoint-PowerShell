---
external help file: Microsoft.Office.Server.Search.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/remove-spenterprisesearchqueryscope
applicable: SharePoint Server Subscription Edition
title: Remove-SPEnterpriseSearchQueryScope
schema: 2.0.0
---

# Remove-SPEnterpriseSearchQueryScope

## SYNOPSIS
Deletes a query scope.

## SYNTAX

```
Remove-SPEnterpriseSearchQueryScope [-Identity] <ScopePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-SearchApplication <SearchServiceApplicationPipeBind>] [-Url <Uri>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
After you upgrade a Search service application to SharePoint Server, you can view shared scopes, but you cannot create, update, or delete them.
Therefore, you cannot use this cmdlet for shared scopes after upgrade.
However, you can convert shared scopes to result sources, which serve a similar purpose.
Similarly, after you upgrade a SharePoint Server site collection to SharePoint Server, you can view local scopes, but you cannot create, update, or delete them.
Therefore, you cannot use this cmdlet for local scopes after you upgrade a site collection.
However, you can convert local scopes to result sources, which serve a similar purpose.

The `Remove-SPEnterpriseSearchQueryScope` cmdlet deletes one or more specified shared scopes from the query scope collection.
A query scope represents a query results scope used by all shared search applications on the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPenterpriseSearchServiceApplication -Identity MySSA
Get-SPEnterpriseSearchQueryScope -Identity MustCrawl -SearchApplication $ssa | Remove-SPEnterpriseSearchQueryScope
```

This example removes a scope named MustCrawl from a search service application named MySSA.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the query scope to delete.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a scope (for example, Scope1); or an instance of a valid Scope object.

```yaml
Type: ScopePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application that contains the query scope collection.

The type must be a valid GUID, of the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Url

> Applicable: SharePoint Server Subscription Edition

Filters to delete scopes of the specified results URL.

The type must be a valid URL, in the form https://server_name.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: u

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
