# Lab 7 — Windows System Health Check & Performance Diagnostics

## Purpose

The purpose of this lab is to perform a full system health check on a Windows 10 virtual machine. This lab demonstrates core IT support skills including performance analysis, event log investigation, system integrity verification, update management, and reliability monitoring. These tasks reflect real-world troubleshooting and diagnostic procedures used by IT support technicians.

---

## Tools Used

- Windows 10 Virtual Machine  
- Task Manager  
- Event Viewer  
- Reliability Monitor  
- Command Prompt (Administrator)  
- Windows Update  

---

## Steps Taken

### 1. Checked System Performance (Task Manager)

I opened **Task Manager** and used the **Performance** tab to review:

- CPU usage  
- Memory usage  
- Disk usage  
- Network activity  

This provided a quick overview of system resource utilisation and helped identify potential performance bottlenecks.

---

### 2. Reviewed Windows Event Logs

I opened **Event Viewer** and examined the following logs:

- **System Logs** for hardware, driver, and OS-level issues  
- **Application Logs** for software-related warnings and errors  

Event Viewer helps diagnose the root causes of crashes, freezes, and performance degradation.

---

### 3. Checked System Stability (Reliability Monitor)

I launched **Reliability Monitor** to view the system stability index and timeline.

This tool displays:

- Application crashes  
- Windows failures  
- Driver issues  
- System warnings  

It provides a historical view of system health and reliability trends over time.

---

### 4. Checked Disk Health

Using **Command Prompt**, I ran the following command:
"wmic diskdrive get status"

This command checks whether the virtual disk reports any hardware issues.  
The disk status returned **Healthy / OK**.

---

### 5. Checked Windows Updates

I opened **Settings → Update & Security → Windows Update** and verified:

- Whether updates were missing  
- Whether the system was fully patched  
- Whether any updates had failed  

This confirms the system is up to date and protected against known vulnerabilities.

---

### 6. Ran an SFC System Integrity Scan

I opened **Command Prompt as Administrator** and ran:
"sfc /scannow"

This scan checks for corrupted system files and attempts automatic repair if issues are found.

---

### 7. Reviewed Results and Overall System Health

Based on the checks performed, I confirmed the system was healthy due to:

- Normal resource usage  
- No critical errors in Event Viewer  
- A stable reliability graph  
- Healthy disk status  
- No integrity violations reported by SFC  

---

## Screenshots

Screenshots included in the `/screenshots` folder:

1. Task Manager — Performance tab  
2. Event Viewer — System logs  
3. Event Viewer — Application logs  
4. Reliability Monitor graph  
5. Windows Update status  
6. Disk health (`wmic diskdrive get status`)  
7. SFC scan results  

---

## What I Learned

- How to diagnose slow or unstable Windows systems  
- How to analyse Windows Event Logs to identify system issues  
- How to monitor system reliability trends  
- How to verify system file integrity using SFC  
- How to confirm disk health status  
- How to validate Windows update and patch status  
- How IT technicians perform real-world system health checks  
