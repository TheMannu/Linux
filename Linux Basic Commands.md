Here's a merged, expanded, and organized list of basic Linux commands. Redundant commands have been removed, additional options have been included, and formatting has been improved.

### Basic Linux Commands

- **`ls`**: List directory contents.
  - Example: `ls` (lists files in the current directory)
  - Example: `ls -a` (lists all files including hidden ones)
  - Example: `ls -lrt` (lists files sorted by modification time, oldest first, long format)

- **`cd`**: Change the directory.
  - Example: `cd /` (changes to the root directory)
  - Example: `cd ~` (changes to the home directory)

- **`pwd`**: Print working directory.
  - Example: `pwd` (prints the current directory path)

- **`cp`**: Copy files and directories.
  - Example: `cp file1 file2` (copies file1 to file2)
  - Example: `cp -r dir1 dir2` (copies directory dir1 to dir2 recursively)

- **`mv`**: Move or rename files and directories.
  - Example: `mv file1 file2` (renames file1 to file2 or moves file1 to file2)
  - Example: `mv dir1 dir2` (moves directory dir1 to dir2)

- **`rm`**: Remove files or directories.
  - Example: `rm file` (removes the file named file)
  - Example: `rm -r dir` (removes directory dir and its contents)

- **`mkdir`**: Create a new directory.
  - Example: `mkdir new_directory` (creates a directory named new_directory)
  - Example: `mkdir -p parent/child` (creates parent and child directories)

- **`rmdir`**: Remove an empty directory.
  - Example: `rmdir empty_directory` (removes an empty directory named empty_directory)

- **`chmod`**: Change file permissions.
  - Example: `chmod 755 file` (sets the permissions of file to rwxr-xr-x)
  - Example: `chmod -R 755 dir` (recursively sets permissions for directory dir)

- **`chown`**: Change file ownership.
  - Example: `chown user:group file` (changes the owner and group of file)
  - Example: `chown -R user:group dir` (recursively changes ownership of directory dir)

- **`ps`**: Display currently running processes.
  - Example: `ps` (lists processes running in the current shell)
  - Example: `ps aux` (lists all processes for all users)

- **`top`**: Display real-time system information.
  - Example: `top` (shows a dynamic real-time view of system processes)

- **`htop`**: Interactive process viewer (enhanced `top`).
  - Example: `htop` (interactive display of processes with more functionality than `top`)

- **`kill`**: Send a signal to a process, often used to terminate it.
  - Example: `kill 1234` (terminates process with PID 1234)
  - Example: `kill -9 1234` (forcefully kills process 1234)

- **`man`**: Show the manual for a command.
  - Example: `man ls` (shows the manual page for the `ls` command)
  - Example: `man -k keyword` (searches for commands related to keyword)

- **`touch`**: Create an empty file or update the timestamp of an existing file.
  - Example: `touch file` (creates or updates file)

- **`cat`**: Concatenate and display the content of a file.
  - Example: `cat file` (displays the content of file)
  - Example: `cat -n file` (numbers all output lines)

- **`more`**: Display the content of a file one screen at a time.
  - Example: `more file` (views file content page by page)

- **`less`**: Similar to `more`, but with more features.
  - Example: `less file` (views file content with the ability to scroll backwards)
  - Example: `less +F file` (follows the file as it grows, similar to `tail -f`)

- **`head`**: Display the first 10 lines of a file.
  - Example: `head file` (shows the first 10 lines of file)
  - Example: `head -n 20 file` (shows the first 20 lines of file)

- **`tail`**: Display the last 10 lines of a file.
  - Example: `tail file` (shows the last 10 lines of file)
  - Example: `tail -f file` (follows the file as it grows)

- **`find`**: Search for files and directories within a directory.
  - Example: `find /path -name filename` (searches for filename in /path)
  - Example: `find /path -type f -name "*.txt"` (finds all .txt files)

- **`locate`**: Search for files by name in the system’s file database.
  - Example: `locate filename` (finds files with name filename)
  - Example: `locate -i filename` (case-insensitive search)

- **`grep`**: Search for a specific pattern in a file.
  - Example: `grep 'pattern' file` (searches for 'pattern' in file)
  - Example: `grep -r 'pattern' /dir` (recursively searches for 'pattern' in /dir)

- **`awk`**: A powerful text-processing language.
  - Example: `awk '{print $1}' file` (prints the first column of each line in file)

- **`sed`**: Stream editor for filtering and transforming text.
  - Example: `sed 's/old/new/g' file` (replaces 'old' with 'new' globally in file)

- **`hostname`**: Displays the name of the host or the Linux distribution.
  - Example: `hostname` (shows the hostname of the system)
  - Example: `hostname -i` (shows the IP address associated with the hostname)

- **`whoami`**: Shows the currently logged-in user.
  - Example: `whoami` (prints the current user name)

- **`clear`**: Clears the terminal screen.
  - Example: `clear` (clears all text on the terminal screen)

- **`su`**: Switch to another user account.
  - Example: `su root` (switches to the root user account)

- **`sudo`**: Execute a command as another user, usually root.
  - Example: `sudo command` (runs command as root)
  - Example: `sudo -u username command` (runs command as the specified user)

- **`history`**: Displays a list of previously entered commands.
  - Example: `history` (lists command history)
  - Example: `!n` (re-executes command number n from history)

- **`stat`**: Displays detailed information (timestamp, size, etc.) about a file.
  - Example: `stat file` (shows detailed information about file)

- **`curl`**: Transfer data from or to a server using various protocols.
  - Example: `curl ifconfig.me` (shows the public IP address)
  - Example: `curl -O https://example.com/file` (downloads file from URL)

- **`wget`**: Download files from the web.
  - Example: `wget https://example.com/file` (downloads file from URL)

- **`scp`**: Securely copy files between hosts over SSH.
  - Example: `scp file user@host:/path/to/destination` (copies file to remote host)

- **`ssh`**: Securely connect to a remote system over SSH.
  - Example: `ssh user@host` (connects to the remote host as user)

- **`uname`**: Show system information.
  - Example: `uname` (shows system name)
  - Example: `uname -a` (shows all available system information)

- **`free`**: Displays memory usage.
  - Example: `free` (shows memory usage in kilobytes)
  - Example: `free -h` (shows memory usage in human-readable format)

- **`df`**: Display disk space usage.
  - Example: `df -h` (shows disk space usage in human-readable format)

- **`du`**: Estimate file space usage.
  - Example: `du -h dir` (shows disk usage for all files and directories in human-readable format)

- **`ifconfig`**: Displays network interface information (deprecated, use `ip` instead).
  - Example: `ifconfig` (shows network interface configuration)

- **`ip`**: Show/manipulate routing, devices, and tunnels.
  - Example: `ip addr show` (shows IP address information)
  - Example: `ip route show` (shows routing table)

- **`cat /etc/os-release`**: Displays OS version information.
  - Example: `cat /etc/os-release` (shows OS version and details)

- **`ping`**: Test connectivity to another host.
  - Example: `ping google.com` (sends ICMP echo requests to google.com)

- **`traceroute`**:

 Trace the path packets take to a network host.
  - Example: `traceroute google.com` (shows the route packets take to reach google.com)

- **`netstat`**: Displays network connections, routing tables, interface statistics (deprecated, use `ss`).
  - Example: `netstat -plnt` (shows active listening ports and associated programs)

- **`ss`**: Displays detailed network statistics.
  - Example: `ss -tuln` (shows active listening ports)
  
- **`reboot`**: Restart the system.
  - Example: `sudo reboot` (restarts the system)

- **`shutdown`**: Power off or restart the system.
  - Example: `sudo shutdown now` (immediately shuts down the system)
  - Example: `sudo shutdown -r now` (reboots the system)

This list contains commands for managing files, processes, system information, and networking, organized for easier reference.
