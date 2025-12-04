# Lab 12 – Windows Updates & Troubleshooting

## Purpose
The purpose of this lab is to demonstrate how to manage Windows Updates, analyse update history, run the built-in Windows Update Troubleshooter, and manually clear the Windows Update cache. These are essential tasks in real IT support environments where update failures and slow update performance are common issues.

## Tools Used
- Windows 10  
- Windows Update  
- Windows Troubleshooter  
- Command Prompt (Administrator)

---

## Steps Performed

### 1. Accessed Windows Update  
Opened **Settings → Update & Security → Windows Update** to view the system’s update status.

*Screenshot: Windows Update main page*

---

### 2. Checked for Windows Updates  
Clicked **Check for updates** to initiate a manual scan. Demonstrated how updates download, install, and complete.

*Screenshot: Updates downloading/installing or “You’re up to date”*

---

### 3. Viewed Update History  
Navigated to **Update history** to review:
- Quality updates  
- Driver updates  
- Definition updates  
- Any failed updates  

This is an important diagnostic area for helpdesk technicians.

*Screenshot: Update history page*

---

### 4. Ran the Windows Update Troubleshooter  
Opened **Settings → Update & Security → Troubleshoot → Additional troubleshooters**  
Ran the **Windows Update Troubleshooter** to detect and fix common problems.

The troubleshooter results may include:
- Issues found  
- Issues fixed  
- No issues detected  

*Screenshot: Troubleshooter running/results screen*

---

### 5. Cleared the Windows Update Cache  
Used Command Prompt (Admin) to reset the Windows Update components.

Commands used:

```
net stop wuauserv
net stop bits
del /s /q C:\Windows\SoftwareDistribution
net start wuauserv
net start bits
```

This is a common real-world fix when updates fail to install or get stuck.

*Screenshot: Command prompt showing update cache reset commands*

---

## What I Learned
- How to manually check for and install Windows updates  
- How to analyse update history for failures or driver issues  
- How to use the Windows Update Troubleshooter  
- How to reset the Windows Update components using Command Prompt  
- How update failures can be diagnosed and resolved in a real IT support environment  

---

## Why This Lab Matters
Windows Update issues are one of the most frequent problems faced by IT support technicians.  
This lab demonstrates practical troubleshooting skills needed to:

- Resolve failed updates  
- Clear stuck downloads  
- Fix corrupted update files  
- Restore Windows Update functionality  

Mastering these steps is essential for CompTIA A+ and real helpdesk roles.

