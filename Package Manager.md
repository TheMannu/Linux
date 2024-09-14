
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
