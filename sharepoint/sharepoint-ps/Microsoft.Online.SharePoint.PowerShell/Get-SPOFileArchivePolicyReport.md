---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Get-SPOFileArchivePolicyReport

## SYNOPSIS
Gets run reports for a File Archive Policy.

## SYNTAX

```
Get-SPOFileArchivePolicyReport -PolicyId <Guid> [<CommonParameters>]
```

## DESCRIPTION
The `Get-SPOFileArchivePolicyReport` cmdlet retrieves the run reports for a File Archive Policy. Reports are kept for the past 12 months and include details about each policy run such as how many sites were processed, how many files were archived, and the total storage archived.

For policies running in WhatIf mode, reports show how many files and how much storage would have been archived instead.

You must be a SharePoint Administrator or Global Administrator to run this cmdlet.

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-SPOFileArchivePolicyReport -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890"
```

Returns all run reports for the specified File Archive Policy from the past 12 months.

## PARAMETERS

### -PolicyId
Specifies the unique identifier (GUID) of the policy to retrieve run reports for.

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
