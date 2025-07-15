---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Add-SPOTenantIdentityMappingGroup

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
Add-SPOTenantIdentityMappingGroup [-SourceTenantCompanyId] <Guid> [-SourceGroupObjectId] <Guid>
 [-TargetGroupObjectId] <Guid> [-TargetGroupName] <String> [-GroupType] <TenantIdentityMappingGroupType>
 [<CommonParameters>]
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

### -GroupType
{{ Fill GroupType Description }}

```yaml
Type: Microsoft.SharePoint.Client.Administration.TenantIdentityMappingGroupType
Parameter Sets: (All)
Aliases:
Accepted values: None, RegularGroup, AdminGroup, O365Group

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceGroupObjectId
{{ Fill SourceGroupObjectId Description }}

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceTenantCompanyId
{{ Fill SourceTenantCompanyId Description }}

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetGroupName
{{ Fill TargetGroupName Description }}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetGroupObjectId
{{ Fill TargetGroupObjectId Description }}

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
