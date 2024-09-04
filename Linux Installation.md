### **Prerequisites**
Before starting the installation, ensure the following:
1. **Virtualization Enabled**: Verify that virtualization is enabled on your system via the Task Manager. If it’s not enabled, follow the provided guide to enable it.
2. **RAM**: 4 to 8 GB of RAM is recommended for a smooth experience. Linux requires at least 2 GB of RAM, and your host machine will need additional RAM to run VirtualBox and other background applications.
3. **Disk Space**: Ensure you have at least 80 GB of free disk space.

### **Download VirtualBox**
- Download VirtualBox from the official [VirtualBox website](https://www.virtualbox.org/wiki/Downloads).
- Follow the user manual for installation instructions.

### **Download Linux Distro ISO**
- After installing VirtualBox, download the ISO file of the Linux distribution you want to install from its official website. For Ubuntu, use the following [link](https://ubuntu.com/download/desktop).

### **Setup Your Linux**
1. **Launch VirtualBox**: Click on the "New" icon to create a new virtual machine.
2. **Name and ISO Location**: Enter a name for your VM (this will be the hostname) and locate the ISO file.
3. **User Setup**: Set up a username and password for logging into the machine.
4. **Hardware Allocation**: Allocate resources to the VM, with a minimum of 2 GB of RAM required.
5. **Installation**: The system will reboot and automatically update all packages during the installation process.

### **Update and Upgrade Your Linux**
After installation, it's important to update and upgrade the system:
1. **Open Terminal**: Launch the terminal.
2. **Update and Upgrade**: Run the following command to update and upgrade all packages:
   ```bash
   sudo apt-get update && sudo apt-get upgrade -y
   ```

### **Fix Screen Resolution**
If you encounter issues with screen resolution:
1. **Insert Guest Additions CD**: Click on the "Devices" icon in VirtualBox and then select "Insert Guest Additions CD image."
2. **Open Terminal**: Navigate to the CD directory and open the terminal.
3. **Run Autorun Script**: Execute the following command:
   ```bash
   ./autorun.sh
   ```
4. **Maximize Screen**: This should fix the screen resolution issue.

### **Fix Sudoers File in Ubuntu**
If you encounter the error "user is not in the sudoers file. This incident will be recorded" when trying to switch to the root user:
1. **Login as Root**: Use the following command to switch to the root user:
   ```bash
   su root
   ```
2. **Edit Sudoers File**: Edit the sudoers file with:
   ```bash
   sudo nano /etc/sudoers
   ```
3. **Add Username**: Add your username after "root" in the privileges section:
   ```bash
   your_username ALL=(ALL:ALL) ALL
   ```
4. **Exit and Retry**: Exit from the root user and try using `sudo su` again.



- After completing these steps, your Linux installation in VirtualBox should be fully functional, allowing to enjoy a virtualized Linux environment.
