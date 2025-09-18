---
external help file: Microsoft.Office.Server.Search.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/set-spenterprisesearchqueryscope
applicable: SharePoint Server Subscription Edition
title: Set-SPEnterpriseSearchQueryScope
schema: 2.0.0
---

# Set-SPEnterpriseSearchQueryScope

## SYNOPSIS
Sets the properties of a query results scope for a shared search application.

## SYNTAX

```
Set-SPEnterpriseSearchQueryScope -AlternateResultsPage <String>
 [-AssignmentCollection <SPAssignmentCollection>] [-CompilationType <Int32>] [-Confirm] [-Description <String>]
 [-DisplayInAdminUI <Boolean>] -Identity <ScopePipeBind> [-Name <String>]
 [-SearchApplication <SearchServiceApplicationPipeBind>] [-Url <Uri>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
After you upgrade a Search service application to SharePoint Server, you can view shared scopes, but you cannot create, update, or delete them.
Therefore, you cannot use this cmdlet for shared scopes after upgrade.
However, you can convert shared scopes to result sources, which serve a similar purpose.
Similarly, after you upgrade to SharePoint Server Site Collection to SharePoint Server mode, you can view local scopes, but you cannot create, update, or delete them.
Therefore, you cannot use this cmdlet for local scopes after you upgrade a site collection.
However, you can convert local scopes to result sources, which serve a similar purpose.

The `Set-SPEnterpriseSearchQueryScope` cmdlet updates properties of a shared scope.
SPEnterpriseSearchQueryScope represents a query results scope used by all shared search applications on the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPenterpriseSearchServiceApplication
Get-SPEnterpriseSearchQueryScope -Identity MustCrawl -SearchApplication $ssa | Set-SPEnterpriseSearchQueryScope -Description "Business critical sites to index" -CompilationType 1 -AlternateResultsPage https://altServer
```

This example obtains a reference to the scope named MustCrawl on the search service application named MySSA and changes the description, compilation type and alternate access URL.

## PARAMETERS

### -AlternateResultsPage

> Applicable: SharePoint Server Subscription Edition

Specifies the location to display results for the new query scope.

The type must be a valid URL, in the form https://server_name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: u

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

### -CompilationType

> Applicable: SharePoint Server Subscription Edition

Specifies the compilation type of the new scope.
The value 0 specifies the conditionally compiled scope type, and the value 1 specifies the always compiled scope type.

The type must be either of the following: 0 or 1.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: type

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Description

> Applicable: SharePoint Server Subscription Edition

Adds a description of the new query scope.

The type must be a valid string; for example, a description of a query scope.

```yaml
Type: String
Parameter Sets: (All)
Aliases: d

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayInAdminUI

> Applicable: SharePoint Server Subscription Edition

Specifies that the new scope is displayed in the administration application user interface (UI).
The default setting is to hide the new scope in the administration application UI.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: disp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the identity of the scope to create.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a scope (for example, Scope1); or an instance of a valid Scope object.

```yaml
Type: ScopePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies a name for the query scope.

The type must be a valid name of a query scope; for example, QueryScope1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application that contains the query scope collection.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

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

Filters to delete scopes for the specified results URL.

The type must be a valid URL, in the form https://server_name.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

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
