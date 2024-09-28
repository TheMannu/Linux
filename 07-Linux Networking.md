# Linux Networking Commands

Linux provides a wide range of networking tools to configure, monitor, and troubleshoot network interfaces. Essential Linux networking commands.

---

## 1. Viewing Network Configuration

- **Check IP Address**  
  - **Command**: `ip addr`  
  - **Description**: Displays all IP addresses and related interface details on the system.
  
- **View Network Interfaces**  
  - **Command**: `ifconfig`  
  - **Description**: Shows the network interfaces and their statuses. Deprecated in newer versions of Linux, where `ip` command is preferred.

- **View Link Status**  
  - **Command**: `ifplugstatus`  
  - **Description**: Checks the link status (whether the network cable is plugged in or not) of network interfaces.
  
- **View Routing Table**  
  - **Command**: `route -n`  
  - **Description**: Displays the routing table in numeric format.

- **Check Active Connections**  
  - **Command**: `netstat -tuln`  
  - **Description**: Lists all listening ports and active network connections. `netstat` is deprecated, so `ss` is the modern replacement.

- **Check Active Connections (Alternative)**  
  - **Command**: `ss -tuln`  
  - **Description**: Displays detailed socket statistics, including open TCP and UDP connections. Preferred over `netstat`.

---

## 2. Configuring Network Interfaces

- **Bring an Interface Up**  
  - **Command**: `ifconfig [interface] up`  
  - **Example**: `sudo ifconfig eth0 up`  
  - **Description**: Brings a network interface (e.g., eth0) online.
  
- **Bring an Interface Down**  
  - **Command**: `ifconfig [interface] down`  
  - **Example**: `sudo ifconfig eth0 down`  
  - **Description**: Takes a network interface (e.g., eth0) offline.

- **Assign IP Address to an Interface**  
  - **Command**: `ip addr add [IP address] dev [interface]`  
  - **Example**: `sudo ip addr add 192.168.1.100/24 dev eth0`  
  - **Description**: Assigns an IP address to a network interface.

---

## 3. Network Diagnostics and Troubleshooting

- **Ping a Host**  
  - **Command**: `ping [hostname/IP]`  
  - **Example**: `ping google.com`  
  - **Description**: Sends ICMP echo requests to test network connectivity to a host.

- **Trace Network Path**  
  - **Command**: `traceroute [hostname/IP]`  
  - **Example**: `traceroute google.com`  
  - **Description**: Shows the path packets take to reach a network destination.

- **Check Port Connectivity**  
  - **Command**: `nc -zv [hostname/IP] [port]`  
  - **Example**: `nc -zv google.com 80`  
  - **Description**: Verifies if a TCP port on a host is open.

- **Run Network Diagnostic**  
  - **Command**: `mtr [hostname]`  
  - **Example**: `mtr google.com`  
  - **Description**: Combines the functionality of `ping` and `traceroute` to provide a detailed analysis of network path performance over time.

- **Get Domain Name Information**  
  - **Command**: `whois [domain]`  
  - **Example**: `whois example.com`  
  - **Description**: Queries information about domain ownership, expiration, and registration details.

---

## 4. Network Monitoring

- **Monitor Network Traffic (Real-time)**  
  - **Command**: `iftop`  
  - **Description**: Provides real-time monitoring of network bandwidth usage per interface.

- **View Network Usage by Process**  
  - **Command**: `nethogs`  
  - **Description**: Displays bandwidth usage per process or application.

---

## 5. DNS and Hostname Resolution

- **Check DNS Information**  
  - **Command**: `dig [hostname]`  
  - **Example**: `dig google.com`  
  - **Description**: Queries DNS servers for information about a domain name.

- **Lookup Hostname**  
  - **Command**: `nslookup [hostname]`  
  - **Example**: `nslookup google.com`  
  - **Description**: Queries DNS to resolve the IP address of a hostname.

---

## 6. Managing Hostnames

- **View Hostname**  
  - **Command**: `hostname`  
  - **Description**: Displays the current hostname of the system.

- **View Hostname Information**
  - **Command:** `hostnamectl`
  - **Example:** `hostnamectl`
  - **Description:** Displays detailed information about the system's hostname, including static and transient hostnames, as well as related metadata like the operating system and kernel version.
  
- **Set Hostname**  
  - **Command**: `hostnamectl set-hostname [new-hostname]`  
  - **Example**: `sudo hostnamectl set-hostname my-server`  
  - **Description**: Changes the system’s hostname.

---

## 7. Network Configuration Files

- **`/etc/network/interfaces`**  
  - **Description**: Contains network interface configuration on Debian-based systems. Used to configure static IPs, gateways, and DNS servers.

- **`/etc/hostname`**  
  - **Description**: Stores the system’s hostname.

- **`/etc/hosts`**  
  - **Description**: Maps IP addresses to hostnames. Used for local DNS resolution.

- **`/etc/resolv.conf`**  
  - **Description**: Contains DNS server information for the system.

---

## 8. Network Services

- **Start Network Service**  
  - **Command**: `systemctl start networking`  
  - **Description**: Starts the network service on the system.

- **Restart Network Service**  
  - **Command**: `systemctl restart networking`  
  - **Description**: Restarts the network service to apply configuration changes.

- **Check Status of Network Service**  
  - **Command**: `systemctl status networking`  
  - **Description**: Displays the current status of the network service.

---

## 9. Network File Transfers

- **Download File via HTTP/FTP**  
  - **Command**: `wget [URL]`  
  - **Example**: `wget https://example.com/file.zip`  
  - **Description**: Downloads files from the web using HTTP, HTTPS, or FTP protocols.

- **Transfer Files via SCP**  
  - **Command**: `scp [source] [user]@[host]:[destination]`  
  - **Example**: `scp file.txt user@192.168.1.100:/home/user/`  
  - **Description**: Copies files from one host to another using SSH.

---

## 10. Miscellaneous Commands

- **Check External IP Address**  
  - **Command**: `curl ifconfig.me`  
  - **Description**: Retrieves the public IP address of your machine.

- **Flush DNS Cache**  
  - **Command**: `systemd-resolve --flush-caches`  
  - **Description**: Clears the system's DNS cache.

---

## Summary of Key Commands

| Command                      | Description                                      |
|------------------------------|--------------------------------------------------|
| `ip addr`                    | Shows IP addresses and network interfaces.       |
| `ifconfig`                   | Displays network interface configurations.       |
| `ping`                       | Tests network connectivity to a host.            |
| `traceroute`                 | Traces the path to a network destination.        |
| `netstat`                    | Lists open connections and listening ports.      |
| `ss`                         | Displays socket statistics (modern replacement for `netstat`). |
| `iftop`                      | Monitors network traffic in real-time.           |
| `mtr`                        | Provides real-time network diagnostics.          |
| `whois`                      | Queries domain name information.                 |
| `dig`                        | Queries DNS for domain name information.         |
| `hostnamectl set-hostname`   | Sets the system's hostname.                      |
| `wget`                       | Downloads files from a URL.                      |
| `scp`                        | Securely copies files between hosts.             |
| `ifplugstatus`               | Checks network cable link status.                |

---

This guide covers all essential networking commands in Linux, providing you with the tools necessary to configure, diagnose, and monitor network settings effectively.
