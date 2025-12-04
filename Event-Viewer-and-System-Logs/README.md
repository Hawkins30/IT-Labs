# Lab 11 – Event Viewer & System Logs

## Purpose
The purpose of this lab is to demonstrate the ability to access, analyse, filter, and export Windows system logs using the Event Viewer. These skills are essential for troubleshooting system issues, diagnosing errors, and supporting users in real IT helpdesk environments.

## Tools Used
- Windows 10  
- Event Viewer (eventvwr.msc)

---

## Steps Performed

### 1. Opened Event Viewer
Used Win + R → `eventvwr.msc` to open the Windows Event Viewer and display the main console.

*Screenshot: Event Viewer main window*

---

### 2. Viewed System Logs
Navigated to **Windows Logs → System** to review system-level events such as hardware issues, driver problems, and service failures.

*Screenshot: System log with errors/warnings visible*

---

### 3. Investigated a System Error
Selected a red error entry and reviewed its detailed information, including:
- Event ID  
- Source  
- Log level  
- Description  

This demonstrates the ability to understand and interpret log data.

*Screenshot: System error details*

---

### 4. Opened Application Logs
Navigated to **Windows Logs → Application** to examine software-related errors and warnings, such as application crashes or service issues.

*Screenshot: Application log error/warning*

---

### 5. Filtered the System Log
Right-clicked **System → Filter Current Log…** and filtered by:
- Error  
- Warning  

This shows the ability to quickly isolate important issues in a busy log.

*Screenshot: Filtered log showing only errors and warnings*

---

### 6. Created a Custom View
Created a custom view under:
**Custom Views → Create Custom View**

Settings:
- Logged: Last hour  
- Event Levels: Error + Warning  
- Logs: System + Application  

Named it:  
`Errors and Warnings – Last Hour`

This is a common task in real IT troubleshooting.

*Screenshot: Custom View displayed in left pane*

---

### 7. Exported the System Log
Right-clicked **Windows Logs → System → Save All Events As…**  
Saved the log as `system-log.evtx` on the desktop.

This demonstrates the ability to export logs for escalation or documentation purposes.

*Screenshot: Saved .evtx file*

---

## What I Learned
- How to navigate Windows Event Viewer  
- Differences between System, Application, and other log types  
- How to interpret log details such as Event IDs and sources  
- How to filter logs to find critical issues quickly  
- How to create and save custom views for rapid troubleshooting  
- How to export logs for analysis or escalation  

---

## Why This Lab Matters
Windows Event Viewer is one of the most important troubleshooting tools in IT support.  
It is used to diagnose:
- Service failures  
- Driver issues  
- System crashes  
- Application errors  
- Boot problems  
- Network issues  

Mastering Event Viewer is essential for both CompTIA A+ and real-world helpdesk roles.

