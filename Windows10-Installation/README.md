# Lab 1 — Installing Windows 10 in VirtualBox

## Purpose
The purpose of this lab is to install Windows 10 inside a VirtualBox virtual machine. This creates a safe environment for practising IT support tasks and sets the foundation for future labs.

## Tools Used
- Oracle VirtualBox
- Windows 10 ISO file
- Windows 11 host computer

## Steps Taken

### 1. Created a New Virtual Machine
I created a VM named **Windows10-Lab** with the following hardware:
- 4GB RAM
- 2 CPU cores
- 50GB virtual hard disk
- Windows 10 (64-bit)

### 2. Attached the Windows 10 ISO
In VirtualBox Storage settings, I selected the Windows10-ISO.iso file as the virtual optical drive.

### 3. Started the VM and Booted Into Windows Setup
When the VM started, it booted from the ISO and opened the Windows Setup screen.

### 4. Selected Windows Edition
I chose **Windows 10 Pro** for the installation.

### 5. Custom Installation
I selected **Custom: Install Windows only (advanced)** and installed Windows on **Drive 0 Unallocated Space**.

### 6. Installation Process
Windows copied files, installed features and updates, and rebooted several times.

### 7. Completed First-Time Setup
I completed the out-of-box setup, created a local user account, and arrived at the Windows 10 desktop.

### 8. Installed VirtualBox Guest Additions
Inside the VM, I opened:
**Devices → Insert Guest Additions CD Image...**

Then I ran **VBoxWindowsAdditions.exe**, installed the drivers, and rebooted the VM.

## Screenshots
Screenshots are stored in the `screenshots` folder and include:

1. Windows Setup initial screen  
2. Windows edition selection (Windows 10 Pro)  
3. Custom installation option  
4. Disk selection screen  
5. Installation progress  
6. First Windows 10 desktop  
7. VirtualBox Guest Additions installer running  

## What I Learned
- How to create and configure a virtual machine  
- How to attach an ISO and boot from it  
- How to perform a clean installation of Windows 10  
- How virtual hard disks and virtual hardware work  
- How to install Guest Additions to improve VM performance
