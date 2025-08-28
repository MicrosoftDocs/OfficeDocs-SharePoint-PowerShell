---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/remove-sppeoplepickersearchaddomain
applicable: SharePoint Server Subscription Edition
title: Remove-SPPeoplePickerSearchADDomain
schema: 2.0.0
---

# Remove-SPPeoplePickerSearchADDomain

## SYNOPSIS
This cmdlet removes a forest of domain from the list that the People Picker uses when searching for users.

## SYNTAX

```
Remove-SPPeoplePickerSearchADDomain -WebApplication <SPWebApplicationPipeBind> -DomainName <String> [-IsForest]
 [-UserName <String>] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
This Remove-SPPeoplePickerSearchADDomain cmdlet removes a forest or domain with domain name and optional login name from the list of Active Directory domains used by People Picker.

## EXAMPLES

### EXAMPLE 1
```powershell
Remove-SPPeoplePickerSearchADDomain -WebApplication http://MyOfficeApp1 -DomainName "corp.contoso.com" -IsForest
```

This example removes forest corp.contoso.com from the People Picker search Active Directory domain list of the Web application MyOfficeApp1.

### EXAMPLE 2
```powershell
Remove-SPPeoplePickerSearchADDomain -WebApplication http://MyOfficeApp1 -DomainName "corp.contoso.com" -UserName "contoso\user"
```

This example removes domain corp.contoso.com from the People Picker search Active Directory domain list of the Web application MyOfficeApp1, with login name contoso\user.

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

Name of the domain or forest.

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

### -IsForest

> Applicable: SharePoint Server Subscription Edition

Specifies that the name specified by the DomainName parameter is an Active Directory forest.
If the IsForest parameter is omitted, the name specified by the DomainName parameter is treated as an Active Directory domain.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName

> Applicable: SharePoint Server Subscription Edition

The login name of the forest or domain.

If this is not specified, it will match domains with empty login name.

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

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

The Web application to remove the People Picker forest/domain settings from.

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

Prompts you for confirmation before executing the command.
For more information, type the following command: get-help about_commonparameters

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
