---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/add-spcertificatenotificationcontact
applicable: SharePoint Server Subscription Edition
title: Add-SPCertificateNotificationContact
schema: 2.0.0
---

# Add-SPCertificateNotificationContact

## SYNOPSIS
Adds an email address to the list of contacts to be notified when certificates are about to expire or have already expired.

## SYNTAX

```
Add-SPCertificateNotificationContact [-EmailAddress] <String> [-AssignmentCollection <SPAssignmentCollection>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The \`Add-SPCertificateNotificationContact\` cmdlet adds an email address to the list of contacts to be notified when certificates are about to expire or have already expired.

## EXAMPLES

### ------------EXAMPLE-----------
```powershell
Add-SPCertificateNotificationContact -EmailAddress sharepoint-admins@example.com
```

This example adds the sharepoint-admins@example.com email address to the list of contacts to be notified when certificates are about to expire or have already expired.

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

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -EmailAddress
An email address to notify when certificates are about to expire or have already expired.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
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
