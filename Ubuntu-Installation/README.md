# Lab 6 — Installing Ubuntu Linux in VirtualBox

## Purpose
This lab shows how to install Ubuntu Linux inside a VirtualBox virtual machine. This provides a safe environment for learning Linux, practising command-line skills, and understanding open-source operating systems used in IT support and server administration.

## Tools Used
- Oracle VirtualBox
- Ubuntu Desktop ISO (24.04 LTS)
- Windows 11 host machine

## Steps Taken

### 1. Created a New Virtual Machine
I created a VM named **Ubuntu-Lab** with:
- 4GB RAM
- 2 CPU cores
- 30GB virtual hard disk
- Ubuntu (64-bit) OS type

### 2. Attached the Ubuntu ISO
In VirtualBox settings under **Storage**, I attached the Ubuntu ISO file to the virtual optical drive.

### 3. Booted the VM and Launched Installer
The VM booted into the Ubuntu GRUB menu.  
I selected **Try or Install Ubuntu** and then chose **Interactive Installation**.

### 4. Selected Installation Options
I kept the default settings and selected:
- Normal installation
- Download updates
- Install third-party software

### 5. Disk Setup
I selected **Erase disk and install Ubuntu**, which formats the virtual disk only.

### 6. User Account Setup
I created a Linux user account and continued with the installation.

### 7. Installation Process
Ubuntu copied files, installed the system, downloaded updates, and configured components.

### 8. First Boot and Basic Linux Commands
After restarting the VM, I reached the Ubuntu desktop and opened the terminal to run:
- `ls`
- `pwd`
- `uname -a`
- `sudo apt update`

These commands confirm that the system is working and able to update packages.

## Screenshots
Screenshots are stored in the `screenshots` folder and include:
1. Main installer screen (“Try Ubuntu / Install Ubuntu”)
2. Interactive Installation screen
3. Disk setup (“Erase disk and install Ubuntu”)
4. User account creation screen
5. Installation progress
6. First Ubuntu desktop
7. Terminal with Linux commands

## What I Learned
- How to install Ubuntu inside a virtual machine  
- Basics of Linux system setup and user creation  
- How to use common terminal commands  
- Understanding of virtual disks and OS installation workflows  
