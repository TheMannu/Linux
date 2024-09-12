

# **Linux System Administration Commands**

## **1. System Information**

- **Display Kernel and System Information**
  - **Command**: `uname -a`
  - **Description**: Shows detailed system information, including kernel version, architecture, and hostname.

- **View System Uptime**
  - **Command**: `uptime`
  - **Description**: Displays how long the system has been running, the number of users, and load averages.

- **View System Load**
  - **Command**: `top`
  - **Description**: Provides a real-time view of system performance, showing CPU, memory usage, and processes.

- **Monitor CPU Usage**
  - **Command**: `mpstat`
  - **Description**: Displays CPU usage statistics.

- **Monitor Memory Usage**
  - **Command**: `free -h`
  - **Description**: Displays the total, used, and available memory in a human-readable format.

- **View Current Date and Time**
  - **Command**: `date`
  - **Description**: Displays the current system date and time.

- **Show System Boot Time**
  - **Command**: `who -b`
  - **Description**: Displays the last system boot time.

---

## **2. User Session Management**

- **Switch to Root User**
  - **Command**: `sudo -i`
  - **Description**: Switches to the root user’s environment with all its privileges.

- **View User Login History**
  - **Command**: `last`
  - **Description**: Shows the login history of users on the system, including login times and sessions.

- **Show Current Logged-in Users**
  - **Command**: `who`
  - **Description**: Displays information about users currently logged in.

- **Show User Information**
  - **Command**: `id [username]`
  - **Example**: `id john`
  - **Description**: Displays user ID, group ID, and other user information.

---

## **3. Process Management**

- **View Running Processes**
  - **Command**: `ps aux`
  - **Description**: Lists all running processes along with their memory and CPU usage.

- **Kill a Process by ID**
  - **Command**: `kill [PID]`
  - **Example**: `kill 1234`
  - **Description**: Terminates a process by its process ID.

- **Kill a Process by Name**
  - **Command**: `pkill [process_name]`
  - **Example**: `pkill firefox`
  - **Description**: Terminates all processes with the specified name.

- **View Detailed Process Information**
  - **Command**: `htop`
  - **Description**: Provides an interactive, detailed view of running processes with options to sort by CPU or memory usage.

- **Check Process Tree**
  - **Command**: `pstree`
  - **Description**: Displays the process tree, showing the hierarchy of processes.

---

## **4. Disk Usage and File Management**

- **Check Disk Usage**
  - **Command**: `df -h`
  - **Description**: Displays disk usage of all mounted filesystems in a human-readable format.

- **Check Disk Inode Usage**
  - **Command**: `df -i`
  - **Description**: Displays inode usage for each mounted filesystem.

- **Find Large Files**
  - **Command**: `du -ah / | sort -rh | head -n 10`
  - **Description**: Finds and lists the 10 largest files in the system.

- **Check Disk Usage for a Specific Directory**
  - **Command**: `du -h [directory_name]`
  - **Example**: `du -h /home`
  - **Description**: Displays the disk usage for a specific directory.

- **Download a File from a URL**
  - **Command**: `wget [URL]`
  - **Example**: `wget https://example.com/file.zip`
  - **Description**: Downloads files from the internet using the provided URL.

- **Locate a File**
  - **Command**: `locate [filename]`
  - **Example**: `locate file.txt`
  - **Description**: Searches for a file on the system using its name.

- **Create a Directory**
  - **Command**: `mkdir [directory_name]`
  - **Example**: `mkdir myfiles`
  - **Description**: Creates a new directory.

- **Create Multiple Files at Once**
  - **Command**: `touch myfiles/{a.txt,b.txt,c.txt}`
  - **Description**: Creates multiple files in a specified directory in a single command.

- **Delete Files or Directories**
  - **Command**: `rm [file_name]` or `rm -r [directory_name]`
  - **Example**: `rm file.txt` or `rm -r old_folder`
  - **Description**: Deletes files or directories.

---

## **5. Archiving and Compression**

- **Create a tar Archive**
  - **Command**: `tar -cvf [archive_name].tar [file(s)]`
  - **Example**: `tar -cvf archive.tar file1 file2`
  - **Description**: Creates an archive of files without compression.

- **Extract a tar Archive**
  - **Command**: `tar -xvf [archive_name].tar`
  - **Example**: `tar -xvf archive.tar`
  - **Description**: Extracts files from a tar archive.

- **Create a Compressed tar Archive (gzip)**
  - **Command**: `tar -czvf [archive_name].tar.gz [file(s)]`
  - **Example**: `tar -czvf archive.tar.gz file1 file2`
  - **Description**: Creates a compressed archive using gzip.

- **Uncompress and Extract tar.gz Archive**
  - **Command**: `tar -xzvf [archive_name].tar.gz`
  - **Example**: `tar -xzvf archive.tar.gz`
  - **Description**: Extracts files from a compressed tar.gz archive.

- **Compress Files into a zip Archive**
  - **Command**: `zip [archive_name].zip [file(s)]`
  - **Example**: `zip archive.zip file1 file2`
  - **Description**: Compresses files into a zip archive.

- **Extract a zip Archive**
  - **Command**: `unzip [archive_name].zip`
  - **Example**: `unzip archive.zip`
  - **Description**: Extracts files from a zip archive.

---

## **6. System Logs and Auditing**

- **View System Logs**
  - **Command**: `journalctl`
  - **Description**: Displays system logs, including boot, kernel, and service logs.

- **View Real-Time Logs**
  - **Command**: `tail -f /var/log/syslog`
  - **Description**: Displays real-time updates of system logs.

- **Check System Logs**
  - **Command**: `dmesg`
  - **Description**: Prints kernel and system messages, useful for troubleshooting hardware or boot issues.

- **Audit System Changes**
  - **Command**: `auditctl`
  - **Description**: Configures the Linux Audit framework to track system changes like file modifications and access attempts.

---

## **7. Network Management**

- **Check Network Configuration**
  - **Command**: `ifconfig` or `ip a`
  - **Description**: Displays the network interface configuration, including IP addresses and network adapters.

- **Ping an IP Address**
  - **Command**: `ping [IP_address]`
  - **Example**: `ping 8.8.8.8`
  - **Description**: Sends ICMP echo requests to test network connectivity to the specified IP.

- **Ping a Domain Name**
  - **Command**: `ping [domain]`
  - **Example**: `ping google.com`
  - **Description**: Sends ICMP echo requests to test network connectivity to a domain name.

- **Monitor Network Usage**
  - **Command**: `nload`
  - **Description**: Provides a real-time view of incoming and outgoing network traffic.

- **Check Open Ports**
  - **Command**: `netstat -tuln`
  - **Description**: Displays all listening ports and associated services.

- **Trace Route to a Host**
  - **Command**: `traceroute [hostname]`
  - **Example**: `traceroute google.com`
  - **Description**: Traces the route packets take to a specified host.

---

## **8. System Services Management**

- **Check Service Status**
  - **Command**: `systemctl status [service_name]`
  - **Example**: `systemctl status apache2`
  - **Description**: Shows the current status of a specific service.

- **Start a Service**
  - **Command**: `systemctl start [service_name]`
  - **Example**: `systemctl start apache2`
  - **Description**: Starts the specified service.

- **Stop a Service**
  - **Command**: `systemctl stop [service_name]`
  - **Example**: `systemctl stop apache2`
  - **Description**: Stops the specified service.

- **Restart a Service**
  - **Command**: `systemctl restart [service_name]`
  - **Example**: `systemctl restart apache

2`
  - **Description**: Restarts the specified service.

- **Enable Service to Start on Boot**
  - **Command**: `systemctl enable [service_name]`
  - **Example**: `systemctl enable apache2`
  - **Description**: Enables the specified service to start on boot.

- **Disable Service on Boot**
  - **Command**: `systemctl disable [service_name]`
  - **Example**: `systemctl disable apache2`
  - **Description**: Disables the specified service from starting on boot.

---

## **9. Scheduled Tasks**

- **List Scheduled Cron Jobs**
  - **Command**: `crontab -l`
  - **Description**: Lists all scheduled cron jobs for the current user.

- **Edit Cron Jobs**
  - **Command**: `crontab -e`
  - **Description**: Opens the crontab file for editing scheduled tasks.

- **List System-Wide Cron Jobs**
  - **Command**: `cat /etc/crontab`
  - **Description**: Lists all system-wide scheduled tasks.

---

## **10. Package Management**

- **Update Package List**
  - **Command**: `sudo apt-get update`
  - **Description**: Fetches the latest package lists from repositories.

- **Upgrade Installed Packages**
  - **Command**: `sudo apt-get upgrade`
  - **Description**: Upgrades all installed packages to their latest versions.

- **Install a Package**
  - **Command**: `sudo apt-get install [package_name]`
  - **Example**: `sudo apt-get install apache2`
  - **Description**: Installs the specified package.

- **Remove a Package**
  - **Command**: `sudo apt-get remove [package_name]`
  - **Example**: `sudo apt-get remove apache2`
  - **Description**: Removes the specified package.

- **Check Installed Packages**
  - **Command**: `dpkg -l`
  - **Description**: Lists all installed packages on the system.

- **Search for a Package**
  - **Command**: `apt-cache search [package_name]`
  - **Example**: `apt-cache search nginx`
  - **Description**: Searches for packages in the repository.

---

## **Summary of Key Commands**
Organized list of key Linux commands:

### **System Information & Monitoring:**
| Command             | Description                                                      |
|---------------------|------------------------------------------------------------------|
| `uname -a`          | Displays detailed system information.                           |
| `uptime`            | Shows system uptime and load averages.                          |
| `top`               | Real-time system performance and process viewer.                |
| `htop`              | Interactive system performance and process viewer.              |
| `df -h`             | Displays disk usage of mounted filesystems in human-readable form.|
| `df -i`             | Displays inode usage for filesystems.                           |
| `free -h`           | Displays memory usage in human-readable form.                   |
| `ps aux`            | Lists all running processes.                                    |
| `kill [PID]`        | Terminates a process by its ID.                                 |
| `pkill [process_name]`| Terminates processes by name.                                 |
| `mpstat`            | Displays CPU usage statistics.                                  |
| `who -b`            | Shows the last system boot time.                                |
| `dmesg`             | Prints kernel and system messages.                              |
| `journalctl`        | Views system logs.                                              |
| `tail -f /var/log/syslog`| Displays real-time updates of system logs.                 |
| `auditctl`          | Configures the Linux Audit framework.                           |

### **Disk & File Management:**
| Command                         | Description                                                      |
|----------------------------------|------------------------------------------------------------------|
| `mkdir [directory_name]`         | Creates a new directory.                                         |
| `touch myfiles/{a.txt,b.txt,c.txt}`| Creates multiple files at once.                               |
| `rm [file_name]`                 | Deletes files or directories.                                   |
| `du -ah / sort -rh`              | Displays disk usage in human-readable form and sorts by size.    |
| `tar -cvf [archive_name].tar [file(s)]` | Creates a tar archive.                                 |
| `tar -xvf [archive_name].tar`    | Extracts files from a tar archive.                              |
| `tar -czvf [archive_name].tar.gz [file(s)]` | Creates a compressed tar.gz archive.                |
| `tar -xzvf [archive_name].tar.gz`| Extracts files from a tar.gz archive.                           |
| `zip [archive_name].zip [file(s)]` | Compresses files into a zip archive.                          |
| `unzip [archive_name].zip`       | Extracts files from a zip archive.                              |
| `locate [filename]`              | Searches for a file on the system.                              |
| `wget [URL]`                     | Downloads files from the internet.                              |

### **Network Management:**
| Command             | Description                                                      |
|---------------------|------------------------------------------------------------------|
| `ifconfig` or `ip a`| Displays network configuration.                                  |
| `ping [IP_address]`  | Tests network connectivity to an IP address.                    |
| `ping [domain]`      | Tests network connectivity to a domain.                         |
| `nload`             | Monitors network traffic in real-time.                           |
| `netstat -tuln`     | Displays listening ports and associated services.                |
| `traceroute [hostname]`| Traces the route packets take to a host.                      |

### **System Services Management:**
| Command                           | Description                                                      |
|------------------------------------|------------------------------------------------------------------|
| `systemctl status [service_name]`  | Shows the status of a system service.                            |
| `systemctl start [service_name]`   | Starts a system service.                                         |
| `systemctl stop [service_name]`    | Stops a system service.                                          |
| `systemctl restart [service_name]` | Restarts a system service.                                       |
| `systemctl enable [service_name]`  | Enables a service to start on boot.                              |
| `systemctl disable [service_name]` | Disables a service from starting on boot.                        |

### **Task Scheduling & Logs:**
| Command             | Description                                                      |
|---------------------|------------------------------------------------------------------|
| `crontab -l`        | Lists scheduled cron jobs for the current user.                  |
| `crontab -e`        | Edits the crontab file for scheduled tasks.                      |
| `cat /etc/crontab`  | Lists system-wide scheduled tasks.                               |

### **Package Management:**
| Command                              | Description                                                      |
|--------------------------------------|------------------------------------------------------------------|
| `sudo apt-get update`                | Updates the package list (minor update).                         |
| `sudo apt-get upgrade`               | Upgrades installed packages (major update).                      |
| `sudo apt-get install [package_name]`| Installs a package.                                              |
| `sudo apt-get remove [package_name]` | Removes a package.                                               |
| `dpkg -l`                            | Lists installed packages.                                        |
| `apt-cache search [package_name]`    | Searches for packages in the repository.                         |

