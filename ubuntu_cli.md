# Ubuntu CLI Commands Guide

This document provides a structured reference to commonly used commands in the Ubuntu Terminal, useful for navigation, file management, system administration, and troubleshooting.

---

## Navigation Commands

| Command | Description |
|---------|-------------|
| `cd <directory>` | Change directory |
| `cd ..` | Move up one directory level |
| `cd ~/Desktop/Videos` | Navigate into nested directories (~ represents home) |
| `cd ../..` | Move up two directory levels |
| `cd ~` | Go to home directory |
| `cd /` | Go to root directory |
| `pwd` | Print current working directory |
| `TAB` | Auto-complete directory or file names |
| `Ctrl + A` | Move cursor to the start of the command |
| `Ctrl + E` | Move cursor to the end of the command |
| `Ctrl + ←` | Move cursor one word to the left |
| `Ctrl + →` | Move cursor one word to the right |
| `Ctrl + C` | Terminate the current command |
| `Ctrl + Z` | Suspend the current process |
| `↑ / ↓` | Navigate through command history |

---

## Directory Listing and Information

| Command | Description |
|---------|-------------|
| `ls` | List directory contents |
| `ls -l` | List with detailed information (permissions, owner, size, date) |
| `ls -a` | List all files, including hidden files |
| `ls -la` | List all files with detailed information |
| `ls -lh` | List with human-readable file sizes |
| `ls -R` | List contents recursively |
| `tree` | Display directory structure as a tree |
| `du -h` | Show disk usage of current directory |
| `du -sh *` | Show disk usage of each item in current directory |

---

## Creating and Deleting Directories

| Command | Description |
|---------|-------------|
| `mkdir <directory>` | Create a new directory |
| `mkdir -p path/to/directory` | Create directory with parent directories |
| `rmdir <directory>` | Remove an empty directory |
| `rm -r <directory>` | Remove a directory and its contents |
| `rm -rf <directory>` | Force remove directory and contents (use with caution) |

---

## File Operations

| Command | Description |
|---------|-------------|
| `touch <filename>` | Create an empty file or update timestamp |
| `cat <filename>` | Display contents of a file |
| `less <filename>` | View file contents page by page |
| `more <filename>` | View file contents page by page (basic) |
| `head <filename>` | Display first 10 lines of a file |
| `head -n 20 <filename>` | Display first 20 lines of a file |
| `tail <filename>` | Display last 10 lines of a file |
| `tail -f <filename>` | Follow file contents in real-time |
| `nano <filename>` | Edit file with nano text editor |
| `vim <filename>` | Edit file with vim text editor |
| `echo "text" > <filename>` | Create or overwrite file with specified content |
| `echo "text" >> <filename>` | Append content to a file |

---

## File and Directory Management

| Command | Description |
|---------|-------------|
| `cp <source> <destination>` | Copy a file |
| `cp -r <source> <destination>` | Copy a directory recursively |
| `mv <source> <destination>` | Move or rename a file/directory |
| `ln -s <target> <linkname>` | Create a symbolic link |
| `find . -name "*.txt"` | Find files by name pattern |
| `find /path -type f -size +100M` | Find files larger than 100MB |
| `locate <filename>` | Quickly find files by name |
| `which <command>` | Show location of a command |
| `whereis <command>` | Show locations of binary, source, and manual |

---

## File Permissions and Ownership

| Command | Description |
|---------|-------------|
| `chmod 755 <filename>` | Change file permissions (rwxr-xr-x) |
| `chmod +x <filename>` | Make file executable |
| `chmod -x <filename>` | Remove executable permission |
| `chown user:group <filename>` | Change file ownership |
| `chgrp <group> <filename>` | Change group ownership |
| `umask 022` | Set default file permissions |

---

## File Deletion and Cleanup

| Command | Description |
|---------|-------------|
| `rm <filename>` | Remove a file |
| `rm -i <filename>` | Remove file with confirmation prompt |
| `rm -f <filename>` | Force remove file without confirmation |
| `shred -u <filename>` | Securely delete a file |

---

## Archive and Compression

| Command | Description |
|---------|-------------|
| `tar -czf archive.tar.gz <directory>` | Create compressed tar archive |
| `tar -xzf archive.tar.gz` | Extract compressed tar archive |
| `tar -tf archive.tar.gz` | List contents of tar archive |
| `zip -r archive.zip <directory>` | Create zip archive |
| `unzip archive.zip` | Extract zip archive |
| `gzip <filename>` | Compress file with gzip |
| `gunzip <filename.gz>` | Decompress gzip file |

---

## Network and Connectivity

| Command | Description |
|---------|-------------|
| `ping <host>` | Test network connectivity to a host |
| `wget <url>` | Download file from URL |
| `curl <url>` | Transfer data from/to server |
| `ssh user@host` | Connect to remote host via SSH |
| `scp file user@host:/path` | Copy file to remote host |
| `rsync -av source/ destination/` | Synchronize directories |
| `netstat -tuln` | Show listening ports and connections |
| `ss -tuln` | Modern replacement for netstat |
| `iptables -L` | List firewall rules |
| `ufw status` | Check UFW firewall status |

---

## Network Configuration

| Command | Description |
|---------|-------------|
| `ip addr show` | Display network interfaces and IP addresses |
| `ip route show` | Display routing table |
| `ifconfig` | Display/configure network interface (deprecated) |
| `nmcli device status` | Show network device status |
| `nmcli connection show` | Show network connections |
| `systemctl restart networking` | Restart networking service |

---

## Process Management

| Command | Description |
|---------|-------------|
| `ps aux` | Display running processes |
| `ps -ef` | Display all processes with full format |
| `top` | Display running processes in real-time |
| `htop` | Enhanced interactive process viewer |
| `kill <PID>` | Terminate process by process ID |
| `killall <process_name>` | Terminate all processes by name |
| `pkill <pattern>` | Kill processes matching pattern |
| `nohup <command> &` | Run command immune to hangups |
| `jobs` | List active jobs |
| `bg` | Put job in background |
| `fg` | Bring job to foreground |

---

## System Information

| Command | Description |
|---------|-------------|
| `uname -a` | Display system information |
| `lsb_release -a` | Display Ubuntu version information |
| `hostnamectl` | Display hostname and system info |
| `uptime` | Show system uptime and load |
| `whoami` | Display current username |
| `id` | Display user and group IDs |
| `w` | Show who is logged in and what they're doing |
| `last` | Show last logged in users |
| `df -h` | Display filesystem disk usage |
| `free -h` | Display memory usage |
| `lscpu` | Display CPU information |
| `lsblk` | List block devices |
| `lsusb` | List USB devices |
| `lspci` | List PCI devices |

---

## Package Management (APT)

| Command | Description |
|---------|-------------|
| `sudo apt update` | Update package list |
| `sudo apt upgrade` | Upgrade installed packages |
| `sudo apt install <package>` | Install a package |
| `sudo apt remove <package>` | Remove a package |
| `sudo apt purge <package>` | Remove package and configuration files |
| `sudo apt autoremove` | Remove unnecessary packages |
| `apt search <package>` | Search for packages |
| `apt show <package>` | Show package information |
| `apt list --installed` | List installed packages |
| `sudo apt-get clean` | Clean package cache |

---

## Snap Package Management

| Command | Description |
|---------|-------------|
| `snap list` | List installed snap packages |
| `sudo snap install <package>` | Install a snap package |
| `sudo snap remove <package>` | Remove a snap package |
| `snap find <package>` | Search for snap packages |
| `snap info <package>` | Show snap package information |
| `sudo snap refresh` | Update all snap packages |

---

## Service Management (systemd)

| Command | Description |
|---------|-------------|
| `systemctl status <service>` | Check service status |
| `sudo systemctl start <service>` | Start a service |
| `sudo systemctl stop <service>` | Stop a service |
| `sudo systemctl restart <service>` | Restart a service |
| `sudo systemctl enable <service>` | Enable service at boot |
| `sudo systemctl disable <service>` | Disable service at boot |
| `systemctl list-units --type=service` | List all services |
| `journalctl -u <service>` | View service logs |
| `journalctl -f` | Follow system logs in real-time |

---

## Environment Variables and Path

| Command | Description |
|---------|-------------|
| `echo $PATH` | Display PATH environment variable |
| `echo $HOME` | Display home directory path |
| `env` | Display all environment variables |
| `export VAR=value` | Set environment variable |
| `unset VAR` | Remove environment variable |
| `printenv` | Print environment variables |
| `source ~/.bashrc` | Reload bash configuration |

---

## Text Processing

| Command | Description |
|---------|-------------|
| `grep "pattern" <file>` | Search for pattern in file |
| `grep -r "pattern" <directory>` | Search recursively in directory |
| `grep -i "pattern" <file>` | Case-insensitive search |
| `sed 's/old/new/g' <file>` | Replace text in file |
| `awk '{print $1}' <file>` | Print first column of file |
| `sort <file>` | Sort lines in file |
| `uniq <file>` | Remove duplicate lines |
| `wc -l <file>` | Count lines in file |
| `cut -d',' -f1 <file>` | Extract first field from CSV |

---

## File Comparison and Differences

| Command | Description |
|---------|-------------|
| `diff file1 file2` | Compare two files |
| `diff -u file1 file2` | Unified diff format |
| `cmp file1 file2` | Compare files byte by byte |
| `comm file1 file2` | Compare sorted files line by line |

---

## Disk and Storage Management

| Command | Description |
|---------|-------------|
| `fdisk -l` | List all disk partitions |
| `lsblk` | List block devices in tree format |
| `mount` | Display mounted filesystems |
| `sudo mount /dev/sdb1 /mnt` | Mount a filesystem |
| `sudo umount /mnt` | Unmount a filesystem |
| `fsck /dev/sdb1` | Check filesystem for errors |
| `mkfs.ext4 /dev/sdb1` | Format partition with ext4 |

---

## User and Group Management

| Command | Description |
|---------|-------------|
| `sudo adduser <username>` | Add a new user |
| `sudo deluser <username>` | Delete a user |
| `sudo usermod -aG <group> <username>` | Add user to group |
| `groups <username>` | Show groups for user |
| `sudo passwd <username>` | Change user password |
| `su - <username>` | Switch to another user |
| `sudo -u <username> <command>` | Run command as another user |

---

## System Control and Power Management

| Command | Description |
|---------|-------------|
| `sudo shutdown -h now` | Shutdown system immediately |
| `sudo shutdown -r now` | Restart system immediately |
| `sudo reboot` | Restart system |
| `sudo halt` | Halt the system |
| `logout` | Log out current user |
| `exit` | Exit current shell |

---

## Help and Documentation

| Command | Description |
|---------|-------------|
| `man <command>` | Display manual page for command |
| `info <command>` | Display info document for command |
| `<command> --help` | Display help for command |
| `apropos <keyword>` | Search manual pages by keyword |
| `whatis <command>` | Display brief description of command |
| `history` | Display command history |
| `alias` | Display current aliases |
| `type <command>` | Display command type and location |

---

## Advanced Commands

| Command | Description |
|---------|-------------|
| `xargs` | Build and execute commands from standard input |
| `tee <file>` | Write output to both file and stdout |
| `screen` | Terminal multiplexer |
| `tmux` | Modern terminal multiplexer |
| `crontab -e` | Edit user's cron jobs |
| `at now + 1 hour` | Schedule command to run later |
| `watch <command>` | Execute command repeatedly |
| `strace <command>` | Trace system calls |
| `lsof` | List open files |
| `fuser` | Identify processes using files |
