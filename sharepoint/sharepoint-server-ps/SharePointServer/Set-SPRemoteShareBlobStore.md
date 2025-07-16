---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spremoteshareblobstore
applicable: SharePoint Server Subscription Edition
title: Set-SPRemoteShareBlobStore
schema: 2.0.0
---

# Set-SPRemoteShareBlobStore

## SYNOPSIS
Configures the specified Remote Share BLOB Store.

## SYNTAX

```
Set-SPRemoteShareBlobStore -RemoteShareBlobStore <SPRemoteShareBlobStorePipeBind> [-Location <String>]
 [-BlobStoreCredential <PSCredential>] [-PoolCapacity <Int32>] [-AssignmentCollection <SPAssignmentCollection>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The \`Set-SPRemoteShareBlobStore\` cmdlet changes the setting of the registed Remote Share BLOB Store.

## EXAMPLES

### -------------EXAMPLE 1------------- 
```powershell
Set-SPRemoteShareBlobStore -RemoteShareBlobStore "RemoteStore" -Location "\\storage_name\blobstore\"
```

This example sets the location of Remote Share BLOB Store "RemoteStore" to "\\\\storage_name\blobstore\"

### -------------EXAMPLE 2------------- 
```powershell
Set-SPRemoteShareBlobStore -RemoteShareBlobStore "RemoteStore" -BlobStoreCredential (Get-Credential)
```

This example prompts the user to provide BLOB store credentials for the specified Remote Share BLOB Store "RemoteStore".

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

### -BlobStoreCredential
Specifies the credentials to use to connect to the BLOB store.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Specifies the path of the SMB storage this BLOB store will use.
You must use a Universal Naming Convention (UNC) share path.
For example: \\\\storage_name\blobstore.

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

### -PoolCapacity
The number of BLOB trunks in each BLOB pool.

If this parameter is not specified, the current value will not be changed.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteShareBlobStore
Specifies the identity of the Remote Share BLOB Store to unregister.

It can either be the Remote Share BLOB Store object or the Remote Share BLOB Store name.

```yaml
Type: SPRemoteShareBlobStorePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
