# Lab 1 — Installing Windows 10 in VirtualBox

## Purpose

The purpose of this lab is to install Microsoft Windows 10 inside an Oracle VirtualBox virtual machine. This creates a safe, isolated environment for practising IT support and troubleshooting tasks and provides the foundation for all subsequent Windows-based labs.

---

## Tools Used

- Oracle VirtualBox  
- Windows 10 ISO file  
- Windows 11 host computer  

---

## Steps Performed

### 1. Created a New Virtual Machine

Created a new virtual machine named **Windows10-Lab** with the following configuration:

- 4 GB RAM  
- 2 CPU cores  
- 50 GB virtual hard disk  
- Operating system type: **Windows 10 (64-bit)**  

---

### 2. Attached the Windows 10 ISO

Opened **VirtualBox → Settings → Storage** and attached the **Windows 10 ISO** file as the virtual optical drive.

---

### 3. Booted Into Windows Setup

Started the virtual machine.  
The VM booted from the ISO and displayed the **Windows Setup** screen.

---

### 4. Selected Windows Edition

Selected **Windows 10 Pro** for installation.  
This edition was chosen as it includes features commonly used in IT support environments.

---

### 5. Performed a Custom Installation

Selected **Custom: Install Windows only (advanced)** and installed Windows on **Drive 0 Unallocated Space**.

---

### 6. Completed the Installation Process

Windows copied files, installed features and updates, and rebooted several times automatically until installation was complete.

---

### 7. Completed First-Time Setup

Completed the out-of-box experience (OOBE), created a local user account, and successfully reached the Windows 10 desktop.

---

### 8. Installed VirtualBox Guest Additions

Inside the virtual machine, selected **Devices → Insert Guest Additions CD Image**.  
Ran **VBoxWindowsAdditions.exe**, installed the required drivers, and rebooted the VM.

Guest Additions improve display resolution, performance, and mouse integration.

---

## Screenshots

Screenshots are stored in the `screenshots` folder and include:

1. Windows Setup initial screen  
2. Windows edition selection (Windows 10 Pro)  
3. Custom installation option  
4. Disk selection screen  
5. Installation progress  
6. First Windows 10 desktop  
7. VirtualBox Guest Additions installer running  

---

## What I Learned

- How to create and configure a virtual machine in VirtualBox  
- How to attach an ISO file and boot from virtual media  
- How to perform a clean installation of Windows 10  
- How virtual hardware and virtual disks function  
- How to install Guest Additions to improve virtual machine usability  
