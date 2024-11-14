
# User and Group Management Lab - Solutions

## Lab Instructions with Solutions

### 1. Create a New User
**Objective:** Create a user named `john` with a home directory and set a password.

**Steps:**
```sh
sudo useradd -m john
sudo passwd john
```
**Explanation:** The `useradd -m john` command creates a new user `john` with a home directory, and `passwd john` sets the user's password.

### 2. Create a Group
**Objective:** Create a group named `developers`.

**Steps:**
```sh
sudo groupadd developers
```
**Explanation:** The `groupadd developers` command creates a new group named `developers`.

### 3. Add User to a Group
**Objective:** Add user `john` to the `developers` group.

**Steps:**
```sh
sudo usermod -aG developers john
```
**Explanation:** The `usermod -aG developers john` command adds `john` to the `developers` group.

### 4. Create a User with a Specific UID
**Objective:** Create a user named `alice` with a specific UID of `1050`.

**Steps:**
```sh
sudo useradd -u 1050 alice
sudo passwd alice
```
**Explanation:** The `useradd -u 1050 alice` command creates a new user `alice` with a UID of `1050`, and `passwd alice` sets the user's password.

### 5. Create a User with a Specific Home Directory
**Objective:** Create a user named `bob` with a custom home directory `/home/custombob`.

**Steps:**
```sh
sudo useradd -m -d /home/custombob bob
sudo passwd bob
```
**Explanation:** The `useradd -m -d /home/custombob bob` command creates a new user `bob` with the specified home directory, and `passwd bob` sets the user's password.

### 6. Create a User with No Login Shell
**Objective:** Create a user named `nologinuser` who cannot log in.

**Steps:**
```sh
sudo useradd -s /usr/sbin/nologin nologinuser
```
**Explanation:** The `useradd -s /usr/sbin/nologin nologinuser` command creates a new user `nologinuser` with no login shell.

### 7. Add Admin/Sudo Privileges to a User
**Objective:** Grant user `john` sudo privileges.

**Steps:**
```sh
sudo usermod -aG sudo john
```
**Explanation:** The `usermod -aG sudo john` command adds `john` to the `sudo` group, granting administrative privileges.

### 8. Delete a User
**Objective:** Delete user `alice`.

**Steps:**
```sh
sudo userdel alice
```
**Explanation:** The `userdel alice` command deletes the user `alice`.

### 9. Delete a Group
**Objective:** Delete the `developers` group.

**Steps:**
```sh
sudo groupdel developers
```
**Explanation:** The `groupdel developers` command deletes the `developers` group.

### 10. Set Password for a User
**Objective:** Set or change the password for user `bob`.

**Steps:**
```sh
sudo passwd bob
```
**Explanation:** The `passwd bob` command sets or changes the password for `bob`.

## Summary

This lab covers essential tasks for managing users and groups in a Linux environment, providing practical experience that mirrors real-world scenarios.
