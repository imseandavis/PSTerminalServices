---
external help file: PSTerminalServices-help.xml
Module Name: PSTerminalServices
online version: http://code.msdn.microsoft.com/PSTerminalServices
schema: 2.0.0
---

# Stop-TSSession

## SYNOPSIS
Logs the session off, disconnecting any user that might be connected.

## SYNTAX

### Id (Default)
```
Stop-TSSession [-ComputerName <String>] [-Id] <Int32> [-Synchronous] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObject
```
Stop-TSSession [-ComputerName <String>] -InputObject <TerminalServicesSession> [-Synchronous] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Use Stop-TSSession to logoff the session and disconnect any user that might be connected.

## EXAMPLES

### EXAMPLE 1
```
Get-TSSession -ComputerName comp1 | Stop-TSSession
```

Description
-----------
logs off all connected users from Active sessions on remote computer 'comp1'.
The caller is prompted to
By default, the caller is prompted to confirm each action.

### EXAMPLE 2
```
Get-TSSession -ComputerName comp1 -State Active | Stop-TSSession -Force
```

Description
-----------
logs off any connected user from Active sessions on remote computer 'comp1'.
By default, the caller is prompted to confirm each action.
To override confirmations, the Force Switch parameter is specified.

### EXAMPLE 3
```
Get-TSSession -ComputerName comp1 -State Active -Synchronous | Stop-TSSession -Force
```

Description
-----------
logs off any connected user from Active sessions on remote computer 'comp1'.
The Synchronous parameter tells the command to
wait until the session is fully disconnected and only tghen it proceeds to the next session object.
By default, the caller is prompted to confirm each action.
To override confirmations, the Force Switch parameter is specified.

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

### -Id
Specifies the session Id number.

```yaml
Type: Int32
Parameter Sets: Id
Aliases: SessionId

Required: True
Position: 1
Default value: 0
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Specifies a session object.
Enter a variable that contains the object, or type a command or expression that gets the sessions.

```yaml
Type: TerminalServicesSession
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Synchronous
When the Synchronous parameter is present the command waits until the session is fully disconnected otherwise it returns
immediately, even though the session may not be completely disconnected yet.

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

## NOTES
Author: Shay Levy
Blog  : http://blogs.microsoft.co.il/blogs/ScriptFanatic/

## RELATED LINKS

[http://code.msdn.microsoft.com/PSTerminalServices](http://code.msdn.microsoft.com/PSTerminalServices)

[http://code.google.com/p/cassia/](http://code.google.com/p/cassia/)

[Get-TSSession
Disconnect-TSSession
Send-TSMessage]()

