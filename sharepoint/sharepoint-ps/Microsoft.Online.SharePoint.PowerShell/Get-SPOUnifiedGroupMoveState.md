---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spounifiedgroupmovestate
applicable: SharePoint Online
title: Get-SPOUnifiedGroupMoveState
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Get-SPOUnifiedGroupMoveState

## SYNOPSIS

Returns the state of an Office 365 Group move between Preferred Data Locations.

## SYNTAX

```
Get-SPOUnifiedGroupMoveState [-GroupAlias] <String> [<CommonParameters>]
```

## DESCRIPTION

Retrieves the state of the Office 365 Group move to the Preferred Data Location (PDL) for the specified. The customer tenant must be multi-geo enabled.

## EXAMPLES

### Example 1

```powershell
Get-SPOUnifiedGroupMoveState -GroupAlias EUTeam
```

Returns the status of the move between geos for the Office 365 Group named 'EUTeam'.

## PARAMETERS

### -GroupAlias

> Applicable: SharePoint Online

The alias of the Office 365 Group.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

The move status for the Office 365 Group. Possible values are:

* Ready to Trigger: The move has not started.
* Scheduled: The move is in queue but has not yet started.
* InProgress (n/4): The move is in progress in one of the following states: Validation (1/4), Backup (2/4), Restore (3/4), Cleanup (4/4).
* Success: The move has completed successfully.
* Failed: The move failed.
* Stopped: The move was canceled by an administrator while it was still queued.
* NotSupported: The move could not be processed because the Preferred Data Location was invalid.
* Rescheduled: The move did not succeed and is being scheduled again for another attempt.

## NOTES

You can also apply the `-Verbose` option to see additional information about the move.

## RELATED LINKS

[Move a SharePoint site to a different geo location](/microsoft-365/enterprise/m365-dr-workload-spo)
