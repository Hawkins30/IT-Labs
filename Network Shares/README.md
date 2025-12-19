# Lab 9 — Network Shares & SMB Permissions (Windows → Linux)

## Lab Objective
Demonstrate the creation, configuration, and testing of Windows SMB shared folders, including layered share and NTFS permissions, and verify access from a Linux client. This mirrors real-world file sharing and access control tasks performed in IT support environments.

---

## Scenario
A support technician is required to configure a shared network folder on a Windows system, apply appropriate access permissions for different user roles, and verify access from a Linux workstation. The goal is to ensure secure, role-based access to shared resources.

---

## Environment
- **Windows 10 Virtual Machine** (SMB host)  
- **Ubuntu Linux Virtual Machine** (client)  
- **Protocols & Technologies:**
  - SMB (Server Message Block)
  - NTFS permissions
  - Windows share permissions

---

## Part 1 — Windows SMB Share Configuration

### 1. Created a Shared Folder
Created a folder named:
"SharedFolder"

Enabled sharing via:
"Properties → Sharing → Advanced Sharing"

Configured the share name as:
"SharedFolder"

---

### 2. Configured Share Permissions
Applied the following share-level permissions:
- **StandardUser:** Read  
- **AdminUser:** Full Control  

---

### 3. Configured NTFS Permissions
Configured NTFS permissions under the **Security** tab:

- **StandardUser:**  
  - Read & Execute  
  - Read  
  - List folder contents  

- **AdminUser:**  
  - Full Control  

This ensured correct layered permissions, with NTFS permissions enforcing final access control.

---

### 4. Created a Test File
Created a test file within the shared folder:
"testfile.txt"

This file was used to validate read and write permissions.

---

### 5. Identified the Windows IP Address
Used the following command to identify the Windows VM’s IPv4 address:
"
This file was used to validate read and write permissions.

---

### 5. Identified the Windows IP Address
Used the following command to identify the Windows VM’s IPv4 address:
"ipconfig"

This IP address was required for SMB access from the Linux client.

---

## Part 2 — Accessing the SMB Share from Ubuntu Linux

### 1. Connected to the SMB Share
From Ubuntu, navigated to:
"Files → Other Locations"

Connected using:
"smb://<Windows_IP>/SharedFolder"

---

### 2. Tested Access as StandardUser
Logged in using **StandardUser** credentials and verified:
- Successful access to the shared folder  
- Ability to read files  
- Inability to edit or save changes (expected behaviour)  

---

### 3. Tested Access as AdminUser
Logged in using **AdminUser** credentials and verified:
- Full read/write access  
- Ability to edit and save files successfully  

---

## Verification
- SMB share accessible from Linux client  
- Share permissions applied correctly  
- NTFS permissions enforced as expected  
- Read-only and full-access roles validated  
- Cross-platform access functioning correctly  

---

## Outcome
The shared folder was successfully configured with secure, role-based access. Permissions behaved as expected across Windows and Linux systems, demonstrating correct implementation of SMB sharing and layered permissions.

---

## Key Takeaways
- How to configure Windows SMB shared folders  
- Difference between share permissions and NTFS permissions  
- How layered permissions interact (NTFS overrides share permissions)  
- How to access Windows shares from Linux systems  
- How to test and verify read/write access  
- How to troubleshoot cross-platform permission issues  

---

## Evidence
Screenshots documenting each stage are stored in the `/screenshots` directory, including:
- Share permissions configuration  
- NTFS permissions settings  
- Windows IP address (`ipconfig`)  
- Ubuntu SMB login prompt  
- Shared folder visible in Ubuntu  
- StandardUser permission denied when editing  
- AdminUser successfully editing files  

---

## Why This Lab Matters
Network shares and permissions are a core responsibility of IT support teams. This lab demonstrates real-world file sharing, access control, and cross-platform troubleshooting skills used daily in business environments.
