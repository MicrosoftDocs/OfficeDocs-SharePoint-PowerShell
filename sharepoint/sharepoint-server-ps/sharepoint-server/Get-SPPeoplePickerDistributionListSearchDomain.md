---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/get-sppeoplepickerdistributionlistsearchdomain
applicable: SharePoint Server Subscription Edition
title: Get-SPPeoplePickerDistributionListSearchDomain
schema: 2.0.0
author:
ms.author:
ms.reviewer:
---

# Get-SPPeoplePickerDistributionListSearchDomain

## SYNOPSIS
Returns all domains in the People Picker distribution list search domains.

## SYNTAX

```
Get-SPPeoplePickerDistributionListSearchDomain -WebApplication <SPWebApplicationPipeBind>
 [-DomainName <String>] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The Get-SPGetPeoplePickerDistributionListSearchDomain cmdlet returns all domains in the People Picker distribution list search domains that match the criteria specified by the parameters.

## EXAMPLES

### -------------EXAMPLE 1------------- 
```powershell
PS C:\> Get-SPPeoplePickerDistributionListSearchDomain -WebApplication http://sitename
```

This example returns all domains in the People Picker distribution list search domains for users in the http://sitename web application.

### -------------EXAMPLE 2------------- 
```powershell
PS C:\> Get-SPPeoplePickerDistributionListSearchDomain -WebApplication http://sitename -DomainName "corp.contoso.com"
```

This example returns the People Picker distribution list search entry in the http://sitename web application that uses the "corp.contoso.com" domain.

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

### -DomainName
Name of the domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplication
Specifies the name, URL, or GUID of the Web application containing the People Picker search settings.

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
Prompts you for confirmation before running the cmdlet.

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
