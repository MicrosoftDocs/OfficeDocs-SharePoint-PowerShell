---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/test-defenderandamsiworkproperly
applicable: SharePoint Server Subscription Edition
title: Test-DefenderAndAmsiWorkProperly
schema: 2.0.0
---

# Test-DefenderAndAmsiWorkProperly

## SYNOPSIS

Tests that Windows Defender components and SharePoint AMSI integration are properly installed and running.

## SYNTAX

```powershell
Test-DefenderAndAmsiWorkProperly [<CommonParameters>]
```

## DESCRIPTION

Use the `Test-DefenderAndAmsiWorkProperly` cmdlet to verify that all Windows Defender components are installed and running correctly, and that SharePoint AMSI (Antimalware Scan Interface) integration is functioning properly.

This cmdlet performs comprehensive checks to ensure that the security infrastructure is operational and can protect SharePoint Server from malicious content. It validates both the Windows Defender antimalware engine and the AMSI integration that allows SharePoint to scan content for potential threats.

The cmdlet does not make any changes to the system configuration but provides diagnostic information about the current state of security components.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1

```powershell
Test-DefenderAndAmsiWorkProperly
```

This example tests the Windows Defender components and SharePoint AMSI integration to verify they are properly installed and running.

### EXAMPLE 2

```powershell
Test-DefenderAndAmsiWorkProperly -Verbose
```

This example tests the Windows Defender components and SharePoint AMSI integration with verbose output to provide detailed information about each component being checked.

## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

This cmdlet does not accept any input objects.

## OUTPUTS

### System.Object

This cmdlet returns diagnostic information about the status of Windows Defender components and SharePoint AMSI integration.

## NOTES

- This cmdlet requires administrator privileges to access security component information.
- Ensure that Windows Defender is properly configured and enabled before running this test.
- SharePoint AMSI integration requires Windows Server 2016 or later with appropriate updates installed.

## RELATED LINKS

[SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets)

[Windows Defender Antivirus](https://learn.microsoft.com/defender-endpoint/microsoft-defender-antivirus-windows)

[Antimalware Scan Interface (AMSI)](https://learn.microsoft.com/windows/win32/amsi/antimalware-scan-interface-portal)