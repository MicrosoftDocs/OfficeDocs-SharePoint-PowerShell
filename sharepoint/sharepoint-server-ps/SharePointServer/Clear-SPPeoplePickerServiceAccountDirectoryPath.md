---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/clear-sppeoplepickerserviceaccountdirectorypath
applicable: SharePoint Server Subscription Edition
title: Clear-SPPeoplePickerServiceAccountDirectoryPath
schema: 2.0.0
---

# Clear-SPPeoplePickerServiceAccountDirectoryPath

## SYNOPSIS
This cmdlet clears the OUs of People Picker service account directory path list.

## SYNTAX

```
Clear-SPPeoplePickerServiceAccountDirectoryPath -WebApplication <SPWebApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Administrative user accounts are often located in a different OU from regular site users.
If user has forced People Picker to only return query results from a specific OU, the OU should also be added into the service account directory path so the administrator can manage the site collection.
This Clear-SPPeoplePickerServiceAccountDirectoryPath cmdlet clears the OUs of the service account directory path list.

## EXAMPLES

### -------------EXAMPLE 1------------- 
```powershell
Clear-SPPeoplePickerServiceAccountDirectoryPath -WebApplication http://MyOfficeApp1
```

This example clears OUs of the service account directory path list of Web application MyOfficeApp1.

## PARAMETERS

### -AssignmentCollection
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
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebApplication
The Web application to clear the service account directory path list to.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: SharePoint Server Subscription Edition

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
