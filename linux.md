# Linux Fundamental 

---
# Linux Basic Commands
## File & Directory Operations
- `ls` – List files and directories
  ```bash

  ```
- `cd` – Change directory
  ```bash

  ```  
- `pwd` – Print working directory
  ```bash

  ```
- `mkdir` – Create a new directory
  ```bash

  ```
- `rmdir` – Remove an empty directory
  ```bash

  ```
- `rm` – Remove files or directories
  ```bash

  ```
- `cp` – Copy files or directories
  ```bash

  ```
- `mv` – Move or rename files or directories
  ```bash

  ```
- `touch` – Create an empty file
  ```bash

  ```
- `cat` – Display file contents
  ```bash

  ```
- `more` / `less` – View file content page by page
  ```bash

  ```
- `head` – Display the first few lines of a file
  ```bash

  ```
- `tail` – Display the last few lines of a file
  ```bash

  ```
- `find` – Search for files in a directory hierarchy
  ```bash

  ```

## File Permissions
- `chmod` – Change file permissions
  ```bash

  ```
- `chown` – Change file owner and group
  ```bash

  ```
- `chgrp` – Change group ownership
  ```bash

  ```


## Process Management
- `ps` – View running processes
  ```bash

  ```
- `top` – Display system tasks in real-time
  ```bash

  ```
- `kill` – Terminate a process by PID
  ```bash

  ```
- `killall` – Terminate processes by name

## System Information
- `uname` – Display system information
  ```bash

  ```
- `df` – Display disk space usage
  ```bash

  ```
-  `du` – Display file and directory space usage
  ```bash

  ```
- `free` – Display memory usage
  ```bash

  ```
- `uptime` – Show how long the system has been running
  ```bash

  ```
- `top` – Show system resource usage
  ```bash

  ```
- `htop` – Interactive system monitor (requires installation)
  ```bash

  ```
  
## Networking
- `ping` – Test network connectivity
  ```bash

  ```
- `ifconfig` – Display network interfaces (older)
  ```bash

  ```
- `ip` – Manage network interfaces (modern replacement for `ifconfig`)
  ```bash

  ```
- `netstat` – Display network connections
  ```bash

  ```
- `curl` – Transfer data from or to a server
  ```bash
  wget https://example.com/file.zip
  ```
- `wget` – Download files from the web
  ```bash
  ssh user@hostname
  ```
- `ssh` – Secure shell access to remote machines
  ```bash
  ssh user@hostname
  ```
- `scp` – Securely copy files between machines
  ```bash
  scp file.txt user@hostname:/path/to/destination
  ```

## Package Management

- `apt-get` – Install, update, and remove packages
  ```bash
  sudo apt-get install package_name
  sudo apt-get update  # Update package list
  sudo apt-get upgrade  # Upgrade installed packages
  ```
- `apt` – Modern package management interface
  ```bash
  sudo apt install package_name
  sudo apt update  # Update package list
  sudo apt upgrade  # Upgrade installed packages
  ```

## Text Processing
- `grep` – Search for patterns in a file
  ```bash
  grep "pattern" file.txt
  ```
- `sort` – Sort lines in a file
  ```bash
  sort file.txt
  ```

## Archiving & Compression
- `tar` – Archive files (with or without compression)
  ```bash
  tar -cvf archive.tar file1 file2  # Create archive
  tar -xvf archive.tar  # Extract archive
  ```
- `gzip` – Compress files
  ```bash
  gzip file.txt
  ```
- `gunzip` – Decompress files
  ```bash
  gunzip file.txt.gz
  ```
- `zip` – Create a zip archive
  ```bash
  zip archive.zip file1 file2
  ```
- `unzip` – Extract a zip archive
  ```bash
  unzip archive.zip
  ```

## File Search
- `find` – Search for files in a directory hierarchy
  ```bash
  find /home/user/ -name "*.txt"
  ```
- `locate` – Quickly find files by name
  ```bash
  locate file.txt
  ```

## User Management
- `useradd` – Add a new user
  ```bash
  sudo useradd user-name
  ```
- `usermod` – Modify user details
  ```bash
  sudo usermod -aG sudo user-name
  ```
- `userdel` – Delete a user
  ```bash
  sudo userdel user-name
  ```
- `passwd` – Change a user password
  ```bash
  sudo passwd user-name
  ```
- `groupadd` – Add a new group
  ```bash
  sudo groupadd group-name
  ```
- `groupdel` – Delete a group
  ```bash
  sudo groupdel group-name
  ```
- `id` – Display user and group IDs
  ```bash
  id user-name
  ```

## System Shutdown & Reboot
- `shutdown` – Shut down or restart the system
  ```bash
  sudo shutdown now  # Shut down immediately
  sudo shutdown -r now  # Restart immediately
  ```
- `reboot` – Reboot the system
  ```bash
  sudo reboot
  ```
- `halt` – Stop the system immediately
  ```bash
  sudo halt
  ```



