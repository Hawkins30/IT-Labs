# Lab 12 — Windows Updates & Troubleshooting

## Purpose

The purpose of this lab is to demonstrate how to manage Windows Updates, review update history, run the built-in Windows Update Troubleshooter, and manually reset Windows Update components. These are essential troubleshooting tasks in real IT support environments where update failures, stuck downloads, or slow update performance are common issues.

---

## Tools Used

- Windows 10 Virtual Machine  
- Windows Update  
- Windows Troubleshooter  
- Command Prompt (Administrator)

---

## Steps Performed

### 1. Accessed Windows Update

Opened **Settings → Update & Security → Windows Update** to review the system’s current update status and configuration.

**Screenshot:** Windows Update main page.

---

### 2. Checked for Windows Updates

Clicked **Check for updates** to initiate a manual update scan.  
Observed the update process, including download, installation, and completion status.

This step demonstrates how technicians verify whether a system is fully up to date.

**Screenshot:** Updates downloading/installing or “You’re up to date” status.

---

### 3. Viewed Update History

Navigated to **View update history** to review previously installed updates, including:

- Quality updates  
- Driver updates  
- Definition updates  
- Any failed or pending updates  

Update history is a key diagnostic area for identifying failed patches or problematic drivers.

**Screenshot:** Windows Update history page.

---

### 4. Ran the Windows Update Troubleshooter

Opened **Settings → Update & Security → Troubleshoot → Additional troubleshooters**  
Ran the **Windows Update Troubleshooter** to automatically detect and resolve common update-related issues.

Possible results include:
- Issues found and fixed  
- Issues found but not fixed  
- No issues detected  

**Screenshot:** Windows Update Troubleshooter running or results screen.

---

### 5. Cleared the Windows Update Cache

Opened **Command Prompt as Administrator** and reset Windows Update components by stopping services, clearing the update cache, and restarting services.

Actions performed:
- Stopped the Windows Update service  
- Stopped the Background Intelligent Transfer Service (BITS)  
- Cleared the SoftwareDistribution folder  
- Restarted required services  

This process is commonly used in real IT environments when updates fail, loop, or become stuck.

**Screenshot:** Command Prompt showing Windows Update reset commands.

---

## What I Learned

- How to manually check for and install Windows updates  
- How to analyse update history to identify failures or driver issues  
- How to use the Windows Update Troubleshooter effectively  
- How to reset Windows Update components using Command Prompt  
- How common Windows Update issues are diagnosed and resolved in IT support roles  

---

## Why This Lab Matters

Windows Update issues are among the most frequent problems handled by IT support technicians.  
This lab demonstrates practical troubleshooting skills required to:

- Resolve failed or incomplete updates  
- Clear stuck or corrupted update downloads  
- Repair Windows Update functionality  
- Maintain system security and stability  

These skills are essential for **CompTIA A+** and real-world **helpdesk and desktop support** roles.
