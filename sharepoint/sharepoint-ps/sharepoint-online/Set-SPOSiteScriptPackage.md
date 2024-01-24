---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Set-SPOSiteScriptPackage

## SYNOPSIS
Updates a previously uploaded site script package. The package file must be a zip archive containing all the files necessary for the site script. A file called "manifest.json" with script actions must be present in this zip file.

## SYNTAX

```
Set-SPOSiteScriptPackage -Identity <SPOSiteScriptPipeBind> [-Title <String>] [-ContentPath <String>]
 [-Description <String>] [-Version <Int32>] [<CommonParameters>]
```

## DESCRIPTION
Updates a previously uploaded site script package. The package file must be a zip archive containing all the files necessary for the site script. A file called "manifest.json" with script actions must be present in this zip file.

## EXAMPLES

### Example 1
```powershell
$manifestContent = @'
{
  "$schema": "schema.json",
  "actions": [
      {
        "verb": "importBusinessApps",
        "listName": "Contoso list",
        "solutionRelativeFilePath": "solution.zip"
      }
  ],
  "version": 2
}
'@;
Set-Content "manifest.json" $manifestContent
$compress = @{
  Path = ".\manifest.json", ".\solution.zip"
  DestinationPath = "c:\scripts\site-script-package-v2.zip"
}
Compress-Archive @compress

Set-SPOSiteScriptPackage -Identity edaec4ec-71e2-4026-ac1e-6686bb30190e -Title "Install Contoso flow" -Description "Installs the new Contoso flow in a list" -ContentPath "c:\scripts\site-script-package-v2.zip" -Version 2
```

This example updates a site script package with ID 'edaec4ec-71e2-4026-ac1e-6686bb30190e' as a zip file containing a manifest.json with script actions as exemplified previously and an updated Dataverse solution zip file.

## PARAMETERS

### -ContentPath
The absolute path to a zip archive file containing the content of the new site script package.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
A description of the site script.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
The ID of the site script.

```yaml
Type: SPOSiteScriptPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title
The display name of the site script.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
The version number of the site script.

```yaml
Type: Int32
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

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
