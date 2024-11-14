
# User and Group Management Lab

## Introduction

Welcome to the User and Group Management Lab for Linux. In this lab, you will learn how to perform essential tasks for managing users and groups in a Linux environment. The tasks simulate real-world scenarios to provide practical experience in system administration.

## Objectives

By the end of this lab, you will be able to:
- Create and manage user accounts.
- Create and manage groups.
- Assign users to groups.
- Configure user accounts with specific settings.
- Manage user permissions and privileges.
- Delete users and groups.

## Lab Environment

This lab can be performed on a virtual machine, a cloud-based Linux environment, or a local Linux installation. Ensure you have sudo (administrative) privileges to perform the tasks.

## Prerequisites

- Basic understanding of Linux command line.
- Access to a Linux system with sudo privileges.

## Lab Instructions

### 1. Create a New User
**Objective:** Create a user named `john` with a home directory and set a password.

**Steps:**
```sh
sudo useradd -m john
sudo passwd john
```

### 2. Create a Group
**Objective:** Create a group named `developers`.

**Steps:**
```sh
sudo groupadd developers
```

### 3. Add User to a Group
**Objective:** Add user `john` to the `developers` group.

**Steps:**
```sh
sudo usermod -aG developers john
```

### 4. Create a User with a Specific UID
**Objective:** Create a user named `alice` with a specific UID of `1050`.

**Steps:**
```sh
sudo useradd -u 1050 alice
sudo passwd alice
```

### 5. Create a User with a Specific Home Directory
**Objective:** Create a user named `bob` with a custom home directory `/home/custombob`.

**Steps:**
```sh
sudo useradd -m -d /home/custombob bob
sudo passwd bob
```

### 6. Create a User with No Login Shell
**Objective:** Create a user named `nologinuser` who cannot log in.

**Steps:**
```sh
sudo useradd -s /usr/sbin/nologin nologinuser
```

### 7. Add Admin/Sudo Privileges to a User
**Objective:** Grant user `john` sudo privileges.

**Steps:**
```sh
sudo usermod -aG sudo john
```

### 8. Delete a User
**Objective:** Delete user `alice`.

**Steps:**
```sh
sudo userdel alice
```

### 9. Delete a Group
**Objective:** Delete the `developers` group.

**Steps:**
```sh
sudo groupdel developers
```

### 10. Set Password for a User
**Objective:** Set or change the password for user `bob`.

**Steps:**
```sh
sudo passwd bob
```

## Assessment
- What command is used to create a new user with a specific UID?
- How do you add a user to a group?
- What command is used to grant sudo privileges to a user?
- How do you delete a user and a group?

## Summary

This lab covers essential tasks for managing users and groups in a Linux environment, providing practical experience that mirrors real-world scenarios.

## Follow-up Questions

**Q1:** How can we automate the process of user creation and group management using shell scripts?

**Q2:** What are some best practices for securing user accounts and managing permissions in Linux?

**Q3:** How can we monitor and audit user activities to ensure compliance with security policies?
