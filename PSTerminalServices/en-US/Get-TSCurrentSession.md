---
external help file: PSTerminalServices-help.xml
Module Name: PSTerminalServices
online version: http://code.msdn.microsoft.com/PSTerminalServices
schema: 2.0.0
---

# Get-TSCurrentSession

## SYNOPSIS
Provides information about the session in which the current process is running.

## SYNTAX

```
Get-TSCurrentSession [[-ComputerName] <String>] [<CommonParameters>]
```

## DESCRIPTION
Provides information about the session in which the current process is running.

## EXAMPLES

### EXAMPLE 1
```
Get-TSCurrentSession
```

Description
-----------
Displays the session in which the current process is running on the local computer.

## PARAMETERS

### -ComputerName
{{ Fill ComputerName Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: CN, IPAddress

Required: False
Position: 1
Default value: $script:server
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Cassia.Impl.TerminalServicesSession
## NOTES
Author: Shay Levy
Blog  : http://blogs.microsoft.co.il/blogs/ScriptFanatic/

## RELATED LINKS

[http://code.msdn.microsoft.com/PSTerminalServices](http://code.msdn.microsoft.com/PSTerminalServices)

[http://code.google.com/p/cassia/](http://code.google.com/p/cassia/)

[Get-TSSession]()

