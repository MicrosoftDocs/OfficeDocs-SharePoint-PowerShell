---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Add-SPOSiteToFileArchivePolicy

## SYNOPSIS
Adds a site to a File Archive Policy.

## SYNTAX

```
Add-SPOSiteToFileArchivePolicy -PolicyId <Guid> -Site <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION
The `Add-SPOSiteToFileArchivePolicy` cmdlet adds a site to an existing File Archive Policy that has a PolicyType of "SelectedSites". The site must exist and be eligible for archiving. At least one site must be added before a "SelectedSites" policy can be activated.

You must be a SharePoint Administrator or Global Administrator to run this cmdlet.

## EXAMPLES

### Example 1
```powershell
PS C:\> Add-SPOSiteToFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890" -Site "https://contoso.sharepoint.com/sites/marketing"
```

Adds the marketing site to the specified File Archive Policy.

## PARAMETERS

### -PolicyId
Specifies the unique identifier (GUID) of the policy to add the site to.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site
Specifies the URL of the site to add to the policy (e.g., "https://contoso.sharepoint.com/sites/marketing"). The site must exist and be eligible for archiving.

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

This cmdlet is part of the File Archive Policies feature which is currently in preview.

## RELATED LINKS
