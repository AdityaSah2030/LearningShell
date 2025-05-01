# Windows CMD Commands Guide

This document provides a structured reference to commonly used commands in the Windows Command Prompt (CMD), useful for navigation, file management, system configuration, and troubleshooting.

---

## Navigation Commands

| Command | Description |
|---------|-------------|
| `cd <name>` | Change directory |
| `cd ..` | Move up one directory level |
| `cd Desktop\Videos` | Navigate into nested directories |
| `cd ../..` | Move up two directory levels |
| `TAB` | Auto-complete directory or file names |
| `HOME` | Move cursor to the start of the command |
| `END` | Move cursor to the end of the command |
| `CTRL + ←` | Move cursor one word to the left |
| `CTRL + →` | Move cursor one word to the right |
| `CTRL + C` | Terminate the current command |
| `CTRL + Z` | Suspend the current process |
| `↑ / ↓` | Navigate through command history |

---

## Directory Listing and Navigation

| Command | Description |
|---------|-------------|
| `dir` | List directory contents |
| `dir /a` | List all files, including hidden |
| `dir /s` | List contents of directory and subdirectories recursively |

---

## Creating and Deleting Directories

| Command | Description |
|---------|-------------|
| `mkdir <folderName>` | Create a new directory |
| `rmdir <folderName>` | Remove an empty directory |
| `rmdir /s <folderName>` | Remove a directory including its contents |
| `del /f /q <fileName>` | Force delete a file without confirmation |

---

## File Operations

| Command | Description |
|---------|-------------|
| `start <fileName>` | Open a file with its default program |
| `more <fileName>` | View file contents page by page |
| `type <fileName.txt>` | Display contents of a text file |
| `echo text > <fileName.txt>` | Create or overwrite a text file with specified content |
| `echo text >> <fileName.txt>` | Append content to a text file |
| `dir > listing.txt` | Save directory listing to a file |

---

## File and Directory Management

| Command | Description |
|---------|-------------|
| `copy abc.txt folderName` | Copy a file to a specified folder |
| `xcopy source destination` | Copy files and directories |
| `xcopy source destination /s` | Copy files including subdirectories |
| `move source destination` | Move a file or directory |
| `rename oldName newName` | Rename a file or folder |

---

## Network and IP Configuration

| Command | Description |
|---------|-------------|
| `ipconfig` | Display IP configuration details |
| `ipconfig /all` | Display detailed network configuration |
| `ipconfig /renew` | Renew IP address for all adapters |
| `ipconfig /release` | Release IP address for all adapters |
| `ipconfig /flushdns` | Clear the DNS resolver cache |
| `ipconfig /allcompartments /all` | Show details of all network compartments |

---

## Network Diagnostics

| Command | Description |
|---------|-------------|
| `ping <host>` | Test network connectivity to a host |
| `tracert <host>` | Trace route to a host |
| `netstat -an` | Show active network connections and listening ports |
| `nslookup <domain>` | Query DNS for domain resolution |

---

## System Path and Environment Variables

| Command | Description |
|---------|-------------|
| `path` | Display system path variable |
| `set PATH=%PATH%;C:\NewPath` | Temporarily add a new directory to the system path |

---

## Drive and Disk Management

| Command | Description |
|---------|-------------|
| `wmic logicaldisk get name` | List all drive letters |
| `D:` | Change to D drive |
| `tree` | Display directory structure as a tree |
| `diskpart` | Launch disk partition management utility |

---

## Color and Appearance

| Command | Description |
|---------|-------------|
| `color XY` | Set background (X) and foreground (Y) colors |
| `color` | Reset CMD color settings |
| `color /?` | Show available color codes and help |

---

## File Attributes

| Command | Description |
|---------|-------------|
| `attrib +R` | Set file to read-only |
| `attrib -R` | Remove read-only attribute |
| `attrib +H` | Hide a file |
| `attrib -H` | Unhide a file |
| `attrib /S /D` | Apply attributes to files and directories recursively |

---

## System Information and Process Control

| Command | Description |
|---------|-------------|
| `tasklist` | Display running processes |
| `taskkill /IM notepad.exe /F` | Forcefully terminate a process by name |
| `shutdown /s /t 0` | Shut down the computer immediately |
| `shutdown /r /t 0` | Restart the computer immediately |
| `systeminfo` | Display detailed system configuration information |

---

## Help and System Information

| Command | Description |
|---------|-------------|
| `help` | Display a list of available commands |
| `<command> /?` | Display help information for a specific command |
| `echo %USERNAME%` | Display current username |
| `echo %COMPUTERNAME%` | Display computer name |
