---
external help file: PSTerminalServices-help.xml
Module Name: PSTerminalServices
online version: http://code.msdn.microsoft.com/PSTerminalServices
schema: 2.0.0
---

# Stop-TSProcess

## SYNOPSIS
Terminates the process running in a specific session or in all sessions.

## SYNTAX

### Name (Default)
```
Stop-TSProcess [-ComputerName <String>] [[-Name] <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Id
```
Stop-TSProcess [-ComputerName <String>] -Id <Int32> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Stop-TSProcess [-ComputerName <String>] [-InputObject] <TerminalServicesProcess> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Session
```
Stop-TSProcess [-ComputerName <String>] [-Session] <TerminalServicesSession> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
Use Stop-TSProcess to terminate one or more processes from a local or remote computers.

## EXAMPLES

### EXAMPLE 1
```
Get-TSProcess -Id 6552 | Stop-TSProcess
```

Description
-----------
Gets process Id 6552 from the local computer and stop it.
Confirmations needed.

### EXAMPLE 2
```
Get-TSSession -Id 3 -ComputerName comp1 | Stop-TSProcess -Force
```

Description
-----------
Terminats all processes connected to session id 3 from remote computer 'comp1', suppress confirmations.

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

### -Force
Overrides any confirmations made by the command.

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

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

### Cassia.Impl.TerminalServicesProcess
## NOTES
Author: Shay Levy
Blog  : http://blogs.microsoft.co.il/blogs/ScriptFanatic/

## RELATED LINKS

[http://code.msdn.microsoft.com/PSTerminalServices](http://code.msdn.microsoft.com/PSTerminalServices)

[http://code.google.com/p/cassia/](http://code.google.com/p/cassia/)

[Get-TSProcess
Get-TSSession]()

