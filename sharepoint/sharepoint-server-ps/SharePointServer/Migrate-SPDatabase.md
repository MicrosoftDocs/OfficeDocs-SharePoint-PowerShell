---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/migrate-spdatabase
title: Migrate-SPDatabase
schema: 2.0.0
---

# Migrate-SPDatabase

## SYNOPSIS
Do not use.

## SYNTAX

### SiteSubscription
```
Migrate-SPDatabase [-Identity] <SPDatabasePipeBind> [-DestinationDatabase] <SPContentDatabasePipeBind>
 [-SiteSubscription] <SPSiteSubscriptionPipeBind> [-ServiceType] <ServiceExtensionType> [-Overwrite]
 [-UseLinkedSqlServer] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### SiteCollection
```
Migrate-SPDatabase [-Identity] <SPDatabasePipeBind> [-SiteCollection] <SPSitePipeBind>
 [-ServiceType] <ServiceExtensionType> [-Overwrite] [-UseLinkedSqlServer]
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Do not use.

## EXAMPLES

### Example 1
```powershell
#Do not use.
```

Do not use.

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationDatabase

> Applicable: SharePoint Server Subscription Edition

Do not use.

```yaml
Type: SPContentDatabasePipeBind
Parameter Sets: SiteSubscription
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Server Subscription Edition

Do not use.

```yaml
Type: SPDatabasePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Overwrite

> Applicable: SharePoint Server Subscription Edition

Do not use.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType

> Applicable: SharePoint Server Subscription Edition

Do not use.

```yaml
Type: ServiceExtensionType
Parameter Sets: (All)
Aliases:
Accepted values: DefaultDatabase, Project, UserProfile, SiteSubscription, BDC, Securityobjects, Taxonomy, AppManagement, All

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCollection

> Applicable: SharePoint Server Subscription Edition

Do not use.

```yaml
Type: SPSitePipeBind
Parameter Sets: SiteCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSubscription

> Applicable: SharePoint Server Subscription Edition

Do not use.

```yaml
Type: SPSiteSubscriptionPipeBind
Parameter Sets: SiteSubscription
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseLinkedSqlServer

> Applicable: SharePoint Server Subscription Edition

Do not use.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server Subscription Edition

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.SharePoint.PowerShell.SPDatabasePipeBind
Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
