---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Remove-SPOListDesign

## SYNOPSIS
Removes a list design. It no longer appears in the UI for creating a new list. 

## SYNTAX

```
Remove-SPOListDesign [-Identity] <SPOListDesignPipeBind> [<CommonParameters>]
```

## DESCRIPTION
Removes a list design. It no longer appears in the UI for creating a new list. 

## EXAMPLES

### Example 1
This example shows how to remove a list design. 

```powershell
Remove-SPOListDesign 44252d09-62c4-4913-9eb0-a2a8b8d7f863
```

{{ Add example description here }}

## PARAMETERS

### -Identity
The ID of the list design to remove. 

```yaml
Type: SPOListDesignPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SPOListDesignPipeBind

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
