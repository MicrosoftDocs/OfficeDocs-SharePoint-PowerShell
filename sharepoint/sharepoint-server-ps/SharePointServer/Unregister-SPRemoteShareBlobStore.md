---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/microsoft.sharepoint.powershell/unregister-spremoteshareblobstore
applicable: SharePoint Server Subscription Edition
title: Unregister-SPRemoteShareBlobStore
schema: 2.0.0
---

# Unregister-SPRemoteShareBlobStore

## SYNOPSIS
This cmdlet unregisters a Remote Share BLOB Store.

## SYNTAX

```
Unregister-SPRemoteShareBlobStore -RemoteShareBlobStore <SPRemoteShareBlobStorePipeBind> [-Force]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The \`Unregister-SPRemoteShareBlobStore\` cmdlet unregisters a Remote Share BLOB Store from your content database.

## EXAMPLES

### EXAMPLE 1
```powershell
Register-SPRemoteShareBlobStore -RemoteShareBlobStore "RemoteBlobStore" -Force
```

This example forcely unregisters "RemoteBlobStore" from the farm

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

### -Force

> Applicable: SharePoint Server Subscription Edition

This switch forces unregistration even if there are BLOBs still in use in the Remote Share BLOB Store.
If there are BLOBs still in use in the BLOB store being unregistered, this cmdlet will throw an exception to prevent unintentionally unregistering a BLOB store in use.

If there is a need to unregister such a BLOB store, you can run the cmdlet with this switch to ignore the detection of in use BLOBs in the BLOB store.

It's not recommended to use this "-Force" switch because it will leave BLOBs in the SMB storage behind and make your SharePoint contents inaccessible.
It's recommended to first migrate BLOBs and then unregister the Remote Share BLOB Store.

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

### -RemoteShareBlobStore

> Applicable: SharePoint Server Subscription Edition

Specifies the identity of the Remote Share BLOB Store to unregister.

It can either be the Remote Share BLOB Store object or the Remote Share BLOB Store name.

```yaml
Type: SPRemoteShareBlobStorePipeBind
Parameter Sets: (All)
Aliases:

Required: True
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
