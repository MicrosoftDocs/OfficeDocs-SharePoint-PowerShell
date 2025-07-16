---
external help file: microsoft.office.project.server.stsadmcommandhandler.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/reset-spprojectqueuesettings

title: Reset-SPProjectQueueSettings
schema: 2.0.0
---

# Reset-SPProjectQueueSettings

## SYNOPSIS
Resets all Project Server Queue settings to their default values for a specific Project Server Service Application.

## SYNTAX

```
Reset-SPProjectQueueSettings [-ServiceApplication <PsiServiceApplicationPipeBind>]
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
Resets all Project Server Queue settings to their default values for a specific Project Server Service Application.

For permissions and the most current information about Windows PowerShell for Project Server, see the online documentation at https://go.microsoft.com/fwlink/p/?LinkId=251833 (https://go.microsoft.com/fwlink/p/?LinkId=251833).

## EXAMPLES

### EXAMPLE
```powershell
$sa = Get-SPServiceApplication | ?{$_.TypeName -eq 'Project Application Services'}
Reset-SPProjectQueueSettings -ServiceApplication $sa
```

This example resets the queue settings for a Project Server Service Application service application.

## PARAMETERS

### -ServiceApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the Project Server service application to target.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name for a Project Server service application (for example, ProjectServiceApp1); or an instance of a valid PsiServiceApplication object.

```yaml
Type: PsiServiceApplicationPipeBind
Parameter Sets: (All)
Aliases: sa

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

{{Fill AssignmentCollection Description}}

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-SPProjectQueueSettings](Set-SPProjectQueueSettings.md)

[Get-SPProjectQueueSettings](Get-SPProjectQueueSettings.md)
