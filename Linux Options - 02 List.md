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
