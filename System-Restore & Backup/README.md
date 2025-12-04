# Lab 13 — Virtual Backup Drive Creation & Backup Simulation

## Purpose
The purpose of this lab is to demonstrate how to create and configure a secondary virtual hard disk in VirtualBox, format it in Windows, assign a drive letter, and use it as a simulated backup drive. This mimics real-world backup procedures used by IT support technicians.

## Tools Used
- Oracle VirtualBox  
- Windows 10 Virtual Machine  
- VirtualBox VDI Virtual Hard Disk  
- Windows Disk Management  
- NTFS File System  
- File Explorer (Copy & Backup Simulation)

---

## Steps Performed

### **1. Created a New Virtual Hard Disk**
- Opened **VirtualBox → File → Virtual Media Manager**  
- Created a new **VDI (VirtualBox Disk Image)**  
- Size: **10 GB**  
- Format: **Dynamically Allocated**

### **2. Attached the Disk to the Windows VM**
- VM Settings → **Storage**  
- Added the new `.vdi` file as a **Secondary SATA Disk**

### **3. Booted Windows & Opened Disk Management**
- Disk detected as **unallocated space**
- Initialized disk as **MBR**

### **4. Created a New Volume**
- Right-clicked unallocated space → **New Simple Volume**
- Assigned drive letter **E:**
- Formatted as **NTFS**
- Labeled volume **BackupDrive**

### **5. Verified Disk Creation**
Disk Management shows:
- C: drive  
- E: **BackupDrive**  
- Status: *Healthy (Primary Partition)*  

### **6. Simulated Backup**
- Created `ImportantFiles` in **Documents**
- Added sample files (text file, folder, etc.)
- Copied folder to **BackupDrive (E:)**  
- Verified successful copy

---

## Screenshots Included
1. VirtualBox: New VDI disk created  
2. Disk Management: Unallocated space  
3. Disk initialized & formatted  
4. Drive assigned letter E  
5. BackupDrive shown as *Healthy*  
6. File copy from Documents → BackupDrive  

---

## Skills Demonstrated
- Hypervisor virtual storage management  
- Windows disk initialization & formatting  
- NTFS configuration  
- Logical volumes & partitioning  
- Basic backup simulation  
- File management & verification  

---

## Conclusion
This lab successfully demonstrates creating and configuring a secondary storage device inside a virtual environment and using it to perform a simulated backup — a core CompTIA A+ skill essential for real IT support work.
