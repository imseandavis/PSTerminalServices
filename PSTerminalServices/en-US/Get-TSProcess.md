---
external help file: PSTerminalServices-help.xml
Module Name: PSTerminalServices
online version: http://code.msdn.microsoft.com/PSTerminalServices
schema: 2.0.0
---

# Get-TSProcess

## SYNOPSIS
Gets a list of processes running in a specific session or in all sessions.

## SYNTAX

### Name (Default)
```
Get-TSProcess [-ComputerName <String>] [[-Name] <String>] [<CommonParameters>]
```

### Id
```
Get-TSProcess [-ComputerName <String>] -Id <Int32> [<CommonParameters>]
```

### InputObject
```
Get-TSProcess [-ComputerName <String>] [-InputObject] <TerminalServicesProcess> [<CommonParameters>]
```

### Session
```
Get-TSProcess [-ComputerName <String>] [-Session] <TerminalServicesSession> [<CommonParameters>]
```

## DESCRIPTION
Use Get-TSProcess to get a list of session processes from a local or remote computers.

## EXAMPLES

### EXAMPLE 1
```
Get-TSProcess
```

Description
-----------
Gets all the sessions processes from the local computer.

### EXAMPLE 2
```
Get-TSSession -Id 0 -ComputerName comp1 | Get-TSProcess
```

Description
-----------
Gets all processes connected to session id 0 from remote computer 'comp1'.

### EXAMPLE 3
```
Get-TSProcess -Name s* -ComputerName comp1
```

Description
-----------
Gets all the processes with name starts with the letter 's' from remote computer 'comp1'.

## PARAMETERS

### -ComputerName
The name of the terminal server computer.
The default is the local computer.
Default value is the local computer (localhost).

```yaml
Type: String
Parameter Sets: (All)
Aliases: CN, IPAddress

Required: False
Position: Named
Default value: $script:server
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the process name.
Wildcards are permitted.

```yaml
Type: String
Parameter Sets: Name
Aliases: ProcessName

Required: False
Position: 1
Default value: *
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
Specifies the process Id number.

```yaml
Type: Int32
Parameter Sets: Id
Aliases: ProcessID

Required: True
Position: Named
Default value: -1
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -InputObject
Specifies a process object.
Enter a variable that contains the object, or type a command or expression that gets the sessions.

```yaml
Type: TerminalServicesProcess
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Session
Specifies the session Id number.

```yaml
Type: TerminalServicesSession
Parameter Sets: Session
Aliases: SessionId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Cassia.Impl.TerminalServicesProcess
## NOTES
Author: Shay Levy
Blog  : http://blogs.microsoft.co.il/blogs/ScriptFanatic/

## RELATED LINKS

[http://code.msdn.microsoft.com/PSTerminalServices](http://code.msdn.microsoft.com/PSTerminalServices)

[http://code.google.com/p/cassia/](http://code.google.com/p/cassia/)

[Get-TSSession
Stop-TSProcess]()

