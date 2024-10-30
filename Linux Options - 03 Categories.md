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
