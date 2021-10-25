---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOBuiltInSiteTemplateSettings
applicable: SharePoint Online
title: Set-SPOBuiltInSiteTemplateSettings
schema: 2.0.0
author: Holland-ODSP
ms.author: hokavian
ms.reviewer:
---

# Set-SPOBuiltInSiteTemplateSettings

## SYNOPSIS

Sets all or specific Microsoft-provided SharePoint site templates to be displayed or hidden in the site template gallery in your tenant. All site templates are displayed by default. 

## SYNTAX

```powershell
Set-SPOBuiltInSiteTemplateSettings -Identity <object> -IsHidden <bool>
```

## DESCRIPTION

The `Set-SPOBuiltInSiteTemplateSettings` cmdlet sets a specific Microsoft-provided SharePoint site templates to be displayed or hidden in the site template gallery in your tenant. 

All site templates are displayed by default.

| Team site templates  | Template ID                 | 
| :------------------- | :------------------- |
| Event planning  | 9522236e-6802-4972-a10d-e98dc74b3344 | 
| Project management              | f0a3abf4-afe8-4409-b7f3-484113dee93e| 
| Training and courses        | 695e52c9-8af7-4bd3-b7a5-46aca95e1c7e  | 
| Training and development team     | 64aaa31e-7a1e-4337-b646-0b700aa9a52c | 
| Team collaboration     | 6b96e7b1-035f-430b-92ca-31511c51ca72  | 


| Communication site templates | Template ID                 | 
| :------------------- | :------------------- |
| Crisis management  | 905bb0b4-01e8-4f55-b73c-f07f08aee3a4 | 
| Department  | 73495f08-0140-499b-8927-dd26a546f26a   | 
| Leadership connection    | cd4c26b2-b231-419a-8bb4-9b1d9b83aef6 | 
| Learning central       | b8ef3134-92a2-4c9d-bca6-c2f14e79fe98  | 
| New employee onboarding      | 2a23fa44-52b0-4814-baba-06fef1ab931e   | 
| Showcase  | 89f21161-0892-497a-91cb-5783eeb1f5f2   | 
| Topic     | a30fef54-a4e5-4beb-a8b5-962c528d753a   | 
| Blank    | 665da395-e0f9-4c92-b35c-773d8c292f2d  | 

You can hide all templates by specifying an empty ID of "00000000-0000-0000-0000-000000000000". Settings specified for a specific template will take precedence over the "all templates" setting. You can hide all templates and then selectively make specific templates visible. [Learn more about SharePoint site templates](support.microsoft.com/office/apply-and-customize-sharepoint-site-templates-39382463-0e45-4d1b-be27-0e96aeec8398).


>[!NOTE]
> - All site templates are displayed by default. [Learn more](support.microsoft.com/office/apply-and-customize-sharepoint-site-templates-39382463-0e45-4d1b-be27-0e96aeec8398?ui=en-US&rs=en-US&ad=US) about SharePoint site templates
> - You must have SharePoint admin credentials (or higher) to use SharePoint PowerShell.
> - The minimum SharePoint PowerShell version required is 16.0.21610.12000.
> - For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell?view=sharepoint-ps).


## EXAMPLES 

### Example 1: This example hides the Department template from the site template gallery.  

```powershell
Set-SPOBuiltInSiteTemplateSettings -Identity "73495f08-0140-499b-8927-dd26a546f26a" -IsHidden $true
```

###  Example 2: This example displays the Department template in the site template gallery. Note all site templates are displayed by default, so this is most relevant if a template has been hidden before.   

```powershell
Set-SPOBuiltInSiteTemplateSettings -Identity "73495f08-0140-499b-8927-dd26a546f26a" -IsHidden $false
```

### Example 3: This example hides all built-in templates from the site template gallery.  

```powershell
Set-SPOBuiltInSiteTemplateSettings -Identity "00000000-0000-0000-0000-000000000000" -IsHidden $true
```



## PARAMETERS

#### -Identity
 
Specifies the ID for the site template you wish to change. 
 
#### -IsHidden
 
Specifies whether the site template is hidden ($true) or displayed ($false). All site templates are displayed by default.


