
---

### **Basic Shell Commands**

1. **`echo`**:
   - **Description**: The `echo` command prints text or variables to the terminal or output.
   - **Usage**:
     ```bash
     echo "I am learning"
     echo "My name is $(whoami)"
     ```
     - **Explanation**:
       - `"I am learning"`: This prints the string `"I am learning"`.
       - `$(whoami)`: This uses command substitution to get the current username and prints it.
   - **Common Use**: Displaying messages, variables, or command output within a script.

---

2. **`free`**:
   - **Description**: Displays information about memory usage.
   - **Usage**:
     ```bash
     free -h
     ```
     - **Explanation**:
       - `-h`: Displays memory usage in a human-readable format (e.g., MB, GB).
   - **Common Use**: Checking memory status before running memory-intensive operations in scripts.

---

3. **`grep`**:
   - **Description**: Used to search for specific patterns within text files or outputs.
   - **Usage**:
     ```bash
     grep "search_term" file.txt
     ```
     - **Explanation**:
       - `"search_term"`: The string or pattern you are looking for.
       - `file.txt`: The file to search within.
   - **Common Use**: Searching log files, filtering outputs in scripts, or finding specific lines in files.

---

4. **Piping (`|`)**:
   - **Description**: Pipes take the output of one command and use it as input for another command.
   - **Usage**:
     ```bash
     ps -ef | grep bash
     ```
     - **Explanation**:
       - `ps -ef`: Lists all running processes.
       - `|`: Passes the output of `ps -ef` to the next command.
       - `grep bash`: Filters the processes to only show lines containing "bash".
   - **Common Use**: Combining commands in scripts to process and filter outputs.

---

5. **`df`**:
   - **Description**: Displays information about the file system’s disk space usage.
   - **Usage**:
     ```bash
     df -h
     ```
     - **Explanation**:
       - `-h`: Displays the output in a human-readable format (e.g., GB, MB).
   - **Common Use**: Checking available disk space before installing new software or performing backups.


Shell Scripts, can automate a wide range of tasks such as system administration, file management, and software installation.