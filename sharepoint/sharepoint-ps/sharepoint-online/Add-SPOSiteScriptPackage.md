---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version:
schema: 2.0.0
---

# Add-SPOSiteScriptPackage

## SYNOPSIS
Uploads a new site script package for use either directly or in a site design.

## SYNTAX

```
Add-SPOSiteScriptPackage -Title <String> -ContentPath <String> [-Description <String>] [<CommonParameters>]
```

## DESCRIPTION
Uploads a new site script package for use either directly or in a site design. The package file must be a zip archive containing all the files necessary for the site script. A file called “manifest.json” with script actions must be present in this zip file.

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
  ]
}'@;
Set-Content "manifest.json" $manifestContent
$compress = @{
  Path = ".\manifest.json", ".\solution.zip"
  DestinationPath = "c:\scripts\site-script-package.zip"
}
Compress-Archive @compress

Add-SPOSiteScriptPackage -Title "Install Contoso flow" -Description "Installs the new Contoso flow in a list" -ContentPath "c:\scripts\site-script-package.zip"
```

This example adds a site script package as a zip file containing a manifest.json with script actions as exemplified previously, as well as a Dataverse solution zip file with a Power Automate flow definition.
 
## PARAMETERS

### -ContentPath
The absolute path to a zip archive file containing the content of the new site script package.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
