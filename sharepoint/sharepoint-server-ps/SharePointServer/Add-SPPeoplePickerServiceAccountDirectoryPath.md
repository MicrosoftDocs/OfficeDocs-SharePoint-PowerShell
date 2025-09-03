---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/add-sppeoplepickerserviceaccountdirectorypath
applicable: SharePoint Server Subscription Edition
title: Add-SPPeoplePickerServiceAccountDirectoryPath
schema: 2.0.0
ms.date: 08/26/2025
---

# Add-SPPeoplePickerServiceAccountDirectoryPath

## SYNOPSIS
This cmdlet adds an OU to People Picker service account directory path list.

## SYNTAX

```
Add-SPPeoplePickerServiceAccountDirectoryPath -WebApplication <SPWebApplicationPipeBind>
 -OrganizationalUnitName <String> [-Index <Int32>] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Administrative user accounts are often located in a different OU from regular site users.
If user has forced People Picker to only return query results from a specific OU, the OU should also be added into the service account directory path so the administrator can manage the site collection.
This Add-SPPeoplePickerServiceAccountDirectoryPath cmdlet adds an OU into the service account directory path list.

## EXAMPLES

### EXAMPLE 1
```powershell
Add-SPPeoplePickerServiceAccountDirectoryPath -WebApplication http://MyOfficeApp1 -OUName "OU=FarmAdmin,DC=Contoso,DC=local"
```

This example adds OU "FarmAdmin" to the service account directory path list of Web application MyOfficeApp1, so that Administrator can use People Picker to get users that are in the OU "FarmAdmin"

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

### -Index

> Applicable: SharePoint Server Subscription Edition

The position to insert the domain in the list beginning with 0.

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

### -OrganizationalUnitName

> Applicable: SharePoint Server Subscription Edition

{{ Fill OrganizationalUnitName Description }}

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

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

The Web application to modify the service account directory path list to.

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
