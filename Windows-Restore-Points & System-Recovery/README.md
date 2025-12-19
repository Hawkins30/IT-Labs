# Lab 14 — Windows Restore Points & System Recovery

## Purpose

The purpose of this lab is to demonstrate how to create, configure, and use Windows System Restore Points on a Windows 10 system. This process allows IT support technicians to safely revert a system to a previous stable state after software issues, misconfiguration, or user error, without affecting personal files.

## Tools Used

- Windows 10 Virtual Machine
- System Protection (System Restore)
- Windows Recovery Tools

## Steps Performed

### 1. Opened System Protection

- Searched for **Create a restore point** in the Start Menu
- Opened **System Properties → System Protection**

### 2. Enabled System Protection

- Selected **C: (System)**
- Clicked **Configure**
- Enabled **Turn on system protection**
- Set **Max Usage** to 5%
- Applied and saved the configuration

### 3. Created a Restore Point

- Clicked **Create**
- Named the restore point **Before-Test**
- Verified that the restore point was created successfully

### 4. Made a System Change

- Created a test folder named **RestoreTest** on the Desktop  
  *(This represents a system or user-level change that may need to be reverted)*

### 5. Performed System Restore

- Opened **System Restore**
- Selected the restore point **Before-Test**
- Followed the wizard (**Next → Finish**)
- System rebooted and restored to the previous state

## Screenshots

Screenshots are stored in the `screenshots` folder and include:

1. System Protection tab open
2. System Protection enabled for C:
3. Restore point creation confirmation
4. Test system change visible
5. System Restore wizard before restore
6. Test change removed after restore

## What I Learned

- How to enable and configure Windows System Protection
- How to create and name restore points
- How to revert a system to a previous state using System Restore
- How technicians use restore points for troubleshooting and recovery
- How to verify system state before and after recovery
