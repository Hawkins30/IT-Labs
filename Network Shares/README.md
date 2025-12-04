# Lab 9 — Network Shares & SMB Permissions (Windows → Linux)

## Purpose
The purpose of this lab is to demonstrate the creation, configuration, and testing of SMB (Server Message Block) shared folders in Windows 10, as well as verifying access from a Linux client. This is a core IT support skill used in businesses for shared drives, team folders, and secure file access.

## Tools Used
- Windows 10 Virtual Machine
- Ubuntu Linux Virtual Machine
- SMB (Server Message Block)
- NTFS Permissions
- Windows Share Permissions

---

## Part 1 — Windows SMB Share Setup

### 1. Created Shared Folder
I created a folder named **SharedFolder** and enabled file sharing through:
- Properties → Sharing → Advanced Sharing  
- Share name: *SharedFolder*

### 2. Configured Share Permissions
- **StandardUser** → Read only  
- **AdminUser** → Full Control  

### 3. Configured NTFS Permissions
Inside the Security tab:
- **StandardUser** → Read & Execute, Read, List folder contents  
- **AdminUser** → Full Control  

This ensures proper layered permissions (Share + NTFS).

### 4. Created a Test File
Created `testfile.txt` inside the shared folder for testing access.

### 5. Retrieved the Windows IP Address
Using `ipconfig`, I identified the VM’s IPv4 address to access over SMB.

---

## Part 2 — Accessing the SMB Share from Ubuntu Linux

### 1. Connected via SMB
From Ubuntu Files → Other Locations:
smb://<windows-ip-address>/SharedFolder


### 2. Tested Access as StandardUser
- Successfully opened the folder  
- Could **read** files  
- Could **NOT edit** or save changes (correct behaviour)

### 3. Tested Access as AdminUser
- Full read/write access  
- Successfully edited and saved files  

---

## Screenshots
Stored in the `screenshots` folder:
1. Share permissions window  
2. NTFS permissions  
3. Windows IP address (ipconfig)  
4. Ubuntu SMB login prompt  
5. Shared folder visible in Ubuntu  
6. StandardUser “permission denied” on edit  
7. AdminUser editing file successfully  

---

## What I Learned
- How to configure Windows SMB shares  
- Difference between Share Permissions and NTFS Permissions  
- How layered permissions interact (NTFS overrides share)  
- How to access Windows shares from Linux  
- How to test and verify read/write access  
- How to troubleshoot permission issues across OS platforms  

This lab demonstrates real-world file sharing and security administration skills used daily in IT support.
