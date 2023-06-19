---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Add-SPOSiteScriptPackage

## SYNOPSIS
Uploads a new site script package for use either directly or in a site design. The package file must be a zip archive containing all the files necessary for the site script. A file called “manifest.json” with script actions must be present in this zip file.

## SYNTAX

```
Add-SPOSiteScriptPackage -Title <String> -ContentPath <String> [-Description <String>] [<CommonParameters>]
```

## DESCRIPTION
Uploads a new site script package for use either directly or in a site design. The package file must be a zip archive containing all the files necessary for the site script. A file called “manifest.json” with script actions must be present in this zip file.

## EXAMPLES

### Example
This example adds a site script package as a zip file containing a manifest.json script, as well as a Dataverse solution zip file with a Power Automate flow definition.

File site-script-package.zip contains:
manifest.json:
```json
{
  "$schema": "schema.json",
  "actions": [
      {
        "verb": "importBusinessApps",
        "listName": "Contoso list",
        "solutionRelativeFilePath": "solution.zip"
      }
  ]
}
```

solution.zip

```powershell
PS C:\> Add-SPOSiteScriptPackage -Title "Install Contoso flow" -Description "Installs the new Contoso flow in a list" -ContentPath "c:\scripts\site-script-package.zip"
```

## PARAMETERS

### -ContentPath
The path to a zip archive file containing the content of the new site script package.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### -Title
The display name of the site script.

```yaml
Type: String
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

## RELATED LINKS
