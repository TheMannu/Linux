List of common options used with Linux commands, along with examples and explanations.

---

### 1. **`-a` (All)**
   - **Explanation**: Displays all files, including hidden ones.
   - **Examples**:
     - `ls -a`: Lists all files, including hidden ones (those starting with `.`).
     - `ps -a`: Displays all processes running for all users.

---

### 2. **`-l` (Long Format)**
   - **Explanation**: Displays detailed information, typically in a long format.
   - **Examples**:
     - `ls -l`: Lists files with detailed attributes (permissions, ownership, timestamps).
     - `ps -l`: Displays processes in long format with additional details.

---

### 3. **`-r` (Recursive)**
   - **Explanation**: Recursively applies a command to directories and subdirectories.
   - **Examples**:
     - `rm -r folder`: Deletes a folder and all its contents recursively.
     - `cp -r dir1 dir2`: Copies a directory and all its contents recursively.

---

### 4. **`-f` (Force)**
   - **Explanation**: Forces an action without prompting or confirmation.
   - **Examples**:
     - `rm -f file.txt`: Forces file deletion without asking for confirmation.
     - `cp -f source.txt dest.txt`: Forcefully overwrites `dest.txt`.

---

### 5. **`-v` (Verbose)**
   - **Explanation**: Shows detailed output of the command's actions.
   - **Examples**:
     - `cp -v source.txt dest.txt`: Verbosely copies the file, showing details.
     - `tar -cvf archive.tar folder`: Verbosely creates an archive, listing all files being added.

---

### 6. **`-i` (Interactive)**
   - **Explanation**: Prompts for confirmation before taking actions.
   - **Examples**:
     - `rm -i file.txt`: Prompts for confirmation before deleting the file.
     - `cp -i source.txt dest.txt`: Asks for confirmation before overwriting `dest.txt`.

---

### 7. **`-n` (No Overwrite)**
   - **Explanation**: Prevents overwriting of existing files.
   - **Examples**:
     - `cp -n file1.txt dir/`: Copy `file1.txt` to `dir/` without overwriting any existing files.

---

### 8. **`-h` (Human-Readable)**
   - **Explanation**: Displays file sizes in a human-readable format (e.g., KB, MB, GB).
   - **Examples**:
     - `ls -lh`: Lists files with human-readable sizes.
     - `df -h`: Displays disk space usage in a human-readable format.

---

### 9. **`-t` (Sort by Time)**
   - **Explanation**: Sorts results by modification time.
   - **Examples**:
     - `ls -lt`: Lists files sorted by modification time.
     - `ps -t`: Displays processes sorted by the time they were started.

---

### 10. **`-u` (User)**
   - **Explanation**: Specifies or shows information related to users.
   - **Examples**:
     - `ps -u username`: Displays processes owned by a specific user.
     - `chown -u username file.txt`: Changes the ownership of `file.txt` to a specific user.

---

### 11. **`-p` (Process or PID)**
   - **Explanation**: Works with Process IDs (PIDs) in commands related to processes.
   - **Examples**:
     - `kill -p 1234`: Kills the process with the specified PID.
     - `ps -p 1234`: Displays details for a specific process by PID.

---

### 12. **`-g` (Group)**
   - **Explanation**: Specifies or changes group-related information.
   - **Examples**:
     - `ps -g`: Displays processes grouped by session ID.
     - `chgrp -g groupname file.txt`: Changes the group ownership of `file.txt`.

---

### 13. **`-d` (Directory)**
   - **Explanation**: Applies the command to directories or displays directory-specific information.
   - **Examples**:
     - `ls -d`: Lists only directories.
     - `find . -type d`: Finds directories recursively starting from the current directory.
