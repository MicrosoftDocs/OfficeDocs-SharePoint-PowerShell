---
title: PnP PowerShell Overview
ms.service: sharepoint-powershell
description: "SharePoint PnP PowerShell Overview"
---


# PnP PowerShell overview

SharePoint Patterns and Practices (PnP) contains a library of PowerShell commands (PnP PowerShell) that allows you to perform complex provisioning and artifact management actions towards SharePoint. The commands use CSOM and can work against both SharePoint Online as SharePoint On-Premises.

![SharePoint Patterns and Practices](https://devofficecdn.azureedge.net/media/Default/PnP/sppnp.png)

_**Applies to:** SharePoint Online_

## Installation #

```powershell
Install-Module -Name PnP.PowerShell
```

## Updating ##

```powershell
Update-Module -Name PnP.PowerShell
``` 

This will automatically load the updated module after a new launch of PowerShell.

You can check the installed PnP-PowerShell version with the following command:

```powershell
Get-Module PnP.PowerShell -ListAvailable | Select-Object Name,Version | Sort-Object Version -Descending
```

## Getting Started #

To use the library you first need to connect to your tenant:

```powershell
Connect-PnPOnline –Url https://yoursite.sharepoint.com –Credentials (Get-Credential)
```

Notice: if you use multi-factor authentication on your tenant, use 

```powershell
Connect-PnPOnline -Url https://yoursite.sharepoint.com -UseWebLogin
```

To view all cmdlets, enter

```powershell
Get-Command -Module PnP.PowerShell
```

### Set and configure credentials ##
See this [page](https://pnp.github.io/powershell/) for more information on how to use PnP PowerShell and to set up various things like the use of a credential manager.



## Additional resources
<a name="bk_addresources"> </a>

-  [Microsoft 365 PnP PowerShell on GitHub](https://github.com/pnp/PnP-PowerShell)
-  [Microsoft 365 PnP PowerShell open source documentation](https://pnp.github.io/powershell)
