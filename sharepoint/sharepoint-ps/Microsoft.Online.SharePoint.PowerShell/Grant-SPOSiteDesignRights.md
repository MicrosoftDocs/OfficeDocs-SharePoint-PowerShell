---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/grant-spositedesignrights
applicable: SharePoint Online
title: Grant-SPOSiteDesignRights
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Grant-SPOSiteDesignRights

## SYNOPSIS

Used to apply permissions to a set of users or a security group, effectively scoping the visibility of the site design in the UX. They start off public, but after you set permissions, only those groups or users with permissions can access the site design.

## SYNTAX

```
Grant-SPOSiteDesignRights [-Identity] <SPOSiteDesignPipeBind> -Principals <String[]>
 -Rights <SPOSiteDesignPrincipalRights> [<CommonParameters>]
```

## DESCRIPTION

Used to apply permissions to a set of users or a security group, effectively scoping the visibility of the site design in the UX. They start off public, but after you set permissions, only those groups or users with permissions can access the site design.

## EXAMPLES

### Example 1

This example shows how to grant view rights on a site design to Nestor (a user at the fictional Contoso site).

```powershell
Grant-SPOSiteDesignRights `
         -Identity 44252d09-62c4-4913-9eb0-a2a8b8d7f863 `
         -Principals "nestorw@contoso.onmicrosoft.com" `
         -Rights View
```

## PARAMETERS

### -Identity

The ID of the site design to get scoping information.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Principals

One or more principles to add permissions for.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rights

Always set to the value **View**. Any user or group with view permissions can view and use the site design.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPrincipalRights
Parameter Sets: (All)
Aliases:
Accepted values: View
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
