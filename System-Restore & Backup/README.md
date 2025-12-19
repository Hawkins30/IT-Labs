# Lab 13 — Virtual Backup Drive Creation & Backup Simulation

## Purpose
The purpose of this lab is to demonstrate how to create and configure a secondary virtual hard disk in VirtualBox, format and mount it in Windows, and use it as a simulated backup drive. This reflects real-world backup and storage management tasks performed by IT support technicians.

---

## Tools Used
- Oracle VirtualBox  
- Windows 10 Virtual Machine  
- VirtualBox VDI (Virtual Disk Image)  
- Windows Disk Management  
- NTFS File System  
- File Explorer  

---

## Steps Performed

### 1. Created a New Virtual Hard Disk
- Opened **VirtualBox → File → Virtual Media Manager**
- Created a new **VDI (VirtualBox Disk Image)**
- Disk size: **10 GB**
- Storage type: **Dynamically Allocated**

---

### 2. Attached the Disk to the Windows Virtual Machine
- Opened **VM Settings → Storage**
- Attached the new `.vdi` file as a **secondary SATA disk**

---

### 3. Initialized the Disk in Windows
- Booted the Windows virtual machine
- Opened **Disk Management**
- Detected the new disk as **unallocated**
- Initialized the disk using **MBR**

---

### 4. Created and Formatted a New Volume
- Right-clicked unallocated space → **New Simple Volume**
- Assigned drive letter **E:**
- Formatted the volume as **NTFS**
- Labeled the volume **BackupDrive**

---

### 5. Verified Disk Creation
Disk Management confirmed:
- **C:** System drive  
- **E:** BackupDrive  
- Status: **Healthy (Primary Partition)**

---

### 6. Simulated a Backup Process
- Created a folder named **ImportantFiles** in *Documents*
- Added sample files (text files and folders)
- Copied the folder to **BackupDrive (E:)**
- Verified the files were copied successfully

---

## Screenshots
Screenshots are stored in the `screenshots` folder and include:
1. VirtualBox – New VDI disk created  
2. Disk Management – Unallocated disk detected  
3. Disk initialized and formatted  
4. Drive letter **E:** assigned  
5. BackupDrive shown as **Healthy**  
6. File copy from Documents → BackupDrive  

---

## What I Learned
- How to create and attach virtual disks in VirtualBox  
- How to initialize and format disks using Windows Disk Management  
- How to create and label NTFS volumes  
- How to simulate a basic backup process  
- Why secondary storage and backups are critical in IT environments  

---

## Why This Lab Matters
Backup and storage management are core responsibilities in IT support roles. This lab demonstrates practical experience with disk provisioning, formatting, and data backup — skills required for both CompTIA A+ and real-world helpdesk environments.
