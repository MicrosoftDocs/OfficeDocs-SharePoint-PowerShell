---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/start-sporestrictedaccessforsitesinsights
applicable: SharePoint Online
title: Start-SPORestrictedAccessForSitesInsights
schema: 2.0.0
author: ishwarit
ms.author: itambakhe
ms.reviewer:
manager:
---
 
# Start-SPORestrictedAccessForSitesInsights

## SYNOPSIS

This cmdlet enables administrator to trigger the build of a new restricted access control insights report for the data from last 28 days.

## SYNTAX

```powershell
Start-SPORestrictedAccessForSitesInsights -RACProtectedSites [-Force <SwitchParameter>] 
```

```powershell
Start-SPORestrictedAccessForSitesInsights -ActionsBlockedByPolicy [-Force <SwitchParameter>] 
```

## DESCRIPTION

After this cmdlet is executed, the restricted access control insights report generation request is initiated for the requested report subtype.                               |

## EXAMPLES

### -----------------------EXAMPLE 1-----------------------------

```powershell
Start-SPORestrictedAccessForSitesInsights -RACProtectedSites
```

Example 1 generates the restricted access control report which contains insights about the list of sites protected with the policy.

### -----------------------EXAMPLE 2-----------------------------

```powershell
Start-SPORestrictedAccessForSitesInsights -ActionsBlockedByPolicy
```

Example 2 generates the restricted access control report which contains insights about access denials by the policy.

## PARAMETERS

### -RACProtectedSites

It is an optional parameter, and it specifies the type of report generation to be triggered.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActionsBlockedByPolicy

It is an optional parameter, and it specifies the type of report generation to be triggered.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

It is an optional parameter which is used to bypass confirmation prompts and execute the command without interruptions.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Online
 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Related Links

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPORestrictedAccessForSitesInsights](./Get-SPORestrictedAccessForSitesInsights.md)
