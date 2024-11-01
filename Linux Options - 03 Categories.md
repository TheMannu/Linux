List of **Linux Options Categoriy Wise** :

---

### **File and Directory Management**
- **`-a` (All)**: Show all files, including hidden ones.
  - Example: `ls -a` (List all files, including hidden ones).
- **`-l` (Long Listing)**: Show detailed information about files (permissions, size, etc.).
  - Example: `ls -l` (List files with detailed attributes).
- **`-R` (Recursive)**: Recursively list subdirectories.
  - Example: `ls -R` (Recursively list directory contents).
- **`-r` (Reverse)**: Reverse the order of listing.
  - Example: `ls -r` (Reverse the order of file listing).
- **`-h` (Human-Readable)**: Show file sizes in human-readable format.
  - Example: `ls -lh` (Show human-readable file sizes).
- **`-n` (No Overwrite)**: Prevent overwriting of existing files.
  - Example: `cp -n file.txt dir/` (Copy file without overwriting).
- **`-t` (Sort by Time)**: Sort by modification time.
  - Example: `ls -lt` (List files sorted by time).

---

### **File Operations**
- **`-f` (Force)**: Force action, ignoring warnings.
  - Example: `rm -f file.txt` (Forcefully delete file without confirmation).
- **`-i` (Interactive)**: Ask for confirmation before taking action.
  - Example: `rm -i file.txt` (Ask before deleting the file).
- **`-v` (Verbose)**: Show detailed actions being performed.
  - Example: `cp -v file1.txt dir/` (Copy with detailed output).
- **`-p` (Preserve)**: Preserve file attributes.
  - Example: `cp -p file1.txt dir/` (Copy while preserving file attributes).


---

### **Process Management**
- **`-e` (Everything)**: Show all processes.
  - Example: `ps -e` (Display all processes).
- **`-u` (User)**: Show processes for a specific user.
  - Example: `ps -u username` (Show processes owned by a specific user).
- **`-a` (All but TTY)**: Show processes not attached to a terminal.
  - Example: `ps -a` (Show all running processes).
- **`-f` (Full)**: Show a full-format listing of processes.
  - Example: `ps -f` (Display processes with full information).
- **`-o` (Output Format)**: Specify the output format for process information.
  - Example: `ps -o pid,user,command` (Show process ID, user, and command).

---

### **System Information**
- **`-a` (All Information)**: Show all available information.
  - Example: `uname -a` (Display all system information).
- **`-r` (Kernel Release)**: Show the kernel release.
  - Example: `uname -r` (Display the kernel release version).
- **`-s` (Kernel Name)**: Show the kernel name.
  - Example: `uname -s` (Display the kernel name).
- **`-m` (Machine Hardware Name)**: Show the machine hardware name.
  - Example: `uname -m` (Display the machine's hardware architecture).

---

### **Networking**
- **`-i` (Interfaces)**: Display all network interfaces.
  - Example: `ifconfig -i` (Show all network interfaces).
- **`-a` (All Connections)**: Display all network connections.
  - Example: `netstat -a` (Show all active connections).
- **`-n` (Numeric)**: Show numeric addresses instead of resolving names.
  - Example: `netstat -n` (Display numeric IP addresses).
- **`-l` (Listening Ports)**: Show listening ports.
  - Example: `netstat -l` (Display listening ports).
---

### **Archive and Compression**
- **`-c` (Create)**: Create an archive.
  - Example: `tar -cvf archive.tar dir/` (Create a tar archive).
- **`-x` (Extract)**: Extract files from an archive.
  - Example: `tar -xvf archive.tar` (Extract files from a tar archive).
- **`-z` (Gzip Compression)**: Use gzip compression.
  - Example: `tar -zcvf archive.tar.gz dir/` (Create a gzip-compressed archive).
- **`-j` (Bzip2 Compression)**: Use bzip2 compression.
  - Example: `tar -jcvf archive.tar.bz2 dir/` (Create a bzip2-compressed archive).
- **`-t` (List Contents)**: List contents of an archive.
  - Example: `tar -tvf archive.tar` (List the contents of a tar archive).

---

### **Permissions and Ownership**
- **`-R` (Recursive)**: Apply changes recursively to directories and subdirectories.
  - Example: `chmod -R 755 dir/` (Recursively change file permissions).
- **`-v` (Verbose)**: Verbosely show the changes made.
  - Example: `chown -v user:group file.txt` (Change ownership and show details).
- **`-c` (Report Changes)**: Report only when changes are made.
  - Example: `chmod -c 644 file.txt` (Show changes only when the file's permissions are modified).

---

### **System Management**
- **`-h` (Help)**: Show help information for a command.
  - Example: `sudo -h` (Display help for the `sudo` command).
- **`-r` (Reboot)**: Reboot the system.
  - Example: `shutdown -r now` (Reboot the system immediately).
- **`-h now` (Shutdown)**: Shut down the system immediately.
  - Example: `shutdown -h now` (Shut down the system).
