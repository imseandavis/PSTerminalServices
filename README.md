---
Module Name: PSTerminalServices
Module Guid: e7e54679-f0fe-4157-85a2-dfc0575e6209
Download Help Link: https://www.powershellgallery.com/packages/PSTerminalServices/1.0
Help Version: 1.0
Locale: en-US
---

*Originally authored by Shay Levy (c) 2009.*

# PSTerminalServices Module
## Description
The PSTerminalServices module contains functions to manage Terminal Services sessions and processes (including Remote Desktop connections).

## PSTerminalServices Cmdlets
### [Disconnect-TSSession](PSTerminalServices/en-US/Disconnect-TSSession.md)
Disconnects any connected user from the session.

### [Get-TSCurrentSession](PSTerminalServices/en-US/Get-TSCurrentSession.md)
Provides information about the session in which the current process is running.

### [Get-TSProcess](PSTerminalServices/en-US/Get-TSProcess.md)
Gets a list of processes running in a specific session or in all sessions.

### [Get-TSServers](PSTerminalServices/en-US/Get-TSServers.md)
Enumerates all terminal servers in a given domain.

### [Get-TSSession](PSTerminalServices/en-US/Get-TSSession.md)
Lists the sessions on a given terminal server.

### [Send-TSMessage](PSTerminalServices/en-US/Send-TSMessage.md)
Displays a message box in the specified session Id.

### [Stop-TSProcess](PSTerminalServices/en-US/Stop-TSProcess.md)
Terminates the process running in a specific session or in all sessions.

### [Stop-TSSession](PSTerminalServices/en-US/Stop-TSSession.md)
Logs the session off, disconnecting any user that might be connected.

## File Tree
```
PSTERMINALSERVICES
|   PSTerminalServices.msi
|   README.md
|   
\---PSTerminalServices
    |   PSTerminalServices.psd1
    |   PSTerminalServices.psm1
    |   
    +---Bin
    |       Cassia.dll
    |       Cassia.zip
    |       
    +---en-US
    |       about_PSTerminalServices_Module.help.txt
    |       Disconnect-TSSession.md
    |       Get-TSCurrentSession.md
    |       Get-TSProcess.md
    |       Get-TSServers.md
    |       Get-TSSession.md
    |       Send-TSMessage.md
    |       Stop-TSProcess.md
    |       Stop-TSSession.md
    |       
    \---Format
            PSFanatic.PSTerminalServices.Format.ps1xml
```
