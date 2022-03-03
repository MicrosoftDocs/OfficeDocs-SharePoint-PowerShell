---
title: PnP PowerShell Overview
description: "SharePoint PnP PowerShell Overview"
---


# PnP PowerShell overview

PnP PowerShell is a .NET Core 3.1 / .NET Framework 4.6.1 based PowerShell Module providing over 600 cmdlets that work with Microsoft 365 environments and more specifically SharePoint Online and Microsoft Teams.

For more information about installing or upgrading to this module, please refer to the documentation at https://pnp.github.io/powershell/articles/index.html

## Supportability and SLA for PnP PowerShell cmdlets

This library is open-source and community provided library with active community providing support for it. This is not Microsoft provided module so there's no SLA or direct support for this open-source component from Microsoft. Please report any issues using the [issues list in GitHub](https://github.com/pnp/powershell/issues).

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
