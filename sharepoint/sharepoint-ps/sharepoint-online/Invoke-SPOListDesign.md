# Invoke-SPOListDesign

## SYNOPSIS

Applies a published list design to a specified site collection. The supported list templates you can apply a list design to include: "modern" team site with M365 group, "modern" team site without an M365 group, communication site, classic team site, and classic publishing site.

## SYNTAX

```powershell
Invoke-SPOListDesign
  [-Identity]
  -WebUrl <string>
  [<CommonParameters>]

```
## DESCRIPTION

Applies a published list design to a specified site collection target. This allows a list design to be applied to an existing site collection.

## EXAMPLES

### Example 1

This example applies a list design whose script creates one list with content types, views and fields

```powershell
Invoke-SPOListDesign -Identity 5b38e500-0fab-4da7-b011-ad7113228920 -WebUrl "https://contoso.sharepoint.com/sites/testgo"

```
### OUTPUT
```yaml
Title                                        OutcomeText Outcome
-----                                        ----------- -------
Create site column WorkAddress through XML               Success
Create site column _Status through XML                   Success
Create site column digits through XML                    Success
Create site column remarks through XML                   Success
Create site column workinghours through XML              Success
Create site column Progress through XML                  Success
Create content type Legal                                   NoOp
Add site column WorkAddress to content type                 NoOp
Add site column _Status to content type                     NoOp
Create content type test_210304                             NoOp
Add site column digits to content type                      NoOp
Add site column remarks to content type                     NoOp
Add site column workinghours to content type                NoOp
Add site column Progress to content type                    NoOp
Add site column _Status to content type                     NoOp
Create content type test_StatusComm                         NoOp
Add site column _Status to content type                     NoOp
Create content type test_11                                 NoOp
Add site column _Status to content type                     NoOp
Create or update library "test_ct"                       Success
Add list column "ActualWork"                             Success
Add list column "Initials"                               Success
Add list column "_Status"                                Success
Add list column "digits"                                 Success
Add list column "remarks"                                Success
Add list column "workinghours"                           Success
Add list column "Progress"                               Success
Add list column "_Comments"                              Success
Add list column "TriggerFlowInfo"                        Success
Add list column "SelectFilename"                         Success
Add content type "Document"                                 NoOp
Add content type "Folder"                                   NoOp
Add content type "Legal"                                 Success
Add content type "test_210304"                           Success
Add content type "test_StatusComm"                       Success
Add content type "test_11"                               Success
Add view "All Documents"                                 Success
Add view "All Documents sorted"                          Success

```

## PARAMETERS

### -Identity

The ID of the list design to apply.

```yaml
Type: SPOListDesignPipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -WebUrl

The URL of the site collection where the list design will be applied.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
