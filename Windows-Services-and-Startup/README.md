# Lab 10 – Windows Services & Startup Optimisation

## Purpose
The purpose of this lab is to demonstrate the ability to manage Windows startup programs, configure Windows services, and use advanced Sysinternals tools to analyse system performance. These are essential troubleshooting skills in IT support and helpdesk environments.

## Tools Used
- Windows 10 Virtual Machine  
- Task Manager  
- Services Console (services.msc)  
- Sysinternals Autoruns (Microsoft)

---

## Steps Performed

### 1. Reviewed Startup Applications  
Opened Task Manager → Startup to view all programs that run automatically at login. Checked their startup impact to identify potential performance issues.

*Screenshot: Startup apps list*

---

### 2. Disabled a Non-Essential Startup Item  
Disabled Microsoft OneDrive to reduce login time and optimise system performance.

*Screenshot: Disabled OneDrive*

---

### 3. Opened the Windows Services Console  
Launched services.msc to view Windows background services, their states, and their roles in system operation.

*Screenshot: Services console*

---

### 4. Restarted a Safe Windows Service  
Restarted a non-critical service (e.g., Print Spooler, Windows Time, BITS, or Themes) to demonstrate safe troubleshooting of service-related issues.

*Screenshot: Service restart*

---

### 5. Changed a Service Startup Type  
Selected a safe optional service (e.g., Xbox Services, Bluetooth Support Service) and changed the Startup Type to Manual to demonstrate understanding of service configuration.

*Screenshot: Startup type changed*

---

### 6. Analysed Startup Items Using Sysinternals Autoruns  
Used Autoruns to inspect hidden startup entries not visible in Task Manager. Focused on the Logon / Winlogon tab to review what executes when the user logs in.

*Screenshot: Autoruns Logon tab*

---

## What I Learned
- How startup programs impact system performance  
- How to disable or manage startup applications  
- How different service states and startup types work  
- How to safely restart Windows services  
- How to use Sysinternals Autoruns for advanced startup analysis  
- How to identify potential performance or security issues related to automatic startup behaviour

## Why This Lab Matters
These tasks closely mirror real-world IT support responsibilities, including:

- Fixing slow PCs  
- Troubleshooting login delays  
- Diagnosing misconfigured or failing services  
- Detecting unnecessary or suspicious startup processes  

This lab strengthens core skills required for helpdesk and junior system administration roles.

