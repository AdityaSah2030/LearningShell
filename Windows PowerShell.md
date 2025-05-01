# Windows PowerShell Commands Guide

This document provides a structured reference to commonly used Windows PowerShell commands for system administration, file operations, scripting, and configuration tasks.

---

## Navigation and Session Management

| Command | Description |
|---------|-------------|
| `Get-Location` or `pwd` | Display current directory |
| `Set-Location <path>` or `cd <path>` | Change current directory |
| `Push-Location` | Save current location to a stack |
| `Pop-Location` | Return to the previous location |
| `Clear-Host` or `cls` | Clear the terminal screen |
| `Exit` | Exit the PowerShell session |

---

## File and Directory Operations

| Command | Description |
|---------|-------------|
| `Get-ChildItem` or `ls` or `dir` | List directory contents |
| `New-Item -ItemType File -Name <name>` | Create a new file |
| `New-Item -ItemType Directory -Name <name>` | Create a new directory |
| `Remove-Item <path>` or `rm <path>` | Delete a file or folder |
| `Copy-Item <source> <destination>` | Copy files or folders |
| `Move-Item <source> <destination>` | Move files or folders |
| `Rename-Item <oldName> <newName>` | Rename a file or folder |

---

## File Content Manipulation

| Command | Description |
|---------|-------------|
| `Get-Content <file>` | Display contents of a file |
| `Set-Content <file> <text>` | Overwrite file with content |
| `Add-Content <file> <text>` | Append content to a file |
| `Out-File <file>` | Redirect output to a file |

---

## Process and Task Management

| Command | Description |
|---------|-------------|
| `Get-Process` | List running processes |
| `Stop-Process -Name <name>` | Terminate a process by name |
| `Start-Process <program>` | Launch a program or process |
| `Get-Service` | List all services |
| `Start-Service <name>` | Start a service |
| `Stop-Service <name>` | Stop a service |
| `Restart-Service <name>` | Restart a service |

---

## System Information and Configuration

| Command | Description |
|---------|-------------|
| `Get-ComputerInfo` | Display detailed system information |
| `Get-Host` | Show PowerShell version and host details |
| `Get-Command` | List all available commands |
| `Get-Help <command>` | Display help for a command |
| `Get-History` | Show command history |
| `Start-Sleep -Seconds <n>` | Pause script for specified seconds |

---

## Network Configuration

| Command | Description |
|---------|-------------|
| `Test-Connection <host>` | Ping a host (similar to `ping`) |
| `Resolve-DnsName <domain>` | Perform DNS lookup |
| `Get-NetIPAddress` | List IP configuration |
| `Get-NetAdapter` | List network adapters |
| `Get-NetRoute` | View routing table |
| `Get-NetTCPConnection` | Display active TCP connections |

---

## Environment Variables and Paths

| Command | Description |
|---------|-------------|
| `$env:PATH` | Show current PATH variable |
| `$env:USERNAME` | Display current user name |
| `$env:COMPUTERNAME` | Display computer name |
| `[System.Environment]::SetEnvironmentVariable()` | Set environment variable (requires specific arguments) |

---

## Scripting and Variables

| Command | Description |
|---------|-------------|
| `$var = "value"` | Create a variable |
| `Write-Output $var` | Display variable value |
| `Write-Host "Message"` | Print a message to the screen |
| `Read-Host "Prompt"` | Take input from user |
| `if`, `else`, `switch` | Conditional logic |
| `foreach`, `while`, `for` | Looping constructs |
| `function <name> { }` | Define a function |
| `.` (dot sourcing) | Run a script in the current scope |

---

## Aliases for Common Commands

| Alias | Actual Cmdlet |
|-------|----------------|
| `ls` | `Get-ChildItem` |
| `cd` | `Set-Location` |
| `pwd` | `Get-Location` |
| `cat` | `Get-Content` |
| `echo` | `Write-Output` |
| `rm` | `Remove-Item` |
| `mv` | `Move-Item` |
| `cp` | `Copy-Item` |

---

## Module and Package Management

| Command | Description |
|---------|-------------|
| `Get-Module` | List imported modules |
| `Import-Module <module>` | Import a module |
| `Install-Module <name>` | Install module from online repository (requires Admin) |
| `Update-Module <name>` | Update installed module |
| `Get-InstalledModule` | List installed modules |

---

## Security and Execution Policy

| Command | Description |
|---------|-------------|
| `Get-ExecutionPolicy` | Check current script execution policy |
| `Set-ExecutionPolicy RemoteSigned` | Allow running local scripts |
| `Set-ExecutionPolicy Bypass -Scope Process` | Temporarily bypass restrictions |

---

## Notes

- PowerShell supports powerful scripting capabilities, object-based output, and rich error handling.
- Unlike CMD, PowerShell passes objects (not plain text) between commands via the pipeline (`|`).
