---
external help file: Microsoft.SharePoint.Publishing.dll-help.xml
Module Name: SharePointServer
online version:
schema: 2.0.0
---

# Deploy-SPVariation

## SYNOPSIS
Creates new site variations on the source variation site specified by the Identity parameter for all target variations labels.

## SYNTAX

```
Deploy-SPVariation -Identity <SPWebPipeBind> [-Recurse] [-Label <String>]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The command creates new site variations on the source variation site specified by the Identity parameter for all target variations labels.
If the Recurse parameter is used, variations for subsites and pages are also created.

## EXAMPLES

### EXAMPLE
```
C:\PS> Deploy-SPVariation -Identity https://server/sites/pub/vhome/source/newsub
```

The example is to create new site variations on the source variation site specified by the Identity parameter for all target variations labels.

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
The source variation site.

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
Creates variations for subsites and pages along with the source variation site.

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
