---
external help file: PSTerminalServices-help.xml
Module Name: PSTerminalServices
online version: http://code.msdn.microsoft.com/PSTerminalServices
schema: 2.0.0
---

# Get-TSServers

## SYNOPSIS
Enumerates all terminal servers in a given domain.

## SYNTAX

```
Get-TSServers [[-DomainName] <String>] [<CommonParameters>]
```

## DESCRIPTION
Enumerates all terminal servers in a given domain.

## EXAMPLES

### EXAMPLE 1
```
Get-TSDomainServers
```

Description
-----------
Get a list of all terminal servers of the caller default domain.

## PARAMETERS

### -DomainName
The name of the domain.
The default is the caller domain name ($env:USERDOMAIN).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $env:USERDOMAIN
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
Author: Shay Levy
Blog  : http://blogs.microsoft.co.il/blogs/ScriptFanatic/

## RELATED LINKS

[http://code.msdn.microsoft.com/PSTerminalServices](http://code.msdn.microsoft.com/PSTerminalServices)

[http://code.google.com/p/cassia/](http://code.google.com/p/cassia/)

[Get-TSSession]()

