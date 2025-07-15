---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# New-SPOPortalLaunchWaves

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
New-SPOPortalLaunchWaves -LaunchSiteUrl <String> -RedirectionType <PortalLaunchRedirectionType>
 -ExpectedNumberOfUsers <PortalLaunchUsersSizeType> [-RedirectUrl <String>] [-WaveSetupJsonFilepath <String>]
 [-Waves <String>] -WaveOverrideUsers <String> [-WhatIf] [-Confirm] [<CommonParameters>]
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

### -ExpectedNumberOfUsers
{{ Fill ExpectedNumberOfUsers Description }}

```yaml
Type: Microsoft.SharePoint.Client.Publishing.PortalLaunch.PortalLaunchUsersSizeType
Parameter Sets: (All)
Aliases:
Accepted values: LessThan10kUsers, From10kTo30kUsers, From30kTo100KUsers, MoreThan100kUsers

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LaunchSiteUrl
{{ Fill LaunchSiteUrl Description }}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectionType
{{ Fill RedirectionType Description }}

```yaml
Type: Microsoft.SharePoint.Client.Publishing.PortalLaunch.PortalLaunchRedirectionType
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, ToTemporaryPage, SiteBased

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectUrl
{{ Fill RedirectUrl Description }}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaveOverrideUsers
{{ Fill WaveOverrideUsers Description }}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Waves
{{ Fill Waves Description }}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaveSetupJsonFilepath
{{ Fill WaveSetupJsonFilepath Description }}

```yaml
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
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
