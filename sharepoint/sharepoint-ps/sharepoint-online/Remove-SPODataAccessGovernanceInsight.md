---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Remove-SPODataAccessGovernanceInsight

## SYNOPSIS

This command deletes the given DAG report

## SYNTAX

```
Remove-SPODataAccessGovernanceInsight -ReportID <Guid> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This command deletes the DAG report, specified by the given ReportID. The ReportID is shown in the output of the 'Start-SPODataAccessGovernanceInsight' command. It can also be fetched from the output of the 'Get-SPODataAccessGovernanceInsight' command.

## EXAMPLES

### Example 1

```powershell
PS C:\> Remove-SPODataAccessGovernanceInsight -ReportID 28f4c550-215a-472b-a123-c11e5fa8804c
```

This command deletes the report of the given ID "28f4c550-215a-472b-a123-c11e5fa8804c"

## PARAMETERS

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

### -ReportID

Specifies the ID of the DAG report to be removed/deleted.

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

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
