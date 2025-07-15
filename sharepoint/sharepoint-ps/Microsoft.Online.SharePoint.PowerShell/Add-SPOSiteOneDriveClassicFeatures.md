---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Add-SPOSiteOneDriveClassicFeatures

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SingleUserLoginParamSet (Default)
```
Add-SPOSiteOneDriveClassicFeatures [-UserLogin] <String> [-Scope] <FeatureScope> [-FeatureIds] <Guid[]>
 [<CommonParameters>]
```

### UserLoginFilePathParamSet
```
Add-SPOSiteOneDriveClassicFeatures [-UserLoginFilePath] <String> [-Scope] <FeatureScope> [-FeatureIds] <Guid[]>
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

### -FeatureIds
{{ Fill FeatureIds Description }}

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
{{ Fill Scope Description }}

```yaml
Type: Microsoft.SharePoint.Client.Administration.FeatureScope
Parameter Sets: (All)
Aliases:
Accepted values: Site, Web

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserLogin
{{ Fill UserLogin Description }}

```yaml
Type: System.String
Parameter Sets: SingleUserLoginParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserLoginFilePath
{{ Fill UserLoginFilePath Description }}

```yaml
Type: System.String
Parameter Sets: UserLoginFilePathParamSet
Aliases:

Required: True
Position: 1
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
