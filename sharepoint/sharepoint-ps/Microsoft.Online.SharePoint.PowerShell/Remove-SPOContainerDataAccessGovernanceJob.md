---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/remove-spocontainerdataaccessgovernancejob
applicable: SharePoint Online
title: Remove-SPOContainerDataAccessGovernanceJob
schema: 2.0.0
---

# Remove-SPOContainerDataAccessGovernanceJob

## SYNOPSIS

Deletes a SharePoint Embedded Data Access Governance report.

## SYNTAX

```
Remove-SPOContainerDataAccessGovernanceJob -ReportID <Guid> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The `Remove-SPOContainerDataAccessGovernanceJob` cmdlet deletes the report identified by `ReportID`. It doesn't delete the SharePoint Embedded containers described by the report.

The cmdlet retrieves the report metadata and verifies that the report belongs to SharePoint Embedded before requesting confirmation or deletion. SharePoint and OneDrive report IDs aren't accepted.

Use `WhatIf` to preview the deletion. The cmdlet still retrieves and validates the report, but doesn't send a deletion request.

Connect to the tenant administration endpoint with `Connect-SPOService` before running this cmdlet. The service must support SharePoint Embedded Data Access Governance reports, and the signed-in account must be authorized to delete them.

## EXAMPLES

### Example 1

```powershell
Remove-SPOContainerDataAccessGovernanceJob -ReportID 28f4c550-215a-472b-a123-c11e5fa8804c -WhatIf
```

This example previews removal without deleting the report. Replace the example ID with an ID returned by `Start-SPOContainerDataAccessGovernanceJob` or `Get-SPOContainerDataAccessGovernanceJob`.

### Example 2

```powershell
Remove-SPOContainerDataAccessGovernanceJob -ReportID 28f4c550-215a-472b-a123-c11e5fa8804c -Confirm
```

This example prompts for confirmation before deleting the report.

## PARAMETERS

### -ReportID

Specifies the ID of the SharePoint Embedded report to delete.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts for confirmation before deleting the report.

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

Shows the proposed deletion without deleting the report. Report metadata is still retrieved and validated.

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

### None

## NOTES

## RELATED LINKS

[Connect-SPOService](./Connect-SPOService.md)

[Start-SPOContainerDataAccessGovernanceJob](./Start-SPOContainerDataAccessGovernanceJob.md)

[Get-SPOContainerDataAccessGovernanceJob](./Get-SPOContainerDataAccessGovernanceJob.md)

[Export-SPOContainerDataAccessGovernanceJob](./Export-SPOContainerDataAccessGovernanceJob.md)
