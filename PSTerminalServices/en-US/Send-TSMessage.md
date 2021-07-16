---
external help file: PSTerminalServices-help.xml
Module Name: PSTerminalServices
online version: http://code.msdn.microsoft.com/PSTerminalServices
schema: 2.0.0
---

# Send-TSMessage

## SYNOPSIS
Displays a message box in the specified session Id.

## SYNTAX

### Session (Default)
```
Send-TSMessage [-ComputerName <String>] [-Text] <String> [-Caption <String>] [[-Id] <Int32>]
 [<CommonParameters>]
```

### InputObject
```
Send-TSMessage [-ComputerName <String>] [-Text] <String> [-Caption <String>]
 [-InputObject] <TerminalServicesSession> [<CommonParameters>]
```

## DESCRIPTION
Use Send-TSMessage display a message box in the specified session Id.

## EXAMPLES

### EXAMPLE 1
```
$Message = "Importnat message`n, the server is going down for maintanace in 10 minutes. Please save your work and logoff."
```

Get-TSSession -State Active -ComputerName comp1 | Send-TSMessage -Message $Message

Description
-----------
Displays a message box inside all active sessions of computer name 'comp1'.

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

### -Text
The text to display in the message box.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Caption
The caption of the message box.
The default caption is 'Alert'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
{{ Fill Id Description }}

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
{{ Fill InputObject Description }}

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

