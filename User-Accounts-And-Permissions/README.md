# Lab 8 — User Accounts & Permissions (Microsoft Windows + Linux)

## Purpose
The purpose of this lab is to demonstrate practical user account administration and file permissions management in **both Microsoft Windows 10** and **Ubuntu Linux**. These skills are essential in any entry-level IT support, helpdesk, or system administration role. This lab shows the ability to create and manage local accounts, configure permissions, secure files, and test access controls across two major operating systems.

---

# Part 1 — Microsoft Windows 10 User Accounts & NTFS Permissions

## 1. Creating Local Windows Accounts
Using **Settings → Accounts → Family & other users**, I created two local accounts:
- **StandardUser** – Standard account with limited privileges  
- **AdminUser** – Elevated account with Administrator privileges  

I then changed the account type of AdminUser to **Administrator**.

**Screenshots included:**
1. Creation of StandardUser  
2. AdminUser listed as an Administrator  

---

## 2. Configuring NTFS Folder Permissions
I created a test folder named **PermissionsTest** on the Windows desktop.  
Through **Right-click → Properties → Security → Edit**, I applied the following permissions:

### StandardUser:
- Allow: **Read**, **Read & Execute**, **List folder contents**  
- Not allowed: Modify, Write, Full Control  
(This provides read-only access.)

### AdminUser:
- Allow: **Full Control**

I then signed into **StandardUser** and attempted to modify a file inside the folder.  
Windows correctly blocked the action with an “Access Denied” message.

**Screenshots included:**
3. NTFS permission settings  
4. StandardUser’s restricted permissions  
5. “Access Denied” message when StandardUser tries to modify a file  

---

# Part 2 — Ubuntu Linux User Accounts & File Permissions

## 3. Creating Linux Users
Using the terminal, I created two Linux accounts:

sudo adduser standarduser
sudo adduser adminuser


- **standarduser** has normal privileges  
- **adminuser** was added to the **sudo** group, giving admin rights  

**Screenshots included:**
6. User creation commands  
7. adminuser added to sudo group  

---

## 4. Configuring Linux File Ownership & Permissions
I created a permissions test folder:
mkdir /home/<my-username>/permissiontest

Then set ownership to **standarduser**:
sudo chown standarduser:standarduser /home/<my-username>/permissiontest

And locked the folder so only the owner can access it:
sudo chmod 700 /home/<my-username>/permissiontest


This means:
- Owner (standarduser) → full access  
- Group → no access  
- Others → no access  

**Screenshots included:**
8. chown and chmod commands  

---

## 5. Permission Testing (Linux)
I switched to adminuser:
su - adminuser

Then attempted to access the folder:
cd /home/<my-username>/permissiontest

Linux correctly returned: permission denied


This confirms that the permissions were applied correctly.

**Screenshot included:**
9. Permission denied error  

---

# What I Learned
- How to create and manage local users in both Windows and Linux  
- How NTFS permissions work and how to apply least-privilege principles  
- The difference between Allow vs Deny permissions in Windows  
- How to test and verify NTFS access restrictions  
- How to create Linux users and elevate to sudo/admin  
- How to use `chown`, `chmod`, and ownership concepts in Linux  
- How to test Linux permission restrictions effectively  
- Cross-platform user and permission management (Microsoft + Linux)

---

# Files & Screenshots
All screenshots for this lab are stored in the `/screenshots` folder.



