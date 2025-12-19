# Lab 10 — Windows Services & Startup Optimisation

## Purpose

The purpose of this lab is to demonstrate the ability to manage Windows startup applications, configure and troubleshoot Windows services, and analyse startup behaviour using advanced Sysinternals tools. These are core troubleshooting skills required in IT support, helpdesk, and junior system administration roles, particularly when diagnosing slow boot times, login delays, or background service issues.

---

## Tools Used

- Windows 10 Virtual Machine  
- Task Manager  
- Services Console (`services.msc`)  
- Sysinternals Autoruns (Microsoft)

---

## Steps Performed

### 1. Reviewed Startup Applications

Opened **Task Manager → Startup** to review all applications configured to run automatically at user login.  
Checked the **Startup Impact** column to identify applications that could negatively affect boot and login performance.

**Screenshot:** Startup applications list with impact ratings.

---

### 2. Disabled a Non-Essential Startup Item

Disabled **Microsoft OneDrive** from startup to reduce unnecessary background processes and improve login performance.  
Confirmed the status changed to **Disabled**.

**Screenshot:** OneDrive disabled in Startup tab.

---

### 3. Opened the Windows Services Console

Launched the **Services Console (`services.msc`)** to review installed Windows services, their current state (Running / Stopped), and startup type (Automatic / Manual / Disabled).  
Reviewed service descriptions to understand their function and importance.

**Screenshot:** Services console overview.

---

### 4. Restarted a Safe Windows Service

Restarted a **non-critical Windows service** (e.g. Print Spooler, Windows Time, BITS, or Themes) to demonstrate safe service troubleshooting procedures.  
Verified the service restarted successfully without system instability.

**Screenshot:** Service restart action.

---

### 5. Changed a Service Startup Type

Selected a **safe, optional service** (e.g. Xbox Services or Bluetooth Support Service) and changed its **Startup Type** from *Automatic* to *Manual*.  
This demonstrates understanding of how startup types affect system behaviour and resource usage.

**Screenshot:** Startup type configuration change.

---

### 6. Analysed Startup Items Using Sysinternals Autoruns

Used **Sysinternals Autoruns** to inspect startup entries not visible in Task Manager.  
Focused on the **Logon** and **Winlogon** tabs to review processes that execute automatically when a user signs in.

**Screenshot:** Autoruns Logon tab showing startup entries.

---

## What I Learned

- How startup programs impact Windows boot and login performance  
- How to enable, disable, and manage startup applications safely  
- How Windows services operate and differ by startup type  
- How to restart services as part of troubleshooting workflows  
- How to use Sysinternals Autoruns for advanced startup analysis  
- How to identify unnecessary or potentially problematic startup behaviour

---

## Why This Lab Matters

These tasks closely reflect real-world IT support responsibilities, including:

- Troubleshooting slow system startup or login delays  
- Optimising system performance for end users  
- Diagnosing service-related issues  
- Identifying unnecessary or suspicious startup processes  
- Applying safe changes without disrupting system stability  

This lab strengthens essential skills required for **helpdesk**, **desktop support**, and **junior system administration** roles.
