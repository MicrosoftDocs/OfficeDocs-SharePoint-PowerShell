---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spouserandcontentmovestate
applicable: SharePoint Online
title: Get-SPOUserAndContentMoveState
schema: 2.0.0
author: trent-green
ms.author: speedta
ms.reviewer:
---

# Get-SPOUserAndContentMoveState

## SYNOPSIS

This cmdlet allows SharePoint administrators to check the status of a user or site move across geo locations.

## SYNTAX

### MoveReport (Default)
```
Get-SPOUserAndContentMoveState [-Limit <UInt32>] [-MoveStartTime <DateTime>] [-MoveEndTime <DateTime>]
 [-MoveState <MoveState>] [-MoveDirection <MoveDirection>] [<CommonParameters>]
```

### UserPrincipalName
```
Get-SPOUserAndContentMoveState -UserPrincipalName <String> [<CommonParameters>]
```

### OdbMoveId
```
Get-SPOUserAndContentMoveState -OdbMoveId <Guid> [<CommonParameters>]
```

## DESCRIPTION

This command gets the information and the status of a move request of a user between sites in a SharePoint Online Multi Geo tenant.

The following are the available move states:

|Status|Description|
| --- | --- |
|ReadyToTrigger| The move is ready to be initiated by an administrator. |
|NotStarted| The move has not started. |
|InProgress| The move is in progress in one of the following states: Validation, Backup, Restore, Cleanup.|
|Success| The move has completed successfully.|
|Failed|The move failed.|
|Stopped|The move was canceled by an administrator while it was still queued.|
|NotSupported|The move could not be processed because the Preferred Data Location was invalid.|
|Rescheduled|The move did not succeed and is being scheduled again for another attempt.|

## EXAMPLES

### Example 1

```Powershell
Get-SPOUserAndContentMoveState -OdbMoveId b298219e-3440-10b8-8931-46e805e2b85b
```

Obtain the move state by OneDrive Move Job ID

### Example 2

```Powershell
Get-SPOUserAndContentMoveState -MoveState NotStarted
```

Getting which moves are being done in a particular state
### Example 3

```Powershell
Get-SPOUserAndContentMoveState -MoveDirection All
```

Gives you the output for users moving in and out from the geo location you are logged into

### Example 4

```Powershell
Get-SPOUserAndContentMoveState -MoveDirection In
```

Gives you the output for users moving into the geo location that you are logged into

### Example 5

```Powershell
Get-SPOUserAndContentMoveState -MoveDirection Out
```

Gives you the output for users moving out from the geo location that you are logged into

### Example 6

```Powershell
Get-SPOUserAndContentMoveState -UserPrincipalName jezz@contoso.com
```

Obtains the status of the move for jezz@contoso.com

## PARAMETERS

### -Limit

> Applicable: SharePoint Online

Get the limit of user on a single call of the parameter

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

Allows you to define the direction of the user move in relation to your current SharePoint location

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

> Applicable: SharePoint Online

Allows you to obtain the moves that are scheduled to end by a particular time, as defined in UTC

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

> Applicable: SharePoint Online

Allows you to obtain the moves that are scheduled to begin at a particular time, as defined in UTC

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

> Applicable: SharePoint Online

Move State current status.

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

### -OdbMoveId

> Applicable: SharePoint Online

OneDrive GUID MoveID that you get when you start a job.

```yaml
Type: System.Guid
Parameter Sets: OdbMoveId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName

> Applicable: SharePoint Online

User Principal name is the unique property on Microsoft Entra ID for each user.

```yaml
Type: String
Parameter Sets: UserPrincipalName
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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Start-SPOUserAndContentMove](Start-SPOUserAndContentMove.md)
