---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-sppeoplepickerconfig
applicable: SharePoint Server Subscription Edition
title: Set-SPPeoplePickerConfig
schema: 2.0.0
---

# Set-SPPeoplePickerConfig

## SYNOPSIS
This cmdlet sets settings of People Picker of a specified Web application.

## SYNTAX

```
Set-SPPeoplePickerConfig -WebApplication <SPWebApplicationPipeBind> [-ActiveDirectoryCustomFilter <String>]
 [-ActiveDirectoryCustomQuery <String>] [-ActiveDirectorySearchTimeout <Int32>]
 [-PeopleEditorOnlyResolveWithinSiteCollection] [-OnlySearchWithinSiteCollection]
 [-NoWindowsAccountsForNonWindowsAuthenticationMode] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf]
 [-SecureSocketsLayer]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
This Set-SPPeoplePickerConfig cmdlet sets the following settings of People Picker of a specified Web application:
        1) The customized query filter sent to AD with People Picker query.
        2) The customized query sent to AD with People Picker query.
        3) The amount of time before AD search time out.
        4) Whether the People Picker control should only return the site collection users when clicking the "Check Names" button.
        5) Whether the People Picker control should only return the site collection users when using the "Select People and Groups" dialog box.
        6) Whether return only non-Active Directory users when the Web application uses form-based authentication.
        7) Whether to enable Secure LDAP (LDAPS) for secure communication.

## EXAMPLES

### EXAMPLE 1
```powershell
Set-SPPeoplePickerConfig -WebApplication http://MyOfficeApp1 -ActiveDirectoryCustomFilter "((Title=Manager))" -ActiveDirectoryCustomQuery (sn={0}*) -ActiveDirectorySearchTimeout 60 -PeopleEditorOnlyResolveWithinSiteCollection -OnlySearchWithinSiteCollection -NoWindowsAccountsForNonWindowsAuthenticationMode
```

This example sets the following settings to the People Picker of Web application MyOfficeApp1:
            - Return a list of Active Directory users with a title of "Manager"
            - The query only searches on the last name
            - 60 seconds before Active Directory search times out
            - The People Picker control should only return the site collection users when clicking the "Check Names" button
            - The People Picker control should only return the site collection users when useing the "Select People and Groups" dialog box
            - The People Picker control return only non-Active Directory users when the Web application uses forms-based authentication

## PARAMETERS

### -ActiveDirectoryCustomFilter

> Applicable: SharePoint Server Subscription Edition

The Lightweight Directory Access Protocol (LDAP) query string to create a customized filter for displaying query results.

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

### -ActiveDirectoryCustomQuery

> Applicable: SharePoint Server Subscription Edition

The Lightweight Directory Access Protocol (LDAP) query string appended to the People Picker query to Active Directory.

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

### -ActiveDirectorySearchTimeout

> Applicable: SharePoint Server Subscription Edition

The amount of seconds of time before Active Directory search times out.

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

### -NoWindowsAccountsForNonWindowsAuthenticationMode

> Applicable: SharePoint Server Subscription Edition

Specifies the People Picker control return only non-Active Directory users when the Web application uses form-based authentication.

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

### -OnlySearchWithinSiteCollection

> Applicable: SharePoint Server Subscription Edition

Specifies the People Picker control should only return the site collection users when using the "Select People and Groups" dialog box.

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

### -PeopleEditorOnlyResolveWithinSiteCollection

> Applicable: SharePoint Server Subscription Edition

Specifies the People Picker control should only return the site collection users when click the "Check Names" button.

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

Specifies whether to enable Secure LDAP (LDAPS) for secure communication in the SharePoint People Picker.

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

The Web application to set People Picker settings to.

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
