# Lab 14 — Windows Restore Points & System Recovery

## Purpose
This lab demonstrates how to create, configure, and restore Windows System Restore Points.  
Restore Points allow IT technicians to revert a system back to a previous stable state after system changes, software issues, misconfiguration, or user error.

## Tools Used
- Windows 10 Virtual Machine  
- System Protection (System Restore)  
- Windows Recovery Tools

---

## Steps Performed

### **1. Open System Protection**
- Searched for **“Create a restore point”** in the Start Menu.  
- Opened **System Properties → System Protection**.  
**Screenshot 1:** System Protection tab open.

---

### **2. Enable System Protection**
- Selected **C: (System)**.  
- Clicked **Configure**.  
- Enabled: **Turn on system protection**.  
- Set **Max Usage** to 5%.  
- Applied settings.  
**Screenshot 2:** Protection enabled for C:.

---

### **3. Create a Restore Point**
- Clicked **Create…**  
- Named restore point: **Before-Test**  
- Restore point created successfully.  
**Screenshot 3:** Confirmation message shown.

---

### **4. Make a System Change**
- Created a test folder named **RestoreTest** on the Desktop  
  (or optionally installed a small program).  
**Screenshot 4:** Change visible on the system.

---

### **5. Perform System Restore**
- Opened **System Restore…**  
- Selected restore point **Before-Test**.  
- Followed wizard → **Next → Finish**.  
- VM rebooted and restored to previous state.  
**Screenshot 5:** System Restore wizard before restore.  
**Screenshot 6:** Evidence that the test change was removed after restore.

---

## Outcome
✔ System protection was successfully enabled.  
✔ Restore point created and verified.  
✔ System changes were reverted using System Restore.  
✔ Windows recovery process fully tested.

This demonstrates key A+ troubleshooting skills:  
- Using restore points to undo system issues  
- Understanding recovery features  
- Verifying system state before and after restore  

---

## Folder Structure

Lab-14-Restore-Points/
│── screenshots/
│── README.md


---

## Status
**Lab Completed Successfully ✅**

## Folder Structure

