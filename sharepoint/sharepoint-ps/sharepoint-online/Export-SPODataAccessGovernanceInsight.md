---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Export-SPODataAccessGovernanceInsight

## SYNOPSIS

This commands exports/downloads the DAG report to the default path "C:\WINDOWS\system32\"

## SYNTAX

```
Export-SPODataAccessGovernanceInsight -ReportID <Guid> [<CommonParameters>]
```

## DESCRIPTION

This commands exports/downloads the DAG report, specified by the ReportID, to the default path "C:\WINDOWS\system32\". The ReportID is shown in the output of the 'Start-SPODataAccessGovernanceInsight' command. It can also be fetched from the output of the 'Get-SPODataAccessGovernanceInsight' command.

## EXAMPLES

### Example 1

```powershell
PS C:\> Export-SPODataAccessGovernanceInsight -ReportID 28f4c550-215a-472b-a123-c11e5fa8804c
```

This command downloads the report of the given ID to the default path "C:\WINDOWS\system32\"

## PARAMETERS

### -ReportID

Specifies the ID of the DAG report to be downloaded.

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

## RELATED LINKS
