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
