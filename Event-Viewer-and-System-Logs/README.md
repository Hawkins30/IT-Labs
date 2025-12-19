# Lab 11 — Event Viewer & System Logs

## Lab Objective
Demonstrate the ability to access, analyse, filter, and export Windows system and application logs using Event Viewer in order to support structured troubleshooting and escalation in an IT support environment.

---

## Scenario
A support technician is required to investigate potential system and application issues on a Windows workstation by reviewing system logs, identifying relevant errors and warnings, and preparing log data for further analysis or escalation.

---

## Environment
- **Operating System:** Windows 10  
- **Tool Used:** Event Viewer (`eventvwr.msc`)

---

## Investigation Steps

### 1. Opened Event Viewer
Launched Event Viewer using:
"Win + R → eventvwr.msc"

This displayed the main Event Viewer console.

---

### 2. Reviewed System Logs
Navigated to:
"Windows Logs → System"

Reviewed system-level events related to:
- Hardware issues  
- Driver problems  
- Service failures  

This log is commonly used to diagnose system stability and boot-related issues.

---

### 3. Investigated a System Error
Selected an error-level event and reviewed detailed information including:
- Event ID  
- Source  
- Log level  
- Description  

This information is critical for identifying the cause of system issues and researching known errors.

---

### 4. Reviewed Application Logs
Navigated to:
"Windows Logs → Application"

Examined software-related events such as:
- Application crashes  
- Application warnings  
- Service-related application issues  

This log is used to diagnose problems affecting installed software.

---

### 5. Filtered the System Log
Applied a filter to the System log using:
"Filter Current Log…"

Filtered by:
- Event Level: Error  
- Event Level: Warning  

This allowed rapid identification of critical issues within a large volume of log entries.

---

### 6. Created a Custom View
Created a custom view under:
"Custom Views → Create Custom View"

Configured the view with the following settings:
- Logged: Last hour  
- Event Levels: Error and Warning  
- Logs: System and Application  

Saved the view as:
"Errors and Warnings — Last Hour"

Custom views are commonly used in real IT environments to quickly monitor recent issues.

---

### 7. Exported the System Log
Exported system logs using:
"Windows Logs → System → Save All Events As…"

Saved the file as:
"system-log.evtx"

Exporting logs is essential for documentation, escalation, and collaboration with senior support teams.

---

## Verification
- System and application logs successfully accessed  
- Errors and warnings identified and reviewed  
- Filters and custom views applied correctly  
- Logs exported in `.evtx` format for further analysis  

---

## Outcome
System and application log data was successfully analysed, filtered, and exported, demonstrating effective use of Event Viewer for troubleshooting and escalation purposes.

---

## Key Takeaways
- How to navigate and use Windows Event Viewer  
- Differences between System and Application logs  
- How to interpret Event IDs, sources, and log levels  
- How to filter logs to identify critical issues quickly  
- How to create and save custom views for rapid troubleshooting  
- How to export logs for analysis or escalation  

---

## Evidence
Screenshots documenting each step are stored in the `/screenshots` directory, including:
- Event Viewer main console  
- System log with errors and warnings visible  
- Detailed view of a system error  
- Application log entries  
- Filtered log view  
- Custom view displayed in the navigation pane  
- Exported `.evtx` log file  

---

## Why This Lab Matters
Windows Event Viewer is one of the most important troubleshooting tools in IT support. It is routinely used to diagnose:
- Service failures  
- Driver issues  
- System crashes  
- Application errors  
- Boot problems  
- Network-related issues  

Proficiency with Event Viewer is essential for both entry-level IT support roles and real-world helpdesk environments.
