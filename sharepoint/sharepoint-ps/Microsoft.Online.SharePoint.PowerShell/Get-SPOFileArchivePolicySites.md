---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Get-SPOFileArchivePolicySites

## SYNOPSIS
Gets the list of sites associated with a File Archive Policy.

## SYNTAX

```
Get-SPOFileArchivePolicySites -PolicyId <Guid> [<CommonParameters>]
```

## DESCRIPTION
The `Get-SPOFileArchivePolicySites` cmdlet retrieves the list of sites that have been added to a File Archive Policy. This is applicable to policies with a PolicyType of "SelectedSites".

You must be a SharePoint Administrator or Global Administrator to run this cmdlet.

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-SPOFileArchivePolicySites -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890"
```

Returns all sites associated with the specified File Archive Policy.

## PARAMETERS

### -PolicyId
Specifies the unique identifier (GUID) of the policy to retrieve the site list for.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
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
