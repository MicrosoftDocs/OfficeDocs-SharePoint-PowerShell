---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Add-SPOTenantIdentityMappingUser

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
Add-SPOTenantIdentityMappingUser [-SourceTenantCompanyId] <Guid> [-SourceUserKey] <String>
 [[-TargetUserPuid] <String>] [-TargetUserUpn] <String> [-TargetUserEmail] <String>
 [-UserType] <TenantIdentityMappingUserType> [<CommonParameters>]
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

### -SourceUserKey
{{ Fill SourceUserKey Description }}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetUserEmail
{{ Fill TargetUserEmail Description }}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetUserPuid
{{ Fill TargetUserPuid Description }}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetUserUpn
{{ Fill TargetUserUpn Description }}

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

### -UserType
{{ Fill UserType Description }}

```yaml
Type: Microsoft.SharePoint.Client.Administration.TenantIdentityMappingUserType
Parameter Sets: (All)
Aliases:
Accepted values: None, RegularUser, AdminUser, GuestUser

Required: True
Position: 5
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
