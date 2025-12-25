# Lab — Windows Server File Server & NTFS Permissions

## Purpose

The purpose of this lab is to demonstrate the configuration and management of a Windows Server file server, including folder creation, NTFS permissions, share permissions, group-based access control, and user access testing. This lab reflects common real-world IT support scenarios involving file access issues and permission troubleshooting.

---

## Tools Used

- Windows Server 2022
- Active Directory Domain Services
- Active Directory Users and Computers
- NTFS Permissions
- Windows File Sharing (SMB)

---

## Environment Setup

- **Server Name:** LAB-SRV-01
- **Domain:** LAB.local
- **Role Installed:** File Server
- **Users:** Domain users
- **Access Model:** Group-based NTFS permissions

---

## Steps Performed

### 1. Installed File Server Role

- Used Server Manager to add the File Server role to the domain controller.
- Verified successful installation before proceeding.

**Screenshot included:** File Server role installation complete

---

### 2. Created Folder Structure

Created a central share location on the server:
C:\Shares
├─ IT
└─ HR

This structure simulates departmental file shares commonly found in enterprise environments.

**Screenshot included:** Folder structure created in File Explorer

---

### 3. Created Security Groups in Active Directory

Created the following Active Directory security groups:

- `IT-Share-Access`
- `HR-Share-Access`

Groups were created as **Global Security Groups** and placed in the same OU as existing users.

**Screenshot included:** Security groups created in Active Directory

---

### 4. Added Users to Groups

- Added **John Smith** to the `IT-Share-Access` group.
- Did not add the user to the HR group to enforce least privilege.

**Screenshot included:** User group membership showing IT-Share-Access

---

### 5. Configured NTFS Permissions

Applied NTFS permissions directly on each folder:

#### IT Folder
- SYSTEM — Full control
- Administrators — Full control
- IT-Share-Access — Modify

#### HR Folder
- SYSTEM — Full control
- Administrators — Full control
- HR-Share-Access — Modify

Inheritance was disabled and inherited permissions were converted and cleaned to remove unintended access.

**Screenshots included:** NTFS permissions for IT and HR folders

---

### 6. Configured Share Permissions

Shared both folders using Advanced Sharing:

- Share permissions:
  - Everyone — Read
  - Administrators — Full Control

NTFS permissions were used as the primary access control mechanism.

**Screenshots included:** Advanced Sharing permissions for IT and HR shares

---

### 7. Tested Access as Standard User

Logged in as **LAB\john.smith** and tested access:

- `\\LAB-SRV-01\IT` → Access successful
- `\\LAB-SRV-01\HR` → Access denied

This confirmed correct group-based access control.

**Screenshots included:** Successful IT access and HR access denied

---

### 8. Troubleshooting Scenario (Resolved)

During testing, the user initially had unintended access to the HR share. This was resolved by:

- Auditing user group membership
- Reviewing NTFS permissions
- Removing inherited or unintended permission entries
- Verifying inheritance was disabled correctly

This mirrors a common real-world helpdesk troubleshooting scenario.

---

## Outcome

- File server successfully configured
- NTFS permissions applied using security groups
- Access correctly restricted by department
- Unintended access identified and resolved
- Permissions validated through user testing

---

## What I Learned

- How to configure a Windows file server
- The difference between NTFS and share permissions
- Why group-based access control is best practice
- How to troubleshoot unintended file access
- How to validate permissions by testing as an end user

---

## Why This Lab Matters

File access issues are among the most common problems handled by IT support teams. This lab demonstrates practical skills required for first-line and junior IT roles, including:

- Folder and permission management
- Active Directory group administration
- Security best practices
- Structured troubleshooting
- Clear validation of access controls

---

## Files & Screenshots

All screenshots related to this lab are stored in the `/screenshots` folder.
