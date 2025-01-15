---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spmachinekey
applicable: SharePoint Server Subscription Edition
title: Set-SPMachineKey
schema: 2.0.0
---

# Set-SPMachineKey

## SYNOPSIS
Configures the ASP.NET view state decryption and validation keys of a web application.

## SYNTAX

```
Set-SPMachineKey -WebApplication <SPWebApplicationPipeBind> [-DecryptionKey <String>] [-ValidationKey <String>]
 [-Local] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The \`Set-SPMachineKey\` cmdlet configures the ASP.NET view state decryption and validation keys of a web application.

## EXAMPLES

### -------------EXAMPLE 1------------- 
```powershell
Set-SPMachineKey -WebApplication http://sitename
```

This example sets the ASP.NET view state decryption and validation keys for web application 'http://sitename' to new randomly generated keys.
The new keys are deployed to all servers in the farm.

### -------------EXAMPLE 2------------- 
```powershell
Set-SPMachineKey -WebApplication http://sitename -DecryptionKey '<Your Key!>' -ValidationKey '<Your Key!>' -Local
```

The preceding sample sets the ASP.NET view state decryption and validation keys for web application 'http://sitename' to new keys specified by the DecryptionKey and ValidationKey parameters. The new keys are only deployed to the local server. Other servers in the farm will continue to use the previous keys.

See **How to generate a `<machineKey> element`** in the [Resolving view state message authentication code (MAC) errors](https://support.microsoft.com/en-us/topic/resolving-view-state-message-authentication-code-mac-errors-6c0e9fd3-f8a8-c953-8fbe-ce840446a9f3) support article for information on generating keys.

## PARAMETERS

### -AssignmentCollection
Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DecryptionKey
Specifies the new ASP.NET view state decryption key.
The key should be represented as a 64-character long hexadecimal string (0-9 and A-F).

If this parameter is not specified, a random decryption key will be generated and used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
Deploy the new decryption and validation keys only to the local server.
Other servers in the farm will continue to use the previous decryption and validation keys.
Web sessions that are load balanced across multiple servers in the farm will fail if these keys are not synchronized on every server in the farm.
Use the Update-SPMachineKey cmdlet to deploy the keys to additional servers in the farm.

If this parameter is not specified, the new decryption and validation keys will be deployed to all servers in the farm.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidationKey
Specifies the new ASP.NET view state validation key.
The key should be represented as a 64-character long hexadecimal string (0-9 and A-F).

If this parameter is not specified, a random decryption key will be generated and used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplication
Specifies the name, URL, or GUID of the Web application.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
