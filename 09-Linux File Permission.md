### **File Permissions & Access Control Lists in Linux**

In Linux, controlling file and directory access is essential for ensuring system security. Permissions and Access Control Lists (ACLs) are powerful tools to manage who can read, write, or execute files.

---

### **1. File Permissions in Linux**

**Overview:**  
File permissions in Linux determine who can do what with a file or directory. Permissions are set for three categories of users:  
- **Owner**: The user who created the file or directory.
- **Group**: A group to which the owner belongs.
- **Others**: All other users on the system.

---

#### **Categories of Users:**
- **Owner**: The user who created the file or directory.
- **Group**: A group of users to which the owner belongs.
- **Others**: Everyone else who has access to the file or directory but is not part of the owner or group.

---

#### **Types of Permissions:**
- **Read (r)**: Allows viewing the file's content.
- **Write (w)**: Allows modifying or deleting the file.
- **Execute (x)**: Allows running the file as a program.

---

### **2. How Permissions Are Represented:**

When you list files using `ls -l`, file permissions are shown as a string of characters:

```
drwxrwxr-x 1 ashwan ashwan 157 Oct 10 18:27 adduserss.sh
-rwxrwxr-x 1 ashwan ashwan 469 Oct 10 18:19 backup.sh
-rwxrwxr-x 1 ashwan ashwan 378 Oct 10 18:19 createDirectories.sh
-rwxrwxr-x 1 ashwan ashwan 58  Oct 10 18:18 forloop.sh
-rwxrwxr-x 1 ashwan ashwan 136 Oct 10 18:15 ifcondi.sh
```
