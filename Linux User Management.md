
### **Linux User Management**

Managing users, groups, and permissions in Linux is essential for maintaining system security and ensuring proper access control. Below is a comprehensive guide to managing users in Linux, along with relevant configuration files and additional commands.

---

### **1. Managing Users**

- **Add a User**  
  - **Command**: `adduser [username]`  
  - **Example**: `sudo adduser john`  
  - **Description**: Creates a new user with a home directory, a default shell, and prompts for a password.

- **Create a User and Add to Existing Group**  
  - **Command**: `adduser [username] [groupname]`  
  - **Example**: `sudo adduser john developers`  
  - **Description**: Creates a new user and directly adds them to an existing group.

- **Delete a User**  
  - **Command**: `userdel [username]`  
  - **Example**: `sudo userdel john`  
  - **Description**: Deletes a user from the system without removing their home directory.

- **Delete User and Home Directory**  
  - **Command**: `sudo deluser --remove-home john`  
  - **Description**: Deletes the user and removes their home directory.

- **Modify a User**  
  - **Command**: `usermod [options] [username]`  
  - **Example**: `sudo usermod -aG sudo john`  
  - **Description**: Modifies user properties, such as adding the user to a group, changing the home directory, or the shell.

- **List All Users**  
  - **Command**: `cat /etc/passwd`  
  - **Description**: Lists all users on the system, showing details like username, UID, GID, home directory, and default shell.

---

### **2. User Information and Status**

- **View Current User**  
  - **Command**: `whoami`  
  - **Description**: Displays the current logged-in user's name.

- **View User Information**  
  - **Command**: `id [username]`  
  - **Example**: `id john`  
  - **Description**: Displays UID, GID, and group memberships of the user.

- **Show Currently Logged-in Users**  
  - **Command**: `who`  
  - **Description**: Lists users currently logged into the system.

---

### **3. Password Management**

- **Change User Password**  
  - **Command**: `passwd [username]`  
  - **Example**: `sudo passwd john`  
  - **Description**: Changes the password for a specified user.

- **Expire User Password (Force Password Change)**  
  - **Command**: `passwd -e [username]`  
  - **Example**: `sudo passwd -e john`  
  - **Description**: Forces the user to change their password at the next login.

- **Set Password Expiration (Chage)**  
  - **Command**: `chage [username]`  
  - **Example**: `sudo chage john`  
  - **Description**: Manages password expiration and aging for a user, such as setting expiry dates.

---

### **4. Group Management**

- **Create a Group**  
  - **Command**: `addgroup [groupname]`  
  - **Example**: `sudo addgroup developers`  
  - **Description**: Creates a new group.

- **Add User to Group**  
  - **Command**: `usermod -aG [groupname] [username]`  
  - **Example**: `sudo usermod -aG developers john`  
  - **Description**: Adds a user to the specified group.

- **Remove User from Group**  
  - **Command**: `gpasswd -d [username] [groupname]`  
  - **Example**: `sudo gpasswd -d john developers`  
  - **Description**: Removes a user from a group.

- **List Group Membership**  
  - **Command**: `groups [username]`  
  - **Example**: `groups john`  
  - **Description**: Lists the groups a user belongs to.

- **List All Groups**  
  - **Command**: `cat /etc/group`  
  - **Description**: Lists all groups on the system.

- **View Group Information**  
  - **Command**: `getent group [groupname]`  
  - **Example**: `getent group developers`  
  - **Description**: Retrieves information about a specific group.

- **Delete a Group**  
  - **Command**: `delgroup [groupname]`  
  - **Example**: `sudo delgroup developers`  
  - **Description**: Removes a group from the system.

---

### **5. User Account Configuration Files**

- **`/etc/passwd`**:  
  Contains basic user account information, including username, UID, GID, home directory, and login shell.

- **`/etc/shadow`**:  
  Stores encrypted passwords and password-related information, such as password expiration and aging policies.

- **`/etc/group`**:  
  Contains group information, including group names, GIDs, and group members.

- **`/etc/sudoers`**:  
  Controls which users have administrative privileges and can use the `sudo` command to execute commands as root.

---

### **6. Account Locking and Expiration**

- **Lock a User Account**  
  - **Command**: `usermod -L [username]`  
  - **Example**: `sudo usermod -L john`  
  - **Description**: Locks the account, preventing login.

- **Unlock a User Account**  
  - **Command**: `usermod -U [username]`  
  - **Example**: `sudo usermod -U john`  
  - **Description**: Unlocks the user account.

- **Set Account Expiry Date**  
  - **Command**: `usermod -e [YYYY-MM-DD] [username]`  
  - **Example**: `sudo usermod -e 2024-12-31 john`  
  - **Description**: Sets an expiration date for the user account.

---

### **7. Switching Users and Root Privileges**

- **Switch User**  
  - **Command**: `su [username]`  
  - **Example**: `su john`  
  - **Description**: Switches to another user's account.

- **Execute Commands as Another User**  
  - **Command**: `sudo [command]`  
  - **Example**: `sudo apt-get update`  
  - **Description**: Executes commands as root or another user.

- **Switch to Root User**  
  - **Command**: `sudo -i` or `su -`  
  - **Description**: Switches to the root user’s environment.

---

### **8. Monitoring Users**

- **View Detailed User Activity**  
  - **Command**: `w`  
  - **Description**: Displays detailed information about logged-in users and their activities.

- **View User's Last Login**  
  - **Command**: `last [username]`  
  - **Example**: `last john`  
  - **Description**: Shows the most recent login records for a user.

---

### **9. User Disk Quotas**

- **Set User Disk Quota**  
  - **Command**: `edquota -u [username]`  
  - **Description**: Edits the disk quota for a user.

- **View Disk Usage and Quota**  
  - **Command**: `quota [username]`  
  - **Description**: Displays the user’s disk usage and quota.

---

### **Summary of Key Commands**

| Command        | Description                                       |
|----------------|---------------------------------------------------|
| `adduser`      | Adds a new user with a home directory.             |
| `deluser`      | Deletes a user account.                           |
| `usermod`      | Modifies user account properties (e.g., group).    |
| `passwd`       | Changes or expires a user's password.             |
| `groupadd`     | Creates a new group.                              |
| `gpasswd`      | Manages group membership.                         |
| `id`           | Displays a user's UID, GID, and group memberships.|
| `whoami`       | Shows the current logged-in user.                 |
| `su`           | Switches to another user account.                 |
| `sudo`         | Executes commands as root or other user.          |
| `w`            | Shows detailed logged-in user activity.           |
| `last`         | Shows login history of users.                     |
| `quota`        | Shows disk usage and quota information.           |

---

This comprehensive guide covers all essential aspects of user and group management in Linux, including commands for managing users, groups, privileges, and monitoring system usage effectively.