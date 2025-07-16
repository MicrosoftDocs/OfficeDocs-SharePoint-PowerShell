---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/register-spremoteshareblobstore
applicable: SharePoint Server Subscription Edition
title: Register-SPRemoteShareBlobStore
schema: 2.0.0
---

# Register-SPRemoteShareBlobStore

## SYNOPSIS
This cmdlet registers a new Remote Share BLOB Store to a given content database.

## SYNTAX

```
Register-SPRemoteShareBlobStore -ContentDatabase <SPContentDatabasePipeBind> -Name <String> -Location <String>
 [-BlobStoreCredential <PSCredential>] [-PoolCapacity <Int32>] [-AssignmentCollection <SPAssignmentCollection>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The \`Register-SPRemoteShareBlobStore\` cmdlet registers a new BLOB store for the specified content database, which offloads BLOB storage in this content database to SMB storage.

## EXAMPLES

### -------------EXAMPLE 1------------- 
```powershell
Register-SPRemoteShareBlobStore -ContentDatabase WSS_Content -Name "RemoteBlob" -Location "\\storage_name\blobstore\"
```

This example registers \\\\storage_name\blobstore\ with name "RemoteBlob" to content database WSS_Content

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

### -ContentDatabase
Specifies a content database to register the Remote Share BLOB Store.

```yaml
Type: SPContentDatabasePipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the new BLOB store.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolCapacity
The number of BLOB chunks in each BLOB pool.

If this parameter is not specified, it will be set to 1000.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: 1000
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
