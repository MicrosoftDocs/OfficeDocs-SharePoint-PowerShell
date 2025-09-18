---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.sharepoint.powershell/get-spremoteshareblobstore
applicable: SharePoint Server Subscription Edition
title: Get-SPRemoteShareBlobStore
schema: 2.0.0
---

# Get-SPRemoteShareBlobStore

## SYNOPSIS
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.

Returns all Remote Share BLOB Stores that match the given criteria.

## SYNTAX

### DefaultSet
```
Get-SPRemoteShareBlobStore [-RemoteShareBlobStore <SPRemoteShareBlobStorePipeBind>]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ContentDatabase
```
Get-SPRemoteShareBlobStore -ContentDatabase <SPContentDatabasePipeBind> [-Name <String>]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The \`Get-SPRemoteShareBlobStore\` cmdlet returns all Remote Share BLOB Stores that match the given criteria.
This cmdlet can help you to get a specific BLOB store, or all the BLOB stores for a given content database, or all the BLOB stores in the SharePoint farm.

## EXAMPLES

### EXAMPLE 1
```powershell
Get-SPRemoteShareBlobStore
```

Gets all the Remote Share BLOB Stores in the SharePoint farm.

### EXAMPLE 2
```powershell
Get-SPRemoteShareBlobStore -RemoteShareBlobStore "RemoteBlobStore"
```

Gets the Remote Share BLOB Store named "RemoteBlobStore."

### EXAMPLE 3
```powershell
Get-SPRemoteShareBlobStore -ContentDatabase "WSS_Content"
```

Gets all the Remote Share BLOB Stores registered in content database "WSS_Content."

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.
NOTE: When the Global parameter is used, all objects are contained in the global store.
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

### -ContentDatabase

> Applicable: SharePoint Server Subscription Edition

Specifies a content database to get the Remote Share BLOB Store.

```yaml
Type: SPContentDatabasePipeBind
Parameter Sets: ContentDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies a Remote Share BLOB store name to get the Remote Share BLOB Store.

```yaml
Type: String
Parameter Sets: ContentDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RemoteShareBlobStore

> Applicable: SharePoint Server Subscription Edition

Specifies the identity of the Remote Share BLOB Store.

It can either be the Remote Share BLOB Store object or the Remote Share BLOB Store name.

```yaml
Type: SPRemoteShareBlobStorePipeBind
Parameter Sets: DefaultSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
