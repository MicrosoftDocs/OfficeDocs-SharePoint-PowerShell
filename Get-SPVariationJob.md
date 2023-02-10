---
external help file: Microsoft.SharePoint.Publishing.dll-Help.xml
Module Name: SharePointServer
online version:
schema: 2.0.0
---

# Get-SPVariationJob

## SYNOPSIS
Displays current status of Variations Propagate Page Job Definition and Variations Propagate Site Job Definition timer jobs that are located on the Timer Job Status page of the SharePoint Central Administration Web site.

## SYNTAX

```
Get-SPVariationJob -Identity <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The command displays current status of Variations Propagate Page Job Definition and Variations Propagate Site Job Definition timer jobs that are located on the Timer Job Status page of the SharePoint Central Administration Web site.

## EXAMPLES

### EXAMPLE
```
C:\PS> Get-SPVariationJob -Identity https://server/sites/pub/vhome/source/newsub
```

The example is to display the current status of Variations Propagate Page Job Definition and Variations Propagate Site Job Definition timer jobs that are located on the Timer Job Status page of the SharePoint Central Administration Web site.

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
