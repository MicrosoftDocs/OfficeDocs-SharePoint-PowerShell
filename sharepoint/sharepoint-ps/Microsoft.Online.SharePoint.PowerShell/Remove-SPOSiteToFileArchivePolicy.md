---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Remove-SPOSiteToFileArchivePolicy

## SYNOPSIS
Removes a site from a File Archive Policy.

## SYNTAX

```
Remove-SPOSiteToFileArchivePolicy -PolicyId <Guid> -Site <SpoSitePipeBind> [<CommonParameters>]
```

## DESCRIPTION
The `Remove-SPOSiteToFileArchivePolicy` cmdlet removes a site from an existing File Archive Policy. The site will no longer be included in future policy runs.

You must be a SharePoint Administrator or Global Administrator to run this cmdlet.

## EXAMPLES

### Example 1
```powershell
PS C:\> Remove-SPOSiteToFileArchivePolicy -PolicyId "a1b2c3d4-e5f6-7890-abcd-ef1234567890" -Site "https://contoso.sharepoint.com/sites/marketing"
```

Removes the marketing site from the specified File Archive Policy.

## PARAMETERS

### -PolicyId
Specifies the unique identifier (GUID) of the policy to remove the site from.

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
Specifies the URL of the site to remove from the policy (e.g., "https://contoso.sharepoint.com/sites/marketing").

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
