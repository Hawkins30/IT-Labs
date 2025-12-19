# Lab 6 — Installing Ubuntu Linux in VirtualBox

## Purpose

The purpose of this lab is to demonstrate how to install Ubuntu Linux inside an Oracle VirtualBox virtual machine. This provides a safe environment for learning Linux fundamentals, practising command-line skills, and understanding open-source operating systems commonly used in IT support and server administration.

## Tools Used

- Oracle VirtualBox
- Ubuntu Desktop ISO (24.04 LTS)
- Windows 11 host machine

## Steps Performed

### 1. Created a New Virtual Machine

Created a new virtual machine named **Ubuntu-Lab** with the following configuration:

- 4 GB RAM  
- 2 CPU cores  
- 30 GB virtual hard disk  
- Ubuntu (64-bit) operating system type  

### 2. Attached the Ubuntu ISO

- Opened **VirtualBox Settings**
- Navigated to **Storage**
- Attached the Ubuntu Desktop ISO to the virtual optical drive

### 3. Booted the VM and Launched the Installer

- Started the virtual machine
- Booted into the Ubuntu GRUB menu
- Selected **Try or Install Ubuntu**
- Chose **Interactive Installation**

### 4. Selected Installation Options

Used the default recommended options:

- Normal installation
- Download updates during installation
- Install third-party software

### 5. Disk Setup

- Selected **Erase disk and install Ubuntu**
- Confirmed that only the virtual disk would be formatted

### 6. User Account Setup

- Created a Linux user account
- Set username and password
- Continued with the installation

### 7. Installation Process

- Ubuntu copied system files
- Installed the operating system
- Downloaded updates
- Configured system components automatically

### 8. First Boot and Basic Linux Commands

After installation completed and the system rebooted, logged into the Ubuntu desktop and opened the terminal to run:

- ls  
- pwd  
- uname -a  
- sudo apt update  

These commands confirmed that the system was functioning correctly and able to update packages.

## Screenshots Included

Screenshots are stored in the `screenshots` folder and include:

1. Ubuntu installer main screen (“Try Ubuntu / Install Ubuntu”)  
2. Interactive installation selection  
3. Disk setup screen (“Erase disk and install Ubuntu”)  
4. User account creation screen  
5. Installation progress screen  
6. First Ubuntu desktop after login  
7. Terminal showing basic Linux commands  

## What I Learned

- How to install Ubuntu Linux inside a virtual machine
- Basics of Linux system setup and user creation
- How to use common Linux terminal commands
- Understanding virtual disks and operating system installation workflows

## Conclusion

This lab demonstrates the successful installation and initial configuration of Ubuntu Linux within a virtualised environment. These skills are foundational for IT support, system administration, and further Linux-based learning.
