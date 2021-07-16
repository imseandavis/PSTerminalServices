---
external help file: PSTerminalServices-help.xml
Module Name: PSTerminalServices
online version: http://code.msdn.microsoft.com/PSTerminalServices
schema: 2.0.0
---

# Get-TSSession

## SYNOPSIS
Lists the sessions on a given terminal server.

## SYNTAX

### Session (Default)
```
Get-TSSession [-ComputerName <String>] [[-Id] <Int32>] [-State <String>] [-ClientName <String>]
 [-UserName <String>] [<CommonParameters>]
```

### InputObject
```
Get-TSSession [-ComputerName <String>] [-InputObject] <TerminalServicesSession> [-State <String>]
 [-ClientName <String>] [-UserName <String>] [<CommonParameters>]
```

### Filter
```
Get-TSSession [-ComputerName <String>] -Filter <ScriptBlock> [-State <String>] [-ClientName <String>]
 [-UserName <String>] [<CommonParameters>]
```

## DESCRIPTION
Use Get-TSSession to get a list of sessions from a local or remote computers.
Note that Get-TSSession is using Aliased properties to display the output on the console (IPAddress and State), these attributes
are not the same as the original attributes (ClientIPAddress and ConnectionState).
This is important when you want to use the -Filter parameter which requires the latter.
To see all aliassed properties and their corresponding properties (Definition column), pipe the result to Get-Member:

PS \> Get-TSSession | Get-Member -MemberType AliasProperty

   TypeName: Cassia.Impl.TerminalServicesSession

Name      MemberType    Definition
----      ----------    ----------
(...)
IPAddress AliasProperty IPAddress = ClientIPAddress
State     AliasProperty State = ConnectionState

## EXAMPLES

### EXAMPLE 1
```
Get-TSSession
```

Description
-----------
Gets all the sessions from the local computer.

### EXAMPLE 2
```
Get-TSSession -ComputerName comp1 -State Disconnected
```

Description
-----------
Gets all the disconnected sessions from the remote computer 'comp1'.

### EXAMPLE 3
```
Get-TSSession -ComputerName comp1 -Filter {$_.ClientIPAddress -like '10*' -AND $_.ConnectionState -eq 'Active'}
```

Description
-----------
Gets all Active sessions from remote computer 'comp1', made from ip addresses that starts with '10'.

### EXAMPLE 4
```
Get-TSSession -ComputerName comp1 -UserName a*
```

Description
-----------
Gets all sessions from remote computer 'comp1' made by users with name starts with the letter 'a'.

### EXAMPLE 5
```
Get-TSSession -ComputerName comp1 -ClientName s*
```

Description
-----------
Gets all sessions from remote computer 'comp1' made from a computers names that starts with the letter 's'.

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies the session Id number.

```yaml
Type: Int32
Parameter Sets: Session
Aliases: SessionID

Required: False
Position: 1
Default value: -1
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
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Filter
Specifies a filter based on the session properties.
The syntax of the filter, including the use of
wildcards and depends on the properties of the session.
Internally, The Filter parameter uses client side
filtering using the Where-Object cmdlet, objects are filtered after they are retrieved.

```yaml
Type: ScriptBlock
Parameter Sets: Filter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
The connection state of the session.
Use this parameter to get sessions of a specific state.
Valid values are:

Value		 Description
-----		 -----------
Active		 A user is logged on to the session.
ConnectQuery The session is in the process of connecting to a client.
Connected	 A client is connected to the session).
Disconnected The session is active, but the client has disconnected from it.
Down		 The session is down due to an error.
Idle		 The session is waiting for a client to connect.
Initializing The session is initializing.
Listening 	 The session is listening for connections.
Reset		 The session is being reset.
Shadowing	 This session is shadowing another session.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionState

Required: False
Position: Named
Default value: *
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientName
The name of the machine last connected to a session.
Use this parameter to get sessions made from a specific computer name.
Wildcrads are permitted.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: *
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Use this parameter to get sessions made by a specific user name.
Wildcrads are permitted.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: *
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

[Stop-TSSession
Disconnect-TSSession
Send-TSMessage]()

