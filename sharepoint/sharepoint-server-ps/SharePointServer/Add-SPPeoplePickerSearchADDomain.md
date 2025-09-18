---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/add-sppeoplepickersearchaddomain
applicable: SharePoint Server Subscription Edition
title: Add-SPPeoplePickerSearchADDomain
schema: 2.0.0
---

# Add-SPPeoplePickerSearchADDomain

## SYNOPSIS
This cmdlet adds a forest or domain to the list that the People Picker uses when searching for users.

## SYNTAX

```
Add-SPPeoplePickerSearchADDomain -WebApplication <SPWebApplicationPipeBind> -DomainName <String> [-IsForest]
 [-Index <Int32>] [-Credential <PSCredential>] [-AssignmentCollection <SPAssignmentCollection>] [-SecureSocketsLayer]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
This Add-SPPeoplePickerSearchADDomain cmdlet adds a forest or domain with domain name and optional login name and password to the list of Active Directory domains used by People Picker.

## EXAMPLES

### EXAMPLE 1
```powershell
Add-SPPeoplePickerSearchADDomain -WebApplication http://MyOfficeApp1 -DomainName "corp.contoso.com" -IsForest
```

This example adds forest corp.contoso.com to the People Picker search Active Directory domain list of the Web application MyOfficeApp1.

### EXAMPLE 2
```powershell
Add-SPPeoplePickerSearchADDomain -WebApplication http://MyOfficeApp1 -DomainName "corp.contoso.com" -Credential (New-Object System.Management.Automation.PSCredential "contoso\user", (ConvertTo-SecureString "password" -AsPlainText -Force))
```

This example adds domain corp.contoso.com to the People Picker search Active Directory domain list of the Web application MyOfficeApp1, with login name user and password password.

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

### -Credential

> Applicable: SharePoint Server Subscription Edition

The login name and password used by People Picker for authenticating to a forest or domain that it doesn't have a two-way trust relationship with.

This parameter is not neccessary if it has a two-way trust relationship with the forest or domain specified by the DomainName parameter.

If this parameter is not specified, then no login name and password will be used.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainName

> Applicable: SharePoint Server Subscription Edition

Name of the forest or domain.

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

The position to insert the forest or domain in the list begin from 0.

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

### -IsForest

> Applicable: SharePoint Server Subscription Edition

Whether the name specified by the DomainName parameter is an active directory forest or an Active Directory domain.

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

### -SecureSocketsLayer

> Applicable: SharePoint Server Subscription Edition

Specifies whether the newly added forest or domain should enable Secure LDAP (LDAPS).

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

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

The Web application to add the People Picker forest/domain search setting to.

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
