---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Get-SPOCrossTenantSiteContentMoveState

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### MoveReport (Default)
```
Get-SPOCrossTenantSiteContentMoveState -PartnerCrossTenantHostUrl <String> [-Limit <UInt32>]
 [-MoveStartTime <DateTime>] [-MoveEndTime <DateTime>] [-MoveState <MoveState>]
 [-MoveDirection <MoveDirection>] [-PartnerRole <OrgRelationRole>] [<CommonParameters>]
```

### SourceSiteUrl
```
Get-SPOCrossTenantSiteContentMoveState -PartnerCrossTenantHostUrl <String> -SourceSiteUrl <String>
 [-PartnerRole <OrgRelationRole>] [<CommonParameters>]
```

### SiteMoveId
```
Get-SPOCrossTenantSiteContentMoveState -PartnerCrossTenantHostUrl <String> -SiteMoveId <Guid>
 [-PartnerRole <OrgRelationRole>] [<CommonParameters>]
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

### -Limit
{{ Fill Limit Description }}

```yaml
Type: System.UInt32
Parameter Sets: MoveReport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MoveDirection
{{ Fill MoveDirection Description }}

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.MoveDirection
Parameter Sets: MoveReport
Aliases:
Accepted values: MoveOut, MoveIn, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MoveEndTime
{{ Fill MoveEndTime Description }}

```yaml
Type: System.DateTime
Parameter Sets: MoveReport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MoveStartTime
{{ Fill MoveStartTime Description }}

```yaml
Type: System.DateTime
Parameter Sets: MoveReport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MoveState
{{ Fill MoveState Description }}

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.MoveState
Parameter Sets: MoveReport
Aliases:
Accepted values: NotStarted, InProgress, Success, Failed, Stopped, Queued, NotSupported, Rescheduled, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerCrossTenantHostUrl
{{ Fill PartnerCrossTenantHostUrl Description }}

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

### -PartnerRole
{{ Fill PartnerRole Description }}

```yaml
Type: Microsoft.SharePoint.Client.Administration.OrgRelationRole
Parameter Sets: (All)
Aliases:
Accepted values: None, Source, Target

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteMoveId
{{ Fill SiteMoveId Description }}

```yaml
Type: System.Guid
Parameter Sets: SiteMoveId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceSiteUrl
{{ Fill SourceSiteUrl Description }}

```yaml
Type: System.String
Parameter Sets: SourceSiteUrl
Aliases:

Required: True
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
