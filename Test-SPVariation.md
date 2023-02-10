---
external help file: Microsoft.SharePoint.Publishing.dll-Help.xml
Module Name: SharePointServer
online version:
schema: 2.0.0
---

# Test-SPVariation

## SYNOPSIS
Analyzes the variations hierarchy and reports identified problems.

## SYNTAX

```
Test-SPVariation -Identity <SPWebPipeBind> [-Recurse] [-Label <String>]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The command analyzes the variations hierarchy and reports identified problems.

## EXAMPLES

### EXAMPLE
```
C:\PS> Test-SPVariation -Identity https://server/sites/pub/vhome/source/newsub
```

The example is to analyze the variations hierarchy and report identified problems.

## PARAMETERS

### -AssignmentCollection
{{ Fill AssignmentCollection Description }}

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

### -Identity
The site in source variation where variations system data is being analyzed.

```yaml
Type: SPWebPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Label
Name of the label of the variation target.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recurse
Scans all subsites of the site specified by the Identity parameter.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
