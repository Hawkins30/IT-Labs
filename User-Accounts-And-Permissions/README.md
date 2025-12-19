# Lab 8 – User Accounts & Permissions (Microsoft Windows + Linux)

## Purpose

The purpose of this lab is to demonstrate practical user account administration and file permission management across both Microsoft Windows 10 and Ubuntu Linux. These skills are essential for entry-level IT support, helpdesk, and system administration roles.

This lab demonstrates the ability to create and manage local user accounts, configure permissions, apply least-privilege principles, and verify access controls across two major operating systems.

---

## Tools Used

- Windows 10 Virtual Machine  
- Ubuntu Linux Virtual Machine  
- NTFS File System  
- Linux Terminal  
- adduser  
- usermod  
- chmod  
- chown  

---

## Part 1 – Microsoft Windows 10 User Accounts & NTFS Permissions

### 1. Creating Local Windows User Accounts

Using **Settings → Accounts → Family & other users**, I created two local user accounts:

- **StandardUser** – Standard account with limited privileges  
- **AdminUser** – Elevated account with Administrator privileges  

I then verified that **AdminUser** was assigned the *Administrator* role.

**Screenshots included:**
1. Creation of StandardUser  
2. AdminUser listed as Administrator  

---

### 2. Configuring NTFS Folder Permissions

I created a test folder named **PermissionsTest** on the Windows desktop.

Using **Right-click → Properties → Security → Edit**, I applied the following NTFS permissions:

**StandardUser**
- Allowed: Read, Read & Execute, List folder contents  
- Not allowed: Modify, Write, Full Control  
- Result: Read-only access  

**AdminUser**
- Allowed: Full Control  

I then signed in as **StandardUser** and attempted to modify a file inside the folder.  
Windows correctly blocked the action and displayed an **“Access Denied”** message.

**Screenshots included:**
3. NTFS permission settings  
4. StandardUser restricted permissions  
5. “Access Denied” message when modification was attempted  

---

## Part 2 – Ubuntu Linux User Accounts & File Permissions

### 3. Creating Linux Users

Using the Linux terminal, I created two user accounts:

- Created **standarduser** using `sudo adduser standarduser`  
- Created **adminuser** using `sudo adduser adminuser`  

I then added **adminuser** to the sudo group using `sudo usermod -aG sudo adminuser`.

- **standarduser** has standard privileges  
- **adminuser** has administrative (sudo) privileges  

**Screenshots included:**
6. User creation commands  
7. adminuser added to sudo group  

---

### 4. Configuring Linux File Ownership & Permissions

I created a permissions test directory named **permissionstest** inside `/home`.

I then configured ownership and permissions as follows:

- Set ownership to **standarduser** using `sudo chown standarduser:standarduser /home/permissionstest`  
- Restricted access so only the owner could access the directory using `sudo chmod 700 /home/permissionstest`  

This configuration results in:

- Owner (standarduser): Full access  
- Group: No access  
- Others: No access  

**Screenshots included:**
8. chown and chmod commands  

---

### 5. Permission Testing (Linux)

I switched to **adminuser** and attempted to access the directory.

Linux correctly returned **permission denied**, confirming that the permissions were enforced correctly and that sudo privileges do not override file ownership without explicit elevation.

**Screenshot included:**
9. Permission denied error  

---

## What I Learned

- How to create and manage local users in both Windows and Linux  
- How NTFS permissions work and how to apply least-privilege principles  
- The difference between Allow vs Deny permissions in Windows  
- How to test and verify NTFS access restrictions  
- How to create Linux users and elevate privileges using sudo  
- How to use chown, chmod, and ownership concepts in Linux  
- How to test Linux permission restrictions effectively  
- Cross-platform user and permission management (Microsoft Windows + Linux)  

---

## Files & Screenshots

All screenshots for this lab are stored in the `/screenshots` folder.
