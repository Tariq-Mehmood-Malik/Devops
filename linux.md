# Linux Fundamental 

---
# Linux Basic Commands
## File & Directory Operations
- `ls` – List files and directories
  ```bash
  ls
  ```
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
-  `du` – Display file and directory space usage
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



