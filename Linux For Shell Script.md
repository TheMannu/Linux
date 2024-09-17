
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

---

6. **Arithmetic Operations**:
   - **Description**: Basic arithmetic operations can be done directly in shell scripts.
   - **Usage**:
     ```bash
     ((sum=10+5))
     echo $sum
     ```
     - **Explanation**:
       - `((sum=10+5))`: Adds the values `10` and `5` and stores the result in the variable `sum`.
       - `echo $sum`: Prints the value of `sum`.
   - **Common Use**: Performing calculations in scripts.

---

7. **Variables**:
   - **Description**: Variables store data that can be reused in a script.
   - **Usage**:
     ```bash
     SOMEVAR="text stuff I am learning"
     echo "$SOMEVAR"
     ```
     - **Explanation**:
       - `SOMEVAR="text stuff I am learning"`: Assigns the value to the variable `SOMEVAR`.
       - `echo "$SOMEVAR"`: Prints the value of `SOMEVAR`.
   - **Common Use**: Storing and reusing values in scripts.

---

8. **Executing Shell Scripts**:
   - **Description**: You can execute a shell script using `sh` or by marking it as executable.
   - **Usage**:
     ```bash
     sh script.sh  # Runs the script with the `sh` command
     ./script.sh   # Runs the script if it is executable
     ```
     - **Explanation**:
       - `sh script.sh`: Executes the script using the `sh` command.
       - `./script.sh`: Runs the script directly if it's marked as executable (`chmod +x script.sh`).
   - **Common Use**: Running shell scripts from the command line.

---

### **Additional Commands for Shell Scripts**

9. **`if` Statements**:
   - **Description**: Conditional execution based on conditions.
   - **Usage**:
     ```bash
     if [ "$USER" == "root" ]; then
       echo "You are root"
     else
       echo "You are not root"
     fi
     ```
     - **Explanation**:
       - `[ "$USER" == "root" ]`: Checks if the current user is "root".
       - `then`: Executes the following commands if the condition is true.
       - `else`: Executes the commands if the condition is false.
   - **Common Use**: Conditional checks for variables, commands, or statuses in scripts.


Shell Scripts, can automate a wide range of tasks such as system administration, file management, and software installation.