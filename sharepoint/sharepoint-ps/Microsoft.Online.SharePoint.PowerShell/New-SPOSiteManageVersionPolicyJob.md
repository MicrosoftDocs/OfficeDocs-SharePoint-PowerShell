---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# New-SPOSiteManageVersionPolicyJob

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### MandatoryTrimOptionalSync
```
New-SPOSiteManageVersionPolicyJob [-Identity] <SpoSitePipeBind> [-FileTypes <String[]>] [-ExcludeDefaultPolicy]
 [-TrimUseListPolicy] [-SyncListPolicy] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MandatorySync
```
New-SPOSiteManageVersionPolicyJob [-Identity] <SpoSitePipeBind> [-FileTypes <String[]>] [-ExcludeDefaultPolicy]
 [-SyncListPolicy] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

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

### -ExcludeDefaultPolicy
{{ Fill ExcludeDefaultPolicy Description }}

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

### -FileTypes
{{ Fill FileTypes Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
{{ Fill Identity Description }}

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SyncListPolicy
{{ Fill SyncListPolicy Description }}

```yaml
Type: SwitchParameter
Parameter Sets: MandatoryTrimOptionalSync
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: MandatorySync
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrimUseListPolicy
{{ Fill TrimUseListPolicy Description }}

```yaml
Type: SwitchParameter
Parameter Sets: MandatoryTrimOptionalSync
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

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
