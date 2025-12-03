# Lab 7 — Windows System Health Check & Performance Diagnostics

## Purpose
The purpose of this lab is to perform a full system health check on a Windows 10 virtual machine. This demonstrates core IT support skills including performance analysis, event log investigation, system integrity checks, update management, and reliability monitoring.

## Tools Used
- Windows 10 Virtual Machine
- Task Manager
- Event Viewer
- Reliability Monitor
- Command Prompt (Admin)
- Windows Update

## Steps Taken

### 1. Checked System Performance (Task Manager)
I opened Task Manager and used the **Performance** tab to view:
- CPU usage
- Memory usage
- Disk usage
- Network activity  
This provides a quick overview of system bottlenecks and resource usage.

### 2. Reviewed Windows Event Logs
I opened **Event Viewer** and examined:
- **System Logs** for driver, hardware, and OS-level issues  
- **Application Logs** for software-level warnings and errors  
Event Viewer helps diagnose causes behind crashes, freezes, and performance degradation.

### 3. Checked System Stability (Reliability Monitor)
I launched **Reliability Monitor** to view the system stability graph.  
This tool shows:
- Application crashes
- Windows failures
- Driver issues
- System warnings  
It provides a timeline of system health and reliability trends.

### 4. Checked Disk Health
In Command Prompt, I ran: wmic diskdrive get status

This checks whether the virtual disk reports any hardware issues (Healthy/OK).

### 5. Checked Windows Updates
I opened **Settings → Update & Security → Windows Update**  
This confirmed:
- Whether updates were missing
- Whether the system was fully patched
- If any updates had failed  

### 6. Ran an SFC System Integrity Scan
I opened Command Prompt as Administrator and ran: sfc /scannow
This checks for corrupted system files and attempts automatic repair.

### 7. Reviewed Results and System Health
I confirmed the system was healthy based on:
- Normal resource usage
- No critical errors in Event Viewer
- Stable reliability graph
- Healthy disk status
- No integrity violations from SFC scan

## Screenshots
Screenshots included in the `screenshots` folder:
1. Task Manager – Performance tab  
2. Event Viewer – System logs  
3. Event Viewer – Application logs  
4. Reliability Monitor graph  
5. Windows Update status  
6. Disk health (`wmic diskdrive get status`)  
7. SFC scan results  

## What I Learned
- How to diagnose slow or unstable Windows systems  
- How to read Windows event logs and identify issues  
- How to monitor system reliability trends  
- How to check system file integrity using SFC  
- How to verify disk health  
- How to confirm update and patch status  
- How technicians perform real-world system health checks




