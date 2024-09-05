 # **Linux User Management** 
### **1. Managing Users**

- **Add a User**
  - **Command**: `adduser [username]`
  - **Example**: `sudo adduser john`
  - **Description**: Creates a new user, sets up a home directory, a default shell, and prompts for a password.

- **Delete a User**
  - **Command**: `deluser [username]`
  - **Example**: `sudo deluser john`
  - **Description**: Removes a user from the system but doesn’t delete the user’s home directory by default.
  - **Delete User and Home Directory**: 
    - **Command**: `sudo deluser --remove-home john`

- **Modify a User**
  - **Command**: `usermod [options] [username]`
  - **Example**: `sudo usermod -aG sudo john`
  - **Description**: Modifies user properties such as adding the user to a group, changing home directory, or shell.

- **List All Users**
  - **Command**: `cat /etc/passwd`
  - **Description**: Lists all users on the system. Each entry contains a username, UID, home directory, and default shell.

---

### **2. User Information and Status**

- **View Current User**
  - **Command**: `whoami`
  - **Description**: Displays the current logged-in user's name.

- **View User Information**
  - **Command**: `id [username]`
  - **Example**: `id john`
  - **Description**: Displays the UID, GID, and group memberships of a user.

- **Show Currently Logged-in Users**
  - **Command**: `who`
  - **Description**: Displays users currently logged into the system.

---

### **3. Password Management**

- **Change User Password**
  - **Command**: `passwd [username]`
  - **Example**: `sudo passwd john`
  - **Description**: Changes the password for a specified user. If no username is provided, the current user’s password is changed.

- **Expire User Password (Force Password Change)**
  - **Command**: `passwd -e [username]`
  - **Example**: `sudo passwd -e john`
  - **Description**: Forces the user to change their password upon next login.

---

### **4. Group Management**

- **Create a Group**
  - **Command**: `groupadd [groupname]`
  - **Example**: `sudo groupadd developers`
  - **Description**: Creates a new group.

- **Add User to Group**
  - **Command**: `usermod -aG [groupname] [username]`
  - **Example**: `sudo usermod -aG developers john`
  - **Description**: Adds the user to the specified group without removing them from other groups.

- **Remove User from Group**
  - **Command**: `gpasswd -d [username] [groupname]`
  - **Example**: `sudo gpasswd -d john developers`
  - **Description**: Removes a user from a specified group.

- **List Group Membership**
  - **Command**: `groups [username]`
  - **Example**: `groups john`
  - **Description**: Lists the groups the user belongs to.

- **List All Groups**
  - **Command**: `cat /etc/group`
  - **Description**: Lists all groups on the system.

---

### **5. User Account Configuration Files**

- **`/etc/passwd`**
  - Contains user account details such as username, UID, GID, home directory, and default shell.

- **`/etc/shadow`**
  - Stores encrypted passwords and password expiration policies.

- **`/etc/group`**
  - Contains group information including group name, GID, and group members.

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
  - **Description**: Sets the expiration date for the user account.

---

### **7. Switching Users and Root Privileges**

- **Switch User**
  - **Command**: `su [username]`
  - **Example**: `su john`
  - **Description**: Switches to another user account.

- **Execute Command as Another User**
  - **Command**: `sudo [command]`
  - **Example**: `sudo apt-get update`
  - **Description**: Runs commands as the root or specified user.

- **Switch to Root User**
  - **Command**: `sudo -i` or `su -`
  - **Description**: Switches to the root user’s environment.

---

### **8. Monitoring Users**

- **View Detailed User Activity**
  - **Command**: `w`
  - **Description**: Displays detailed info about logged-in users and their activity.

- **View User’s Last Login**
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

### **Summary of Key Commands:**

| Command            | Description                                        |
|--------------------|----------------------------------------------------|
| `adduser`          | Adds a new user with home directory.               |
| `deluser`          | Deletes a user account.                            |
| `usermod`          | Modifies user account properties (e.g., group).    |
| `passwd`           | Changes or expires a user’s password.              |
| `groupadd`         | Creates a new group.                               |
| `gpasswd`          | Manages group membership.                          |
| `id`               | Displays a user’s UID, GID, and group memberships. |
| `whoami`           | Shows the current logged-in user.                  |
| `su`               | Switches to another user account.                  |
| `sudo`             | Executes commands as root or other user.           |
| `w`                | Shows detailed logged-in user activity.            |
| `last`             | Shows login history of users.                      |
| `quota`            | Shows disk usage and quota information.            |

---

This set of commands,  can be used to manage users, groups, and permissions, ensuring both system security and user management on Linux.
