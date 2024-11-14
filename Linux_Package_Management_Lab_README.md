
# Hands-On Lab: Linux Package Management in a Real-World Scenario (Debian and RedHat Distros)

**Difficulty Level:** Beginner to Medium  
**Duration:** 30-40 minutes  
**Objective:** Learn to manage software packages in a real-world scenario on both Debian-based (Ubuntu, Debian) and RedHat-based (CentOS, RHEL, Fedora) distributions. This lab simulates package management in a real-world production environment, focusing on installing, updating, and troubleshooting applications.

---

## Scenario:

You are a system administrator for a startup company running both **Ubuntu** and **CentOS** servers. Your team has identified an issue where critical performance monitoring tools are missing on some servers, and outdated software is running on others. Additionally, the development team needs specific tools for compiling code.

Your task is to:
- Install the missing performance monitoring tools (`htop`) on both Debian-based and RedHat-based servers.
- Search for and update essential tools (`vim`) across the servers.
- Ensure all software packages are up-to-date.
- Install a package group that provides a complete development environment for the team.

---

## Lab Setup:

You will need access to:
- **One Debian-based system** (e.g., Ubuntu or Debian)
- **One RedHat-based system** (e.g., CentOS or Fedora)

Ensure you have **sudo** privileges on both systems.

---

## Lab Outline:

1. **Task 1: Diagnose and Install Missing Monitoring Tools**
   - Install the `htop` system monitoring tool to address the missing package.
   
2. **Task 2: Search for and Update an Essential Tool**
   - Search for and update the `vim` text editor, ensuring the latest version is installed.
   
3. **Task 3: Fix Dependency Issues with a Broken Package**
   - Simulate a scenario where a package installation has failed due to broken dependencies. Resolve the issue.
   
4. **Task 4: Update All Installed Packages**
   - Update all installed software packages to the latest versions.
   
5. **Task 5: Install Development Tools for the Team**
   - Install a development environment using a metapackage or group of software.

---

## Step-by-Step Instructions:

---

### **Task 1: Diagnose and Install Missing Monitoring Tools**

#### Debian-based System (Ubuntu/Debian):

1. **Update the package index**:
   ```bash
   sudo apt update
   ```

2. **Install `htop`**:
   ```bash
   sudo apt install htop
   ```

3. **Verify the installation** by running `htop`:
   ```bash
   htop
   ```

#### RedHat-based System (CentOS/Fedora):

1. **Update the package index**:
   ```bash
   sudo yum check-update   # On CentOS/RHEL
   sudo dnf check-update   # On Fedora
   ```

2. **Install `htop`**:
   ```bash
   sudo yum install htop   # On CentOS/RHEL
   sudo dnf install htop   # On Fedora
   ```

3. **Verify the installation** by running `htop`:
   ```bash
   htop
   ```

---

### **Task 2: Search for and Update an Essential Tool**

#### Debian-based System (Ubuntu/Debian):

1. **Search for the `vim` package**:
   ```bash
   apt search vim
   ```

2. **Install or upgrade `vim`**:
   ```bash
   sudo apt install vim
   ```

3. **Check the installed version**:
   ```bash
   vim --version
   ```

#### RedHat-based System (CentOS/Fedora):

1. **Search for the `vim` package**:
   ```bash
   yum search vim   # On CentOS/RHEL
   dnf search vim   # On Fedora
   ```

2. **Install or upgrade `vim`**:
   ```bash
   sudo yum install vim   # On CentOS/RHEL
   sudo dnf install vim   # On Fedora
   ```

3. **Check the installed version**:
   ```bash
   vim --version
   ```

---

### **Task 3: Fix Dependency Issues with a Broken Package**

#### Debian-based System (Ubuntu/Debian):

1. **Simulate a package with broken dependencies**:
   If a package installation fails, you can use `--fix-broken` to resolve dependencies:
   ```bash
   sudo apt install --fix-broken
   ```

2. **Resolve dependencies automatically**:
   ```bash
   sudo apt install -f
   ```

#### RedHat-based System (CentOS/Fedora):

1. **Simulate a package with broken dependencies**:
   If a package installation fails, use `yum` or `dnf` to resolve dependencies:
   ```bash
   sudo yum install <package> --skip-broken   # On CentOS/RHEL
   sudo dnf install <package> --skip-broken   # On Fedora
   ```

2. **Manually resolve dependencies**:
   ```bash
   sudo yum deplist <package>   # On CentOS/RHEL
   sudo dnf deplist <package>   # On Fedora
   ```

---

### **Task 4: Update All Installed Packages**

#### Debian-based System (Ubuntu/Debian):

1. **Update the package index**:
   ```bash
   sudo apt update
   ```

2. **Upgrade all installed packages**:
   ```bash
   sudo apt upgrade
   ```

#### RedHat-based System (CentOS/Fedora):

1. **Update the package index**:
   ```bash
   sudo yum check-update   # On CentOS/RHEL
   sudo dnf check-update   # On Fedora
   ```

2. **Upgrade all installed packages**:
   ```bash
   sudo yum update   # On CentOS/RHEL
   sudo dnf upgrade  # On Fedora
   ```

---

### **Task 5: Install Development Tools for the Team**

#### Debian-based System (Ubuntu/Debian):

1. **Install the `build-essential` metapackage** (includes GCC, G++, and other tools):
   ```bash
   sudo apt install build-essential
   ```

#### RedHat-based System (CentOS/Fedora):

1. **Install the `Development Tools` group** (provides compilers, libraries, and related tools):
   ```bash
   sudo yum groupinstall "Development Tools"   # On CentOS/RHEL
   sudo dnf groupinstall "Development Tools"   # On Fedora
   ```

---

## Lab Wrap-Up:

In this lab, you managed package installations, updates, and troubleshooting on both Debian-based and RedHat-based systems in a real-world scenario. You installed essential software for monitoring, ensured tools were up-to-date, resolved dependency issues, and provided a development environment for the team. These skills are vital for managing software on production Linux servers and are commonly used in system administration roles.
