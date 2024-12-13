# Linux Fundamental 

---
## Table of Contents

**[Linux Basic Commands](#linux-basic-commands)**
-  [Sysytem Information](#sysytem-information)
-  [File & Directory Operations](#file--directory-operations)
-  [File Permissions](#file-permissions)
-  [Process Management](#process-management)
-  [System Information](#system-information)
-  [Networking](#networking)
-  [Package Management](#package-management)
-  [Text Processing](#text-processing)
-  [Archiving & Compression](#archiving--compression)
-  [File Search](#file-search)
-  [User Management](#user-management)
-  [System Shutdown & Reboot](#system-shutdown--reboot)


# Linux Basic Commands
## System Information
- `hostname`
  Displays or sets the system's hostname.
  ```bash
  hostname
  ```     
  To set a new hostname:    
  ```bash
  sudo hostname new-hostname
  ```
- `whoami`
  Displays the current logged-in user's name.
  ```bash
  whoami
  ```




## File & Directory Operations
- `ls` – List files and directories
- `ls -l`: Lists files in long format, showing permissions, owner, size, etc.
- `ls -a`: Shows hidden files (those starting with `.`).
- `ls -lh`: Lists files with human-readable sizes.
- `ls -R`: Recursively lists subdirectories.
- `ls -la`: Combines `-l` and `-a`.
- `cd` – Change directory
  ```bash
  cd /home/user/Documents
  ```  
- `pwd` – Print working directory
  ```bash
  pwd
  ```
- `mkdir` – Create a new directory
  ```bash
  mkdir new_folder
  ```
- `rmdir` – Remove an empty directory
  ```bash
  rmdir old_folder
  ```
- `rm` – Remove files or directories
  ```bash
  rm file.txt
  rm -r directory_name  # To remove a directory
  ```
- `cp` – Copy files or directories
  ```bash
  cp file.txt /path/to/destination/
  cp -r folder/ /path/to/destination/  # To copy a directory
  ```
- `mv` – Move or rename files or directories
  ```bash
  mv oldfile.txt newfile.txt  # Rename a file
  mv file.txt /path/to/destination/  # Move file
  ```
- `touch` – Create an empty file
  ```bash
  touch newfile.txt
  ```
- `cat` – Display file contents
  ```bash
  cat file.txt
  ```
- `more` / `less` – View file content page by page
  ```bash
  more file.txt
  less file.txt
  ```
- `head` – Display the first few lines of a file
  ```bash
  head file.txt
  head -n 10 file.txt  # Display first 10 lines
  ```
- `tail` – Display the last few lines of a file
  ```bash
  tail file.txt
  tail -n 10 file.txt  # Display last 10 lines
  ```
- `find` – Search for files in a directory hierarchy
  ```bash
  find /home/user/ -name "*.txt"  # Find all .txt files
  ```

## File Permissions
- `chmod` – Change file permissions
  ```bash
  chmod 755 file.txt  # Read, write, and execute for owner; read and execute for others
  ```
- `chown` – Change file owner and group
  ```bash
  chown user:group file.txt
  ```
- `chgrp` – Change group ownership
  ```bash
  chgrp group file.txt
  ```


## Process Management
- `systemctl` - Used to examine and control the systemd system and service manager. It can start, stop, enable, disable, and check the status of system services.
    To check the status of a service:
    ```bash
    systemctl status apache2
    ```
    To start a service:
    ```bash
    sudo systemctl start apache2
    ```
    To enable a service at boot:
    ```bash
    sudo systemctl enable apache2
    ```
- `ps` – View running processes
  ```bash
  ps aux  # View all running processes
  ```
- `top` – Display system tasks in real-time
  ```bash
  top
  ```
- `kill` – Terminate a process by PID
  ```bash
  kill 1234  # Terminate process with PID 1234
  ```
- `killall` – Terminate processes by name
  ```bash
  killall firefox  # Kill all firefox processes
  ```
  
## System Information
- `uname` – Display system information
  ```bash
  uname -a  # Display all system information
  ```
- `df` – Display disk space usage
  ```bash
  df -h  # Human-readable format
  ```
- `du` – Display file and directory space usage
  ```bash
  du -sh /path/to/directory
  ```
- `free` – Display memory usage
  ```bash
  free -h  # Human-readable format
  ```
- `uptime` – Show how long the system has been running
  ```bash
  uptime
  ```
- `top` – Show system resource usage
  ```bash
  top
  ```
- `htop` – Interactive system monitor (requires installation)
  ```bash
  htop
  ```
  
## Networking
- `ping` – Test network connectivity
  ```bash
  ping google.com
  ```
- `ifconfig` – Display network interfaces (older)
  ```bash
  ifconfig
  ```
- `ip` – Manage network interfaces (modern replacement for `ifconfig`)
  ```bash
  ip a
  ```
- `netstat` – Display network connections
  ```bash
  netstat -tuln  # Show listening ports
  ```
- `curl` – Transfer data from or to a server
  ```bash
  curl https://example.com
  ```
- `wget` – Download files from the web
  ```bash
  wget https://example.com/file.zip
  ```
- `ssh` – Secure shell access to remote machines
  ```bash
  ssh user@hostname( or IP)
  ```
- `scp` – Securely copy files between machines
  ```bash
  scp file.txt user@hostname(or IP):/path/to/destination
  ```

## Package Management

- `dpkg -i name.deb` - Installs a `.deb` package file.
  
    ```bash
    sudo dpkg -i example-package.deb
    ```     
    If there are dependency issues, you can resolve them with:
    ```bash
    sudo apt-get install -f
    ```
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

## Others


