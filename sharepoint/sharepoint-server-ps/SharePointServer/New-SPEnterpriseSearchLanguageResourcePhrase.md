---
external help file: Microsoft.Office.Server.Search.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/new-spenterprisesearchlanguageresourcephrase
applicable: SharePoint Server Subscription Edition
title: New-SPEnterpriseSearchLanguageResourcePhrase
schema: 2.0.0
---

# New-SPEnterpriseSearchLanguageResourcePhrase

## SYNOPSIS
Adds a language resource phrase to a shared search application.

## SYNTAX

```
New-SPEnterpriseSearchLanguageResourcePhrase [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 -Language <String> [-Mapping <String>] -Name <String> -Owner <SearchObjectOwner>
 -SearchApplication <SearchServiceApplicationPipeBind> [-SourceId <Guid>] -Type <LanguageResourceType>
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The `New-SPEnterpriseSearchLanguageResourcePhrase` cmdlet adds a query keyword phrase to a shared search application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
New-SPEnterpriseSearchLanguageResourcePhrase -SearchApplication $ssa -Language en-us -Type QuerySuggestionBlockList -Name secret
```

This example adds a new entry to the QuerySuggestionBlockList for the en-us language.

## PARAMETERS

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

### -Language

> Applicable: SharePoint Server Subscription Edition

Adds the phrase for the specified source language.

The type must be a valid name of a language; for example, en-us or ja-jp.

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

### -Mapping

> Applicable: SharePoint Server Subscription Edition

Allows a term or phrase to be mapped to another term or phrase.
For example, the nickname "John" could be mapped to "Jonathan".

This parameter only applies to nicknames and substitutions.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the term to add to the list specified in the Type parameter.

The type must be a valid name of a language resource phrase (for example, LanguageResourcePhrase1).

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

### -Owner

> Applicable: SharePoint Server Subscription Edition

Specifies the search object owner that defines the scope at which the corresponding LanguageResourcePhrase is created.

The owner must be one of the following valid levels:

- Search Service Application
- Site Subscription
- Site Collection
- Site

```yaml
Type: SearchObjectOwner
Parameter Sets: (All)
Aliases: o

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application that contains the language resources.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceId

> Applicable: SharePoint Server Subscription Edition

Identifies the search result source for which the LanguageResourcePhrase applies to.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type

> Applicable: SharePoint Server Subscription Edition

Specifies the type of the new phrase.

The type must be one of the following valid types of phrases:

- QuerySuggestionBlockList
- QuerySuggestionAlwaysSuggest
- Nickname
- QuerySuggestionSubstitution

```yaml
Type: LanguageResourceType
Parameter Sets: (All)
Aliases:

Required: True
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
