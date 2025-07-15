---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/Set-SPOBuiltInSiteTemplateSettings
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

```
Set-SPOBuiltInSiteTemplateSettings [-Identity] <SPOBuiltInSiteTemplateSettingsPipeBind> [-IsHidden <Boolean>]
 [<CommonParameters>]
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
| Team collaboration     | c8b3137a-ca4c-48a9-b356-a8e7987dd693  |
| Retail management     | e4ec393e-da09-4816-b6b2-195393656edd  |

<br>

| Communication site templates | Template ID                 |
| :------------------- | :------------------- |
| Brand central| f2c6bb0c-9234-40c2-9ec3-ee86a70330fb|
| Crisis management| 905bb0b4-01e8-4f55-b73c-f07f08aee3a4 |
| Department| 73495f08-0140-499b-8927-dd26a546f26a   |
| Event| 3e4352aa-0cff-44aa-87c9-fefba31f1434|
| Human resources| b8ef3134-92a2-4c9d-bca6-c2f14e79fe98|
| Leadership connection    | cd4c26b2-b231-419a-8bb4-9b1d9b83aef6 |
| Learning central       | b8ef3134-92a2-4c9d-bca6-c2f14e79fe98  |
| New employee onboarding| 2a23fa44-52b0-4814-baba-06fef1ab931e   |
| Organization home| 6da87011-20ac-4123-a6b8-44c8e4c99d91|
| Showcase| 89f21161-0892-497a-91cb-5783eeb1f5f2|
| Volunteer center| b6e04a41-1535-4313-a856-6f3515d31999   |
| Topic     | a30fef54-a4e5-4beb-a8b5-962c528d753a   |
| Blank    | f6cc5403-0d63-442e-96c0-285923709ffc  |

You can hide all templates by specifying an empty ID of "00000000-0000-0000-0000-000000000000". Settings specified for a specific template will take precedence over the "all templates" setting. You can hide all templates and then selectively make specific templates visible. [Learn more about SharePoint site templates](https://support.microsoft.com/office/apply-and-customize-sharepoint-site-templates-39382463-0e45-4d1b-be27-0e96aeec8398).



>[!NOTE]
> - All site templates are displayed by default. [Learn more](https://support.microsoft.com/office/apply-and-customize-sharepoint-site-templates-39382463-0e45-4d1b-be27-0e96aeec8398) about SharePoint site templates
> - You must have SharePoint admin credentials (or higher) to use SharePoint PowerShell.
> - The minimum SharePoint PowerShell version required is 16.0.21610.12000.
> - For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).



## EXAMPLES

### Example 1: Hide a template

This example hides the Department template from the site template gallery.

```powershell
Set-SPOBuiltInSiteTemplateSettings -Identity "73495f08-0140-499b-8927-dd26a546f26a" -IsHidden $true
```

###  Example 2: Display a template that's been hidden

This example displays the Department template in the site template gallery. Note all site templates are displayed by default, so this is most relevant if a template has been hidden before.

```powershell
Set-SPOBuiltInSiteTemplateSettings -Identity "73495f08-0140-499b-8927-dd26a546f26a" -IsHidden $false
```

### Example 3: Hide all templates from Microsoft

This example hides all built-in templates from the site template gallery.

```powershell
Set-SPOBuiltInSiteTemplateSettings -Identity "00000000-0000-0000-0000-000000000000" -IsHidden $true
```



## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the ID for the site template you wish to change.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOBuiltInSiteTemplateSettingsPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsHidden

> Applicable: SharePoint Online

Specifies whether the site template is hidden ($true) or displayed ($false). All site templates are displayed by default.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SPOBuiltInSiteTemplateSettingsPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPOBuiltInSiteTemplateSettings](Get-SPOBuiltInSiteTemplateSettings.md)

[Apply and customize SharePoint sites](https://support.microsoft.com/office/apply-and-customize-sharepoint-site-templates-39382463-0e45-4d1b-be27-0e96aeec8398)

