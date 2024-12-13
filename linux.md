# Linux Fundamental 

---
## Table of Contents

**[Linux Basic Commands](#linux-basic-commands)**
-  [System Information](#system-information)
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
-  [Others](#others)


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
  <br>
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
    <br>
- `cd` – Change directory
  ```bash
  cd /home/user/Documents
  ```  
  <br>
- `pwd` – Print working directory
  ```bash
  pwd
  ```
  <br>
- `mkdir` – Create a new directory
  ```bash
  mkdir new_folder
  ```
  <br>
- `rmdir` – Remove an empty directory
  ```bash
  rmdir old_folder
  ```
  <br>
- `rm` – Remove files or directories
  ```bash
  rm file.txt
  rm -r directory_name  # To remove a directory
  ```
  <br>
- `cp` – Copy files or directories
  ```bash
  cp file.txt /path/to/destination/
  cp -r folder/ /path/to/destination/  # To copy a directory
  ```
  <br>
- `mv` – Move or rename files or directories
  ```bash
  mv oldfile.txt newfile.txt  # Rename a file
  mv file.txt /path/to/destination/  # Move file
  ```
  <br>
- `touch` – Create an empty file
  ```bash
  touch newfile.txt
  ```
  <br>
- `cat` – Display file contents
  ```bash
  cat file.txt
  ```
  <br>
- `more` / `less` – View file content page by page
  ```bash
  more file.txt
  less file.txt
  ```
  <br>
- `head` – Display the first few lines of a file
  ```bash
  head file.txt
  head -n 10 file.txt  # Display first 10 lines
  ```
  <br>
- `tail` – Display the last few lines of a file
  ```bash
  tail file.txt
  tail -n 10 file.txt  # Display last 10 lines
  ```
  <br>
- `find` – Search for files in a directory hierarchy
  ```bash
  find /home/user/ -name "*.txt"  # Find all .txt files
  ```

## File Permissions
- `chmod` – Change file permissions
  ```bash
  chmod 755 file.txt  # Read, write, and execute for owner; read and execute for others
  ```
  <br>
- `chown` – Change file owner and group
  ```bash
  chown user:group file.txt
  ```
  <br>
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
    <br>
- `ps` – View running processes
  ```bash
  ps aux  # View all running processes
  ```
  <br>
- `top` – Display system tasks in real-time
  ```bash
  top
  ```
  <br>
- `kill` – Terminate a process by PID
  ```bash
  kill 1234  # Terminate process with PID 1234
  ```
  <br>
- `killall` – Terminate processes by name
  ```bash
  killall firefox  # Kill all firefox processes
  ```

  
## System Information
- `uname` – Display system information
  ```bash
  uname -a  # Display all system information
  ```
  <br>
- `df` – Display disk space usage
  ```bash
  df -h  # Human-readable format
  ```
  <br>
- `du` – Display file and directory space usage
  ```bash
  du -sh /path/to/directory
  ```
  <br>
- `free` – Display memory usage
  ```bash
  free -h  # Human-readable format
  ```
  <br>
- `uptime` – Show how long the system has been running
  ```bash
  uptime
  ```
  <br>
- `top` – Show system resource usage
  ```bash
  top
  ```
  <br>
- `htop` – Interactive system monitor (requires installation)
  ```bash
  htop
  ```
  
## Networking
- `ping` – Test network connectivity
  ```bash
  ping google.com
  ```
  <br>
- `ifconfig` – Display network interfaces (older)
  ```bash
  ifconfig
  ```
  <br>
- `ip` – Manage network interfaces (modern replacement for `ifconfig`)
  ```bash
  ip a
  ```
  <br>
- `netstat` – Display network connections
  ```bash
  netstat -tuln  # Show listening ports
  ```
  <br>
- `curl` – Transfer data from or to a server
  ```bash
  curl https://example.com
  ```
  <br>
- `wget` – Download files from the web
  ```bash
  wget https://example.com/file.zip
  ```
  <br>
- `ssh` – Secure shell access to remote machines
  ```bash
  ssh user@hostname( or IP)
  ```
  <br>
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
    <br>
- `apt-get` – Install, update, and remove packages
  ```bash
  sudo apt-get install package_name
  sudo apt-get update  # Update package list
  sudo apt-get upgrade  # Upgrade installed packages
  ```
  <br>
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
  <br>
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
  <br>
- `gzip` – Compress files
  ```bash
  gzip file.txt
  ```
  <br>
- `gunzip` – Decompress files
  ```bash
  gunzip file.txt.gz
  ```
  <br>
- `zip` – Create a zip archive
  ```bash
  zip archive.zip file1 file2
  ```
  <br>
- `unzip` – Extract a zip archive
  ```bash
  unzip archive.zip
  ```

## File Search
- `find` – Search for files in a directory hierarchy
  ```bash
  find /home/user/ -name "*.txt"
  ```
  <br>
- `locate` – Quickly find files by name
  ```bash
  locate file.txt
  ```

## User Management
- `useradd` – Add a new user
  ```bash
  sudo useradd user-name
  ```
  <br>
- `usermod` – Modify user details
  ```bash
  sudo usermod -aG sudo user-name
  ```
  <br>
- `userdel` – Delete a user
  ```bash
  sudo userdel user-name
  ```
  <br>
- `passwd` – Change a user password
  ```bash
  sudo passwd user-name
  ```
  <br>
- `groupadd` – Add a new group
  ```bash
  sudo groupadd group-name
  ```
  <br>
- `groupdel` – Delete a group
  ```bash
  sudo groupdel group-name
  ```
  <br>
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
  <br>
- `reboot` – Reboot the system
  ```bash
  sudo reboot
  ```
  <br>
- `halt` – Stop the system immediately
  ```bash
  sudo halt
  ```

## Others
- `nano` - A text editor for the command line, simpler than `vi`.

  ```bash
  nano filename.txt    # To open text file in nano editor
  ```
<br>      

- `vi` - A powerful text editor used in Unix-based systems. More complex than `nano`.
  ```bash
  vi filename.txt     # To open text file in vi editor
  ```
  Press `i`, then to save and exit, press `Esc`, type `:wq`, and press Enter. <br><br>

- `echo` - Displays a message or value to the terminal.
  ```bash
  echo "Hello, world!"
  ```
  `echo` with user input
  ```bash
  read -p "Enter your name: " name    # read user input & save it in name
  echo "Hello, $name!" 
  ```
<br>

- `man` - Displays the manual page for a command, explaining its usage.
  ```bash
  man ls
  ``` 
<br>

- `alias` - Used to create custom shortcuts for commands.
  ```bash
  alias ll='ls -l' 
  ```
<br>

- `find` - Searches for files and directories in a directory hierarchy.
  ```bash
  find /home/user -name "*.txt"
  ```
<br>

- `adduser` - Adds a new user to the system with interactive prompts.
  ```bash
  sudo adduser newuser
  ```
<br>

- `useradd` - Adds a user, but without interactive prompts (compared to `adduser`).
  ```bash
  sudo useradd -m -s /bin/bash newuser
  ```
<br>

- `visudo` - A safe editor for editing the `/etc/sudoers` file to configure sudo permissions.

  ```bash
  sudo visudo
  ```
<br>

- `ntpdate` - Syncs the system clock with a remote NTP server.
  ```bash
  sudo ntpdate pool.ntp.org
  ```
<br>

- `timedatectl` - Displays and sets the system time and date, as well as time zone information.
  ```bash
  timedatectl
  ```
  Displays the current time, date, and time zone information.

  To set the time zone:
  ```bash
  sudo timedatectl set-timezone America/New_York
  ```
<br>

- `vmstat` - Reports information about system processes, memory, paging, block IO, traps, and CPU activity.

  ```bash
  vmstat 1      # Displays system statistics every second
  ```
<br>

- `glances` - A cross-platform system monitoring tool, providing real-time information about CPU, memory, disk, network, and more.
  ```bash
  glances
  ```
<br>

- `sar` - Collects, reports, and saves system activity information (CPU, memory, IO stats).
  ```bash
  sar -u 1 3       # Displays CPU usage statistics every 1 second, repeated 3 times.
  ```
<br>

- `free` - Displays memory usage (RAM) information.
  ```bash
  free -h #Human readable
  ```
<br>

- `env` - Displays the environment variables of the current session or runs a command in a modified environment.
  ```bash
  env       # Displays all environment variables.
  ```
  To set a temporary environment variable and run a command:
  ```bash
  env VAR=value command  
  ```
  <br>
