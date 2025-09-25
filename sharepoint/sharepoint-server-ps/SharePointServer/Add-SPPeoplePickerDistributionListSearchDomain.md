---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/add-sppeoplepickerdistributionlistsearchdomain
applicable: SharePoint Server Subscription Edition
title: Add-SPPeoplePickerDistributionListSearchDomain
schema: 2.0.0
---

# Add-SPPeoplePickerDistributionListSearchDomain

## SYNOPSIS
This cmdlet adds a domain to the People Picker distribution list search domains.

## SYNTAX

```
Add-SPPeoplePickerDistributionListSearchDomain -WebApplication <SPWebApplicationPipeBind> -DomainName <String>
 [-Index <Int32>] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The list of distribution list search domain restricts the search of a distribution list to a specific subset of domains.
This Add-SPPeoplePickerDistributionListSearchDomain cmdlet adds a domain to the distribution list search domain list.

## EXAMPLES

### EXAMPLE 1
```powershell
Add-SPPeoplePickerDistributionListSearchDomain -WebApplication http://MyOfficeApp1 -DomainName "corp.contoso.com" -Index 2
```

This example inserts domain "corp.contoso.com" to the distribution list search domain list of Web application MyOfficeApp1 at position 2.
If the length of the list was less than 2 before the insert, an exception will be thrown.

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -DomainName

> Applicable: SharePoint Server Subscription Edition

The domain name to add in the list.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Index

> Applicable: SharePoint Server Subscription Edition

The position to insert the domain in the list begin from 0.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

The Web application to modify the distribution list search domain list to.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before running the cmdlet.

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

### -WhatIf

> Applicable: SharePoint Server Subscription Edition

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
