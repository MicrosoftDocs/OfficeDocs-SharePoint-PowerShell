---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/en-us/powershell/module/microsoft.online.sharepoint.powershell/get-spotenantserviceprincipalpermissionrequests
applicable: SharePoint Online
title: Get-SPOTenantServicePrincipalPermissionRequests
schema: 2.0.0
author: samkabue
ms.author: speedta
ms.reviewer:
---

# Get-SPOTenantServicePrincipalPermissionRequests

## SYNOPSIS

Gets the collection of permission requests for the "SharePoint Online Client" service principal

## SYNTAX

```
Get-SPOTenantServicePrincipalPermissionRequests [<CommonParameters>]
```

## DESCRIPTION

Gets the collection of permission requests for the "SharePoint Online Client" service principal.

Permission request object

A permission request contains the following properties:

- Id: The identifier of the request.

- Resource: The resource that the application requires access to.

- Scope: The value of the scope claim that the resource application should expect in the OAuth 2.0 access token.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantServicePrincipalPermissionRequests
```

Gets the collection of permission requests for the "SharePoint Online Client" service principal.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
