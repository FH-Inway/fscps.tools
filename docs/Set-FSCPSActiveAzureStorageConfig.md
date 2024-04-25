﻿---
external help file: fscps.tools-help.xml
Module Name: fscps.tools
online version:
schema: 2.0.0
---

# Set-FSCPSActiveAzureStorageConfig

## SYNOPSIS
Set the active Azure Storage Account configuration

## SYNTAX

```
Set-FSCPSActiveAzureStorageConfig [[-Name] <String>] [[-ConfigStorageLocation] <String>] [-Temporary]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Updates the current active Azure Storage Account configuration with a new one

## EXAMPLES

### EXAMPLE 1
```
Set-FSCPSActiveAzureStorageConfig -Name "UAT-Exports"
```

This will import the "UAT-Exports" set from the Azure Storage Account configurations.
It will update the active Azure Storage Account configuration.

### EXAMPLE 2
```
Set-FSCPSActiveAzureStorageConfig -Name "UAT-Exports" -ConfigStorageLocation "System"
```

This will import the "UAT-Exports" set from the Azure Storage Account configurations.
It will update the active Azure Storage Account configuration.
The data will be stored in the system wide configuration storage, which makes it accessible from all users.

### EXAMPLE 3
```
Set-FSCPSActiveAzureStorageConfig -Name "UAT-Exports" -Temporary
```

This will import the "UAT-Exports" set from the Azure Storage Account configurations.
It will update the active Azure Storage Account configuration.
The update will only last for the rest of this PowerShell console session.

## PARAMETERS

### -Name
The name the Azure Storage Account configuration you want to load into the active Azure Storage Account configuration

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigStorageLocation
Parameter used to instruct where to store the configuration objects

The default value is "User" and this will store all configuration for the active user

Valid options are:
"User"
"System"

"System" will store the configuration so all users can access the configuration objects

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: User
Accept pipeline input: False
Accept wildcard characters: False
```

### -Temporary
Instruct the cmdlet to only temporarily override the persisted settings in the configuration storage

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgressAction
{{ Fill ProgressAction Description }}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: proga

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
This is refactored function from d365fo.tools

Original Author: Mötz Jensen (@Splaxi)
Author: Oleksandr Nikolaiev (@onikolaiev)

You will have to run the Add-FSCPSAzureStorageConfig cmdlet at least once, before this will be capable of working.

## RELATED LINKS
