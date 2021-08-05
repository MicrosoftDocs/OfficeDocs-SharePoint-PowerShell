---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/remove-spcertificate
applicable: SharePoint Server Subscription Edition
title: Remove-SPCertificate
schema: 2.0.0
author:
ms.author:
ms.reviewer:
---

# Remove-SPCertificate

## SYNOPSIS
Deletes a certificate and any associated private key.

## SYNTAX

```
Remove-SPCertificate [-Identity] <SPServerCertificatePipeBind> [-Force]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Deletes a certificate and any associated private key.

The following will happen when you delete a certificate from SharePoint:

By default, SharePoint won't allow you to delete a certificate if it's currently assigned to a SharePoint object.
You must override the default behavior with the Force parameter if you want to force the deletion of a certificate.
If you override the default behavior, existing assignments of the certificate are cleared.

The certificate and any private key associated with that certificate is deleted from the Windows certificate store on every server in the SharePoint farm.

The certificate and any private key associated with it is deleted from the SharePoint configuration database.

Any previous exports of the certificate through the SharePoint administration interface won't be deleted.
Those exported files will still exist.

## EXAMPLES

### ------------EXAMPLE-----------
```powershell
Remove-SPCertificate -Identity "Team Sites Certificate"
```

This example deletes the "Team Sites Certificate" certificate and any private key associated with that certificate.

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

### -Force
Specifies that the certificate should be deleted from SharePoint, even if the certificate is currently assigned to SharePoint objects.
If this parameter is specified, any existing assignments of the certificate are also cleared.
If this parameter isn't specified and the certificate is assigned to a SharePoint object, the operation will fail.

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

### -Identity
The certificate to delete from SharePoint.

```yaml
Type: SPServerCertificatePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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
