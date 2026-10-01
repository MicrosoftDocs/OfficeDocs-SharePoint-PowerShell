---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/microsoft.online.sharepoint.powershell/start-spoinformationbarrierspolicycompliancereport
applicable: SharePoint Online
title: Start-SPOInformationBarriersPolicyComplianceReport
schema: 2.0.0
author: srmuppana
ms.author: srmuppana
manager: dbolick
ms.reviewer: nibandyo
---

# Start-SPOInformationBarriersPolicyComplianceReport

## SYNOPSIS

Generates an Information Barriers policy compliance report for SharePoint sites, OneDrive accounts, and user-owned SharePoint Embedded containers in the organization.

## SYNTAX

```
Start-SPOInformationBarriersPolicyComplianceReport [-UpdateOneDriveSegments]
 [-UpdateUserOwnedContainerSegments] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet generates an Information Barriers policy compliance report that identifies SharePoint sites, OneDrive accounts, and user-owned SharePoint Embedded containers that are noncompliant with current Information Barriers policies.

Use the optional update parameters to automatically update segments for noncompliant OneDrive accounts or user-owned SharePoint Embedded containers while the report is being generated. Report generation can take a long time, depending on the number of sites, accounts, and containers in the organization. To check the report status, run `Get-SPOInformationBarriersPolicyComplianceReport` without any parameters.

## EXAMPLES

### Example 1

```powershell
Start-SPOInformationBarriersPolicyComplianceReport
```

This example generates an Information Barriers policy compliance report without automatically updating segments.

### Example 2

```powershell
Start-SPOInformationBarriersPolicyComplianceReport -UpdateUserOwnedContainerSegments
```

This example generates the report and automatically updates segments for noncompliant user-owned SharePoint Embedded containers.

### Example 3

```powershell
Start-SPOInformationBarriersPolicyComplianceReport -UpdateOneDriveSegments -UpdateUserOwnedContainerSegments
```

This example generates the report and automatically updates segments for noncompliant OneDrive accounts and user-owned SharePoint Embedded containers.

## PARAMETERS

### -UpdateOneDriveSegments

Automatically updates segments for noncompliant OneDrive accounts during report generation.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateUserOwnedContainerSegments

Automatically updates segments for noncompliant user-owned SharePoint Embedded containers during report generation.

```yaml
Type: System.Management.Automation.SwitchParameter
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

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-ProgressAction`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### System.Object

## RELATED LINKS

[Get-SPOInformationBarriersPolicyComplianceReport](./Get-SPOInformationBarriersPolicyComplianceReport.md)

[Create an Information Barriers policy compliance report](/purview/information-barriers-sharepoint-report)
