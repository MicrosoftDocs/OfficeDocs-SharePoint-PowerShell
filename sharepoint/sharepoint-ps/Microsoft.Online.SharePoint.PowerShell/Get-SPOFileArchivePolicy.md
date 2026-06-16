---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Get-SPOFileArchivePolicy

## SYNOPSIS
Gets one or all File Archive Policies for the tenant.

## SYNTAX

```
Get-SPOFileArchivePolicy [-PolicyId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The `Get-SPOFileArchivePolicy` cmdlet retrieves the properties of File Archive Policies for the connected SharePoint Online tenant. If the `-PolicyId` parameter is specified, returns only the matching policy. If omitted, returns all File Archive Policies under the tenant.

You must be a SharePoint Administrator or Global Administrator to run this cmdlet.

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-SPOFileArchivePolicy
```

Returns all File Archive Policies configured for the tenant.

### Example 2
```powershell
PS C:\> Get-SPOFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890"
```

Returns the File Archive Policy with the specified ID.

## PARAMETERS

### -PolicyId
Specifies the unique identifier (GUID) of the policy to retrieve. If not specified, all policies under the tenant are returned.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

This cmdlet is part of the File Archive Policies feature which is currently in preview.

## RELATED LINKS
