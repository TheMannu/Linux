## **Linux Boot Process**

The **Linux Boot Process** is a sequence of steps that occur when a system is powered on, leading to the operating system's full initialization. 

Structured Overview of the boot process:
---

### 1. **Power ON/Restart**
   - **Description**: The boot process starts when you power on or restart your machine. This triggers the initialization of system hardware and loads the operating system.
  
### 2. **System Startup/Hardware Initialization**
   - **Description**: The **BIOS (Basic Input/Output System)** initializes the system hardware. It performs a **POST (Power-On Self Test)** to ensure all necessary hardware components like the CPU, memory, and peripherals are functioning properly.
   - **Key Functions**:
     - Verifies hardware functionality through POST.
     - Locates the boot device containing the **Master Boot Record (MBR)**, and hands over control to it.

### 3. **MBR (Master Boot Record)**
   - **Description**: The **MBR** resides in the first sector of the bootable disk (usually 512 bytes). It contains boot loader information and the partition table.
   - **Key Functions**:
     - Loads the boot loader into memory (typically **GRUB** or another boot manager).
     - Contains partition information to identify the location of the bootloader and system partitions.
