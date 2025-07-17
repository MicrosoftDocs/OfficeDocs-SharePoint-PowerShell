---
description: Learn about the Microsoft.SharePoint.Powershell module, which contains cmdlets for managing SharePoint Server.
title: Overview of the Microsoft.SharePoint.Powershell module
ms.service: sharepoint-powershell
---

# Overview of the Microsoft.SharePoint.Powershell module

For a listing of the SharePoint Server cmdlets, see [Microsoft.SharePoint.Powershell cmdlets][04].

## Accessing PowerShell for SharePoint Server

After you install SharePoint Server, applicable PowerShell cmdlets are available in the SharePoint
2016 Management Shell. You can manage most aspects of SharePoint Server in the SharePoint Management
Shell. You can create new site collections, web applications, user accounts, service applications,
proxies, and more. Commands that you type in the SharePoint Management Shell return SharePoint
objects that are based on the Microsoft .NET Framework. You can apply these objects as input to
subsequent commands or store the objects in local variables for later use.

With the SharePoint Management Shell, you don't have to register the snap-in that contains the
cmdlets. Registration is handled by the `Add-PSSnapin Microsoft.SharePoint.PowerShell` line in the
`SharePoint.ps1` file. This file is located in
`%CommonProgramFiles%\Microsoft Shared\Web Server Extensions\<version>\Config\PowerShell\Registration` folder.

- `<version>` 15 equals SharePoint Server 2013
- and `<version>` 16 equals SharePoint Server 2016

To use the PowerShell console, you must register this snap-in manually.

Whether you use the SharePoint Management Shell or the PowerShell console, you can also load
additional snap-ins and modules.

> [!NOTE]
> The SharePoint Management Shell and the PowerShell console also differ in the use of the
> **ReuseThread** option, which defines how the threading model is used. The SharePoint Management
> Shell's use is defined by this line, `{Host.Runspace.ThreadOptions = "ReuseThread"}`, which is in
> the `SharePoint.ps1` file. For more information, see
> [PS Thread Options][01].

## Permissions

Before you can use the `Add-SPShellAdmin` cmdlet to grant permissions for users to run SharePoint
Server cmdlets, verify that you meet all of the following minimum requirements:

- You must have membership in the **SecurityAdmin** fixed server role on the SQL Server instance.
- You must be a member of the Administrators group on the server on which you are running the
  PowerShell cmdlet.

> [!NOTE]
> If these permissions aren't satisfied, contact your Setup administrator or SQL Server
> administrator to request these permissions.

For additional information about PowerShell permissions, see [Add-SPShellAdmin][05].

If you don't have membership in the **SharePoint_Shell_Access** role or **WSS_Admin_WPG** local
group, use the `Add-SPShellAdmin` cmdlet to add the **WSS_Admin_WPG** group in all front-end web
servers in the SharePoint farm and the **SharePoint_Shell_Access** role. If the SQL Server database
doesn't have a **SharePoint_Shell_Access** role, the role is automatically created when you run the
`Add-SPShellAdmin` cmdlet. After you run the `Add-SPShellAdmin` cmdlet, users can run SharePoint
PowerShell cmdlets in a multiple-server farm environment.

> [!NOTE]
> When you install SharePoint Server, the user account from which you run the installation is
> granted the appropriate permissions to run PowerShell cmdlets. If any users haven't been added to
> run a PowerShell cmdlet, you can use the `Add-SPShellAdmin` cmdlet to add them.

To see a list of all **SPShellAdmin** cmdlets, from a PowerShell command prompt, type
`Get-Command -Noun SPShellAdmin`.

## Scripts and execution policies

Although you can use Microsoft PowerShell to perform a single administrative task, you can also use
a script to automate a series of tasks. A script is a text file that contains one or more Microsoft
PowerShell commands. Microsoft PowerShell scripts have a `.ps1` file name extension.

To run scripts, the minimum required execution policy for SharePoint Server is **RemoteSigned**,
although the default policy for PowerShell is **Restricted**. If the policy is left as
**Restricted**, the SharePoint Management Shell changes the policy for PowerShell to
**RemoteSigned**. This means that you must select **Run as administrator** to start the SharePoint
Management Shell with elevated administrative permission. This change applies to all PowerShell
sessions. For more information about scripts and execution policies, see [about_scripts][03] and
[About Execution Policies][02].

<!-- link references -->
[01]: /dotnet/api/system.management.automation.runspaces.psthreadoptions
[02]: /powershell/module/microsoft.powershell.core/about/about_execution_policies
[03]: /powershell/module/microsoft.powershell.core/about/about_scripts
[04]: /powershell/module/microsoft.sharepoint.powershell
[05]: /powershell/module/microsoft.sharepoint.powershell/add-spshelladmin?view=sharepoint-ps&preserve-view=true
