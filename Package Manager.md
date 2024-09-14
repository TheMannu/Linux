
---

## Linux Package Managers and Service Management
Package managers automate the installation, configuration, upgrade, and removal of software. Different Linux distributions use different package managers, but their functionality remains largely similar.

### Common Linux Package Managers

#### 1. APT (Advanced Package Tool) - Ubuntu/Debian
**Package Format**: .deb  
**Basic APT Commands**:

```bash
# Update package list
sudo apt update

# Upgrade installed packages
sudo apt upgrade

# Install a package
sudo apt install package_name

# Remove a package
sudo apt remove package_name

# Search for a package in the cache
apt-cache search keyword

# Show package details
apt show package_name

# Auto-remove unused packages
sudo apt autoremove

# Clean local repository of retrieved package files
sudo apt clean

# List available versions of a package
apt-cache madison package_name
```

---

#### 2. YUM / DNF - CentOS/RHEL/Fedora
**Package Format**: .rpm  
**YUM is used in RHEL/CentOS**; **DNF replaces YUM in Fedora**.  
**Basic YUM/DNF Commands**:

```bash
# Update package list
sudo yum update            # or sudo dnf update

# Install a package
sudo yum install package_name  # or sudo dnf install package_name

# Remove a package
sudo yum remove package_name   # or sudo dnf remove package_name

# Search for a package
yum search package_name        # or dnf search package_name

# View installed packages
yum list installed             # or dnf list installed

# Clean up cache
sudo yum clean all             # or sudo dnf clean all

# Show package details
yum info package_name          # or dnf info package_name
```

---

#### 3. Pacman - Arch Linux
**Package Format**: .pkg.tar.xz  
**Basic Pacman Commands**:

```bash
# Update package list and upgrade packages
sudo pacman -Syu

# Install a package
sudo pacman -S package_name

# Remove a package
sudo pacman -R package_name

# Search for a package
pacman -Ss package_name

# Show package details
pacman -Si package_name
```

---

#### 4. Zypper - SUSE/OpenSUSE
**Package Format**: .rpm  
**Basic Zypper Commands**:

```bash
# Refresh repository list
sudo zypper refresh

# Install a package
sudo zypper install package_name

# Remove a package
sudo zypper remove package_name

# Search for a package
zypper search package_name

# List installed packages
zypper se --installed-only
```

---