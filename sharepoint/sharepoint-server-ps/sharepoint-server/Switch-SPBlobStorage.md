---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/switch-spblobstorage
applicable: SharePoint Server Subscription Edition
title: Switch-SPBlobStorage
schema: 2.0.0
author:
ms.author:
ms.reviewer:
---

# Switch-SPBlobStorage

## SYNOPSIS
This cmdlet switches active BLOB storage.

## SYNTAX

### SQL
```
Switch-SPBlobStorage -ContentDatabase <SPContentDatabasePipeBind> [-SQL]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoteShareBlobStore
```
Switch-SPBlobStorage -RemoteShareBlobStore <SPRemoteShareBlobStorePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.

The \`Switch-SPBlobStorage\` cmdlet switches the BLOB of a content database between Remote Share BLOB Store and SQL tables.

## EXAMPLES

### -------------EXAMPLE 1------------- 
```powershell
PS C:\> Switch-SPBlobStorage -ContentDatabase "WSS_Content" -SQL
```

This example switches BLOB storage to SQL tables for content database "WSS_Content."

### -------------EXAMPLE 2------------- 
```powershell
PS C:\> Switch-SPBlobStorage -RemoteShareBlobStore "RemoteBlobStore"
```

This example switches BLOB storage to the Remote Share BLOB Store named "RemoteBlobStore."

## PARAMETERS

### -AssignmentCollection
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
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ContentDatabase
The content database this operation will be applied to.

```yaml
Type: SPContentDatabasePipeBind
Parameter Sets: SQL
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RemoteShareBlobStore
Specifies the Remote Share BLOB Store for new content.

It can either be the Remote Share BLOB Store object or the Remote Share BLOB Store name.

```yaml
Type: SPRemoteShareBlobStorePipeBind
Parameter Sets: RemoteShareBlobStore
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SQL
Indicates the content database will use SQL for BLOB storage for new content.

```yaml
Type: SwitchParameter
Parameter Sets: SQL
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
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
